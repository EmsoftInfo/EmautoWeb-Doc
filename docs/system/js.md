![EMAUTO Web](https://www.emsoft.inf.br/wp-content/uploads/2018/08/logo_horizontal_160x40.png)
# Documentação EMAutoWeb
## Detalhando o JavaScript em suas relações.


A pasta `JS` contém os arquivos JavaScript que fornecem interatividade ao aplicativo, além das pastas `Acionadores` e `externos`.

### Arquivos JavaScript:

- **Pages.js**: Contém chamadas e funções para exibição de tabelas, paginação, buscas, filtros, exclusões e inclusões. Pode ser incluído em qualquer documento HTML ou PHP que necessite dessas funcionalidades. Realiza solicitações ao servidor e exibe os resultados. Deve ser incluído manualmente, pois não está presente em todas as páginas.

- **Principal.js**: Disponibiliza funções necessárias para todo o sistema. Presente em todas as páginas. Importa módulos extras, como a chamada do menu lateral.

- **Login.js**: Presente apenas na página de login. Captura dados preenchidos e os envia ao servidor para validação, retornando com o resultado e executando ações.

- **Edits.js**: Responsável pela edição de itens de uma tabela. Captura o ID/chave de verificação e traz os dados referentes ao cadastro. Realiza importações de módulos extras.

- **Dashboard.js**: Gerencia interações no dashboard do sistema. Realiza solicitações ao servidor e exibe resultados.

- **modulosexts.js**: Utilizado na página de módulos extras. Realiza uma requisição ao servidor para exibir módulos instalados e disponíveis para uso, incorporando o conteúdo quando selecionado.

### Pasta `Acionadores`:

- **crud/**: Módulos JavaScript responsáveis por operações de CRUD (create, read, update, delete) que serão reutilizados em todo o sistema.

- **efeitos/**: Módulos JavaScript responsáveis por efeitos visuais, como loading e transições.

- **templates/**: Módulos para mudanças no layout do sistema.

- **validacoes/**: Módulos para tratamento e validação de dados.

- **includes/**: Módulos específicos para cada página, utilizados em conjunto com arquivos PHP.

### Pasta `externos`:

- Contém plugins e bibliotecas externas, como Bootstrap, jQuery, Chart.js, entre outros.

Essa estrutura permite a modularização e reutilização de funcionalidades em todo o sistema, melhorando a manutenção e escalabilidade.



## Relação entre Arquivos JavaScript


### Pages.js:
- Responsável por funcionalidades relacionadas à manipulação de páginas, como exibição de tabelas, paginação, buscas, filtros, exclusões e inclusões.
- Realiza solicitações ao servidor e exibe os resultados.
- Deve ser incluído manualmente nas páginas que requerem suas funcionalidades.

### Principal.js:
- Fornece funções essenciais para todo o sistema.
- Presente em todas as páginas do sistema.
- Importa módulos extras, como a chamada do menu lateral.

### Login.js:
- Especificamente utilizado na página de login.
- Captura dados inseridos pelo usuário e os envia ao servidor para validação.
- Executa ações com base no resultado da validação.

### Edits.js:
- Utilizado quando um usuário clica em um item de uma tabela para edição.
- Captura a identificação/chave do item selecionado e carrega os dados para edição.

### Dashboard.js:
- Responsável por interações na página do dashboard.
- Realiza solicitações ao servidor e exibe os resultados.

### modulosexts.js:
- Utilizado na página de módulos extras para listar e incorporar módulos disponíveis.

### Acionadores/**:
- Contém diferentes módulos JavaScript que fornecem funcionalidades específicas.
- Dividido em subpastas como `crud`, `efeitos`, `templates`, `validacoes` e `includes`.
- Esses módulos são reutilizados em todo o sistema, proporcionando modularidade e facilitando a manutenção.

### externos/**:
- Contém plugins e bibliotecas externas utilizadas no sistema, como Bootstrap, jQuery, Chart.js, entre outros.

Essa relação mostra como os diferentes arquivos JavaScript do sistema se relacionam e as responsabilidades de cada um na aplicação.


## Integração JavaScript e PHP:

- Os arquivos JavaScript se comunicam com os arquivos PHP por meio de chamadas AJAX, enviando dados e recebendo respostas para atualizar dinamicamente a interface do usuário sem recarregar a página.

- Os arquivos PHP processam as solicitações recebidas dos arquivos JavaScript, realizam operações no banco de dados/API, se necessário, e retornam os resultados para os arquivos JavaScript.

Essa integração entre os arquivos PHP e JavaScript permite uma aplicação web dinâmica e responsiva, fornecendo uma experiência de usuário agradável.
