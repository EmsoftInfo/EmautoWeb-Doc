![EMAUTO Web](https://www.emsoft.inf.br/wp-content/uploads/2018/08/logo_horizontal_160x40.png)
# Documentação EMAutoWeb
## Estrutura do Sistema Web

Este documento descreve a estrutura básica do sistema web.

### Arquivos e Diretórios

O sistema web possui a seguinte estrutura de arquivos e diretórios:

- **index.php**: Este arquivo está localizado no diretório principal do sistema e é responsável por todas as funcionalidades da aplicação. Ele monta e inclui as páginas dinamicamente.

- **system/**: Este diretório contém os arquivos e recursos internos do sistema.
  - **app/**: Este diretório contém os arquivos específicos da aplicação.
    - **classes/**: Contém todas as classes que serão utilizadas em todo o sistema.
    - **config/**: Contém arquivos de configuração do sistema, constantes e funções globais.
    - **controles/**: Contém arquivos PHP responsáveis por receber as solicitações do JavaScript e instanciar classes.
    - **includes/**: Contém arquivos com conteúdos que serão utilizados em todo o sistema.
      - **AcoesPages/**: Arquivos PHP com conteúdos chamados ao longo do sistema e em outras subpastas.
      - **FiltrosPages/**
      - **FormPages/**
      - **ModelosExtras/**
      - **ModulosExtras/**
      - **TabelasPages/**
    - **temp/**: Contém arquivos temporários gerados durante o uso do sistema.
    
- **public/**: Este diretório contém os arquivos acessíveis ao público.
  - **CSS/**: Contém arquivos de estilização do sistema.
  - **midia/**: Contém arquivos de mídia usados em todo o sistema, como logos e ícones.
  - **pages/**: Contém o layout das páginas que serão montadas e incluídas no index.php.
  - **template/**: Contém o topo, o menu lateral e o menu mobile.
  - **JS/**: Contém arquivos JavaScript.
    - **Acionadores/**: Contém módulos export function JavaScript que podem ser usados em todo o sistema.
    - **externos/**: Contém plugins e bibliotecas externas.

### Estrutura de Diretórios

sistema-web/
│
├── index.php
│
├── system/
│ ├── app/
│ │ ├── classes/
│ │ ├── config/
│ │ │ ├── funcoesGlobais.php
│ │ │ ├── config.php
│ │ │ └── palavras.php
│ │ ├── controles/
│ │ ├── includes/
│ │ │ ├── AcoesPages/
│ │ │ ├── FiltrosPages/
│ │ │ ├── FormPages/
│ │ │ ├── ModelosExtras/
│ │ │ ├── ModulosExtras/
│ │ │ └── TabelasPages/
│ │ └── temp/
│ │
│ └── public/
│ ├── CSS/
│ ├── midia/
│ ├── pages/
│ ├── template/
│ └── JS/
│ ├── Acionadores/
│ └── externos/




## Resumo do Padrão de Projeto e Arquitetura


### Padrão de Projeto Utilizado: Arquitetura de Aplicação Web

### Arquitetura:
- O sistema utiliza uma arquitetura de aplicação web tradicional.
- Divisão clara de responsabilidades entre o cliente (navegador) e o servidor.
- Utiliza linguagem de programação do lado do servidor, como PHP.
- A comunicação entre o cliente e o servidor é realizada através do protocolo HTTP.

### Componentes ou Comportamentos:
- O sistema é baseado em componentes, com diferentes partes responsáveis por funcionalidades específicas.
- Os componentes incluem classes, controles, configurações, páginas, estilos e scripts.

### Vantagens:
- Separação clara de responsabilidades entre cliente e servidor.
- Reutilização de código através de componentes modulares.
- Facilidade de manutenção e escalabilidade.
- Potencial para implementação de testes automatizados para garantir a qualidade do software.

