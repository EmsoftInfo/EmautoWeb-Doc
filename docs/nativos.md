![EMAUTO Web](https://www.emsoft.inf.br/wp-content/uploads/2018/08/logo_horizontal_160x40.png)
# Documentação EMAutoWeb

## Funcionalidades Nativas do Sistema EMAutoWeb

As funcionalidades nativas do sistema EMAutoWeb permitem a criação de conteúdo de maneira mais rápida, fácil e dinâmica.


### Emauto_select

A funcionalidade `Emauto_select` permite a unificação de options repetidos dentro de um select. É útil quando o select obtém dados do servidor onde o valor traseiro pode ser igual ao que já está na listagem, permitindo a unificação sem comprometer a integridade dos dados.

Exemplo de Uso:
```html
<select emauto_select>
    <option value=""></option>
</select>
```


### Datalist

A funcionalidade `Datalist` é dependente de outros fatores, como o banco de dados, para trazer os dados necessários. Para construí-la, é necessário adicionar a tag `emauto_datalist="Referencia"` ao elemento input. A referência sempre será o nome ou o ID do elemento input, que também deve ser usado na tag ul abaixo para sugerir dados durante a digitação do usuário.

Exemplo de Uso:
```html
<input type="text" emauto_datalist="fornecedor">
<ul emauto_datalist="fornecedor"></ul>
```

