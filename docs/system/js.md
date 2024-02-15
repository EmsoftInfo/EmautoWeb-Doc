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

- **crud/**: Contém arquivos JavaScript responsáveis por operações de CRUD (create, read, update, delete) que serão reutilizados em todo o sistema.

- **efeitos/**: Módulos JavaScript responsáveis por efeitos visuais, como loading e transições.

- **templates/**: Módulos para mudanças no layout do sistema.

- **validacoes/**: Módulos para tratamento e validação de dados.

- **includes/**: Módulos específicos para cada página, utilizados em conjunto com arquivos PHP.

### Pasta `externos`:

- Contém plugins e bibliotecas externas, como Bootstrap, jQuery, Chart.js, entre outros.

Essa estrutura permite a modularização e reutilização de funcionalidades em todo o sistema, melhorando a manutenção e escalabilidade.
