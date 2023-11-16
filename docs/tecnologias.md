![EMAUTO Web](https://www.emsoft.inf.br/wp-content/uploads/2018/08/logo_horizontal_160x40.png)
# Documentação EMAutoWeb

## 1. Aplicação das tecnologias e linguagens utilizadas

Este documento técnico fornece uma visão geral do sistema desenvolvido, descrevendo as linguagens de programação, tecnologias e bibliotecas utilizadas. O sistema foi construído utilizando PHP e JavaScript como linguagens primárias, com HTML5 e CSS3 empregados para marcação de texto e estilização, respectivamente.

## 2. Linguagens de Programação e Papéis no Desenvolvimento
- **PHP (Backend):** Selecionado como a linguagem principal para o desenvolvimento do lado do servidor, o PHP desempenha um papel fundamental na lógica de negócios, manipulação de dados e interações com o banco de dados.
- **JavaScript (Frontend):** Utilizado como a linguagem principal para o desenvolvimento do lado do cliente, o JavaScript é responsável por criar interações dinâmicas e aprimorar a experiência do usuário final.

## 3. Frameworks e Bibliotecas Utilizadas
O sistema faz uso das seguintes frameworks e bibliotecas para facilitar o desenvolvimento e proporcionar funcionalidades específicas:

### 3.1. Bootstrap
- **Utilização:** Empregado para estilizar e organizar o conteúdo do sistema.
- **Localização dos arquivos:** Os arquivos estão localizados na pasta `system/public/js/externos` para os arquivos JavaScript e `system/public/css/externos` para os arquivos CSS.
- **Invocação:** Os arquivos são invocados no arquivo `index.php`, presente na pasta principal do sistema.

### 3.2. jQuery
- **Utilização:** Principal biblioteca de JavaScript utilizada para interações com o usuário.
- **Localização dos arquivos:** Todos os arquivos do jQuery estão presentes na pasta `JS`, localizada em `system/public/js`.

### 3.3. Plugin_tabelas jQuery
- **Utilização:** Utilizado para a ordenação automática de tabelas com base no clique nos títulos.
- **Localização do plugin:** Presente na pasta `system/public/js/externos`.
- **Invocação:** A invocação desse plugin está no arquivo `pags.php`, localizado em `system/public/pages/`.

### 3.4. Plugin Mask jQuery
- **Utilização:** Utilizado para criar máscaras de campos quando necessário.
- **Localização dos arquivos:** As importações são feitas de maneira específica para cada componente, dentro da pasta `system/public/js/includes`.
- **Invocação:** Caso um componente necessite utilizar máscaras, a invocação é feita dentro da pasta `includes` em JS, onde os arquivos específicos para cada componente estão presentes.

## 4. Considerações Finais
A utilização dessas linguagens, frameworks e bibliotecas foi essencial para desenvolver um sistema robusto, responsivo e interativo. A combinação do PHP no backend e do JavaScript no frontend, aliada às frameworks e bibliotecas mencionadas, resultou na criação de uma aplicação eficiente e amigável ao usuário final.
