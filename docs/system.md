![EMAUTO Web](https://www.emsoft.inf.br/wp-content/uploads/2018/08/logo_horizontal_160x40.png)
# Documentação EMAutoWeb
## Arquitetura.



### Estrutura de Pastas:

Estrutura de Pastas do Projeto ERP*

*Diretório Inicial:*
<pre>
- `app`: Este diretório contém a lógica do lado do servidor do aplicativo ERP.
- `public`: Este diretório contém ativos e recursos acessíveis diretamente pelo navegador.
</pre>
*Arquivos:*
<pre>
- `index.php`: Este arquivo é a entrada principal do aplicativo ERP e é responsável por iniciar o aplicativo.
- `autoload.php`: Este arquivo é usado para carregar automaticamente classes e recursos do aplicativo.
</pre>
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


### Lógica

*Lógica do Projeto ERP - Documentação Técnica*

*1. Fluxo Inicial:*

O sistema ERP segue um fluxo inicial a partir do arquivo `index.php`, que é o ponto de entrada principal do aplicativo. O fluxo é o seguinte:

- Quando o usuário não fez login, o `index.php` verifica e chama a página de login, que está localizada em `public/pages/login.php`. O acesso direto à página é evitado, e a inclusão da página é realizada via PHP (`include`).

*2. Página de Login:*

- A página de login apresenta um formulário onde o usuário fornece suas credenciais (como nome de usuário e senha).
- O JavaScript pode ser usado para validar as entradas do usuário e enviar uma solicitação AJAX para o servidor.
- No lado do servidor, a lógica de login verifica as credenciais, autentica o usuário e cria uma sessão ou token de autenticação.
- Após o login bem-sucedido, o usuário é redirecionado para a página inicial.

*3. Página Inicial (Home):*

- A página inicial (`public/pages/home.php`) é a primeira página após o login.
- Ela contém chamadas AJAX em JavaScript para incluir o menu lateral e o topo da página.
- O menu lateral lista todas as rotas das páginas, mas o acesso direto a elas é desencorajado. Em vez disso, o menu envia uma solicitação GET para o `index.php`, indicando a página desejada.
- O arquivo `index.php` chama a classe `VerificaPages` localizada em `app/classes/VerificaPages.php` para determinar se a página solicitada existe.

*4. Verificação e Montagem de Páginas:*

- A classe `VerificaPages` é responsável por verificar a existência da página e fornecer informações, como cores, título e conteúdo da página.
- O `index.php` lê as informações retornadas pela classe e monta a página para o cliente.
- Os arquivos JavaScript em `public/js` são responsáveis por manipulações no DOM e na interface do usuário à medida que o usuário interage com a página.

*5. Solicitações da API:*

- Os dados são recebidos via API. Uma classe chamada `RequisicoesAPI` é responsável por tratar todas as solicitações de outras classes e arquivos.
- Ela retorna os resultados obtidos após processar as solicitações.

*6. Acesso a Novas Páginas:*

- Ao acessar uma nova página, uma solicitação AJAX é feita ao arquivo `tabelas.php`, localizado em `app/controles/`.
- O arquivo `tabelas.php` faz uma solicitação à classe `RequisicoesAPI`.
- Após o sucesso da solicitação, `tabelas.php` retorna os resultados para a solicitação AJAX, que os apresenta na tela.

*7. Elementos da Tela:*

- Formulários, modais, collapses e outros elementos da interface são requisitados pela classe `VerificaPages`.
- A classe procura pelos elementos na pasta `includes`, que está dentro do diretório `app`.
- Se o arquivo for encontrado, a classe retorna o resultado para a exibição na tela.




