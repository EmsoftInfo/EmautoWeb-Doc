![EMAUTO Web](https://www.emsoft.inf.br/wp-content/uploads/2018/08/logo_horizontal_160x40.png)
# Documentação EMAutoWeb


## Detalhando as funções PHP


### filtroURL

Função responsável por filtrar URLs, removendo possíveis comandos maliciosos, mas preservando caracteres importantes para URLs.

Exemplo de uso:
```php
<?php
$var = FiltroURL("@urlaqui#");
// Saída: urlaqui
?>
```

### filtroHTML
A função `FiltroHTML` é responsável por filtrar elementos HTML, removendo comandos maliciosos e garantindo a segurança contra possíveis vulnerabilidades.

Exemplo de uso
```php
<?php
$var = FiltroHTML("<a href='test'>Test</a>");
// Saída: &lt;a href=&#039;test&#039;&gt;Test&lt;/a&gt;
?>
```

### chaveURL
Função que converte os parâmetros presentes na URL em base64.

Exemplo de uso
```php
<?php
$var = ChaveURL("01.00.00");
// Saída: MDEuMDAuMDA=
?>
```

### filtro
Esta função é amplamente utilizada em várias ações no sistema para sanitizar comandos ou caracteres maliciosos.

Exemplo de uso
```php
<?php
$var = Filtro(" UNION textoaqui ' SELECT");
// Saída: textoaqui
?>
```

### filtroNUM 
A função `FiltroNUM` é utilizada para sanitizar variáveis, removendo todos os caracteres que não são números inteiros.

Exemplo de uso
```php
<?php
$var = FiltroNUM("Teste05044ff");
// Saída: 05044
?>
```

### verificaLogado 
A função `verificaLogado` é utilizada para verificar se existe um usuário logado, para exibir e realizar as solicitações posteriores. Se não existir usuário logado, a página de login é requisitada

Exemplo de uso
```php
<?php
$var = verificaLogado("$_SESSION['chave']","$_SESSION['usuario']");
?>
```

