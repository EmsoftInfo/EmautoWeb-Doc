![EMAUTO Web](https://www.emsoft.inf.br/wp-content/uploads/2018/08/logo_horizontal_160x40.png)
# Documentação EMAutoWeb

## Funcionalidades Nativas do Sistema EMAutoWeb

As funcionalidades nativas do sistema EMAutoWeb permitem a criação de conteúdo de maneira mais rápida, fácil e dinâmica.


### Emauto_select

A funcionalidade `Emauto_select` permite a unificação de options repetidos dentro de um select. É útil quando o select obtém dados do servidor onde o valor trazido pode ser igual ao que já está na listagem, permitindo a unificação sem comprometer a integridade dos dados.

Exemplo de Uso:
```html
<select emauto_select>
    <option value=""></option>
</select>
```


### Datalist

A funcionalidade `Datalist` é dependente de outros fatores, como o banco de dados, para trazer os dados necessários. Para construí-la, é necessário adicionar a tag `emauto_datalist_ref="Referencia"` ao elemento input. A referência sempre será o nome ou o ID do elemento input, que também deve ser usado na tag ul abaixo para sugerir dados durante a digitação do usuário. Além disso, é necessário também adicionar a tag `emauto_datalist=" ClasseAPI {CHAVE} {VALOR}"`, esta é responsável por buscador os dados no servidor.

Exemplo de Uso:
```html
<input type="text" emauto_datalist_ref="fornecedor" emauto_datalis="Fornecedor {ID} {NOME}">
<ul emauto_datalist_ref="fornecedor"></ul>
```


### Required

Ao utilizar o AJAX para o envio de requisições ao servidor, pode haver situações em que os inputs com atributos `required` ou regras nos seus valores não são validados corretamente. Nesse contexto, o sistema possui uma forma nativa de validação de dados.

O sistema emprega a validação dos dados antes do envio ao servidor. Para tornar um campo obrigatório durante o preenchimento, é utilizado o atributo `required`, da mesma forma como em qualquer outro elemento HTML presente na web.

O sistema realiza a validação para garantir que os dados obrigatórios tenham sido preenchidos antes do envio ao servidor. Isso permite uma verificação prévia dos campos, assegurando que informações cruciais estejam presentes antes da submissão da requisição AJAX.

Exemplo de Uso:
```html
<input type="text" required>

```


### Select com dados dos servidor

A função em PHP `GeraSelect()` é responsável por buscar os dados no servidor conforme os parâmetros fornecidos. Para gerar os elementos `<option>` de um `<select>`, são necessários três parâmetros: Endereço/ClasseAPI, Nome de Exibição e ID de Seleção, que será utilizado como valor.

É importante notar que, para a construção do `<select>`, o atributo `selected` do `<option>` precisa estar fora do escopo da função para possibilitar manipulações posteriores. Além disso, recomenda-se o uso do atributo `emauto_select` em conjunto com essa função para evitar a repetição dos dados, mantendo o `<option selected>` fora do escopo da função.

Exemplo de Utilização:

```php
<select class="form-control" id="fiscal" emauto_select>
    <option selected value=""></option>
    <?php echo GeraSelect("FormasDePagamentoFiscal", "Descricao", "ID"); ?>
  
</select>
```


### Edits

A função `VerificaSePaginaEdits` é responsável por verificar se a página atual corresponde à página de edição e habilita funções ou componentes específicos para esta condição. Esse recurso é especialmente útil quando um componente é reutilizado em várias páginas, como um formulário que é utilizado tanto para cadastro quanto para edição. No contexto de edição, podem ser necessárias funcionalidades adicionais que não estão presentes na página de cadastro.

O retorno desta função é um valor booleano: 
- Retorna `1` quando a página atual está no modo de edição.
- Retorna `0` quando não está no modo de edição.

 Exemplo de Utilização em JavaScript:
```javascript
<script>
import { VerificaSePaginaEdits } from '../js';

if (VerificaSePaginaEdits() == 1) {
    // Habilitar funcionalidades específicas para a página de edição
    // Coloque o código correspondente aqui
} else {
    // Tratar o caso em que não é uma página de edição (opcional)
}
</script>
```


### Máscaras 

As máscaras são aplicadas utilizando a biblioteca jQuery Mask, a qual é organizada em microfunções para facilitar a organização e manutenção do código.

Para utilizar as máscaras disponíveis, siga os seguintes passos:

- Passo 1: Definição dos Elementos HTML

No seu código HTML, defina os elementos nos quais deseja aplicar as máscaras. Utilize o atributo `emauto_mascara` para especificar o tipo de máscara desejada. Por exemplo:

```html
<input type="text" name="Comissao" emauto_mascara="Porcentagem">
<input type="text" name="CEP" emauto_mascara="Cep">
```

- Passo 2: Importação das Funções de Máscara

Realize a importação das funções de máscara desejadas no seu arquivo JavaScript para habilitar essas funcionalidades. Por exemplo:

```javascript
<script>
import { MascaraCEP, MascaraPorcentagem } from '../js';
// Importe as funções de máscara necessárias
</script>
```