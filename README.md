![EMAUTO Web](https://www.emsoft.inf.br/wp-content/uploads/2018/08/logo_horizontal_160x40.png)
# Documentação EMAutoWeb
## Introdução.

O EMAutoWeb é mais do que apenas um sistema; é a próxima evolução na gestão de autopeças e serviços automotivos. Anteriormente disponível apenas como um sistema desktop, agora estamos levando esse poderoso ERP (Enterprise Resource Planning) para o mundo da web, tornando-o mais acessível, ágil e amigável.

O EMAutoWeb é um sistema especialmente projetado para atender às necessidades de negócios no setor de autopeças. Sua funcionalidade abrangente cobre todos os aspectos da gestão, desde o controle de estoque e vendas até a gestão financeira, proporcionando um fluxo de trabalho eficiente e uma visão abrangente do seu negócio. 

O que diferencia o EMAutoWeb é o compromisso com o suporte ao cliente de maneira verdadeiramente humanizada. Valorizamos cada cliente e estamos empenhados em fornecer assistência personalizada para garantir que você aproveite ao máximo o sistema. Não apenas vendemos um software, mas também construímos relacionamentos duradouros com nossos clientes.

Embora inicialmente tenhamos concentrado nossos esforços no Rio de Janeiro, a versão web do EMAutoWeb permitirá que autopeças de todo o Brasil e além tenham acesso a essa ferramenta poderosa. Estamos comprometidos em fornecer uma solução que não apenas melhore a eficiência dos negócios, mas também eleve a experiência do usuário a um novo patamar.

Com a adaptação para a versão web, o EMAutoWeb está pronto para revolucionar a forma como o setor de autopeças gerencia seus negócios. Seja bem-vindo à nova era da gestão de autopeças, onde eficiência, acessibilidade e suporte humanizado se encontram.

### Objetivos
O EMAutoWeb tem como objetivo simplificar e otimizar a gestão de negócios no setor de autopeças por meio de uma plataforma web acessível, proporcionando aos usuários uma maneira eficiente de gerenciar estoque, vendas, finanças e outras operações essenciais.


### Características 
Linguagens de Programação Utilizadas: PHP e JavaScript
Bibliotecas e Frameworks: Jquey, BootStrap e Ionicons

Requisitos para utilização:
Apache HTTP Server
PHP 8.1+
Navegadores com suporte ao ECMAScript 6


## Arquitetura


### Estrutura de Pastas:

Estrutura de Pastas do Projeto ERP*

*Diretório Inicial:*
- `app`: Este diretório contém a lógica do lado do servidor do aplicativo ERP.
- `public`: Este diretório contém ativos e recursos acessíveis diretamente pelo navegador.

*Arquivos:*
- `index.php`: Este arquivo é a entrada principal do aplicativo ERP e é responsável por iniciar o aplicativo.
- `autoload.php`: Este arquivo é usado para carregar automaticamente classes e recursos do aplicativo.

*Pasta `public`:*
- `css`: Contém arquivos de estilo (CSS) usados para estilizar as páginas do aplicativo.
- `js`: Contém arquivos JavaScript usados para funcionalidades dinâmicas no aplicativo.
- `midia`: Possui recursos de mídia, como imagens e vídeos, usados no aplicativo.
- `pages`: Contém páginas do aplicativo acessadas diretamente pelos usuários.
- `template`: Armazena templates ou layouts usados para renderizar as páginas do aplicativo.

*Pasta `app`:*
- `classes`: Este diretório contém classes PHP que implementam a lógica de negócios do aplicativo ERP.
- `config`: Armazena arquivos de configuração que definem variáveis de ambiente e configurações do aplicativo.
- `controles`: Contém scripts ou classes que atuam como controladores, gerenciando as interações entre as páginas e a lógica de negócios.
- `includes`: Guarda arquivos que são incluídos em várias partes do aplicativo para reutilização de código.
- `temp`: Pode ser usado para armazenar arquivos temporários ou caches usados pelo aplicativo.

### Arquitetura utilizada

Arquitetura Modular e Hierárquica - Documentação Técnica*

*1. Visão Geral:*

A arquitetura "Modular e Hierárquica" é a base da estrutura do projeto ERP. Ela enfatiza a organização e a divisão eficaz das responsabilidades em um ambiente de desenvolvimento web. Embora não se enquadre em um padrão de projeto específico, essa arquitetura oferece flexibilidade, escalabilidade e reutilização de código.

*2. Principais Componentes:*

- *Páginas (Pages)*: As páginas da interface do usuário são a face visível do aplicativo e estão contidas no diretório `public/pages`. Elas são compostas dinamicamente com base nas necessidades do usuário.

- *Classes de Lógica (Logic Classes)*: As classes PHP em `app/classes` implementam a lógica de negócios do ERP. Cada classe tem uma única responsabilidade bem definida, promovendo a reutilização de código.

- *Controladores (Controllers)*: Os controladores no diretório `app/controles` atuam como intermediários entre as páginas da interface do usuário e as classes de lógica de negócios. Eles gerenciam as interações e as solicitações entre essas partes.

- *Recursos Públicos (Public Resources)*: Os recursos acessíveis diretamente pelo navegador, como arquivos CSS, JavaScript e mídia, são mantidos em `public/css`, `public/js` e `public/midia`, respectivamente.

*3. Funcionamento Geral:*

- *Inclusões de Página*: O arquivo `index.php` atua como o ponto de entrada. Inicialmente, chama a página de login e, após o login bem-sucedido, redireciona para a página inicial. As inclusões de página são feitas por meio do comando `include`.

- *Controle de Acesso*: O controle de acesso é implementado para garantir que os usuários autorizados acessem as páginas corretas. A classe `VerificaPages` em `app/classes/VerificaPages.php` gerencia o controle de acesso.

- *Composição de Páginas*: As páginas são compostas dinamicamente, com a lógica da classe `VerificaPages` determinando as informações, cores, títulos e conteúdo a serem exibidos.

- *Interação AJAX*: O JavaScript em `public/js` é usado para manipular o DOM e para interações AJAX, permitindo atualizações dinâmicas da interface do usuário.

- *Requisições API*: A classe `RequisicoesAPI` é responsável por tratar as solicitações da API. Ela recebe solicitações de outras classes e arquivos, processa-as e retorna resultados.

- *Componentes de Interface*: Elementos da interface, como formulários, modais e colapsos, são requisitados pela classe `VerificaPages`, que busca por esses componentes na pasta `includes` em `app`.

*4. Benefícios:*

- *Organização Eficiente*: A arquitetura modular facilita a organização e a manutenção do código.

- *Reutilização de Código*: O uso de classes e componentes promove a reutilização de código, reduzindo a duplicação.

- *Flexibilidade na Interface*: A composição dinâmica das páginas permite uma interface flexível e personalizável.

- *Segurança*: O controle de acesso e a autenticação são implementados para garantir a segurança do aplicativo.

*5. Desafios Potenciais:*

- *Complexidade Crescente*: À medida que o projeto cresce, a complexidade pode aumentar, tornando a manutenção mais desafiadora.

- *Desempenho*: Muitas inclusões de arquivos e solicitações AJAX podem afetar o desempenho, tornando o aplicativo mais lento.

- *Curva de Aprendizado*: A estrutura pode ter uma curva de aprendizado para novos desenvolvedores que entram no projeto.

- *Dependência de JavaScript*: A funcionalidade do aplicativo depende fortemente do JavaScript, o que pode ser um problema se o usuário desativar o JavaScript no navegador.






