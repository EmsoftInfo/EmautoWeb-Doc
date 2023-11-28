![EMAUTO Web](https://www.emsoft.inf.br/wp-content/uploads/2018/08/logo_horizontal_160x40.png)
# Documentação EMAutoWeb


## Configuração do Ambiente

Este guia fornece instruções para configurar o ambiente necessário para executar o sistema web em sua máquina. Certifique-se de seguir os passos abaixo para garantir que todas as dependências estejam devidamente instaladas.

### Pré-Requisitos

Antes de iniciar a configuração, verifique se sua máquina atende aos seguintes pré-requisitos:

- Apache (Web Server) instalado.
- PHP 8.2 instalado.
- Navegador da web com suporte ao ECMAScript 6.

### Instalação do Apache

Certifique-se de que o Apache esteja instalado e configurado em sua máquina. Você pode fazer o download do Apache no [site oficial do Apache](https://httpd.apache.org/download.cgi). Certifique-se de configurar o Apache para servir os arquivos do seu sistema web.

### Instalação do PHP 8.2

Certifique-se de que o PHP 8.2 esteja instalado e configurado em sua máquina. Você pode fazer o download do PHP 8.2 em [php.net](https://www.php.net/downloads.php). Verifique se o PHP está corretamente configurado no Apache para executar scripts PHP.

### Navegador com Suporte ao ECMAScript 6

Certifique-se de que você esteja usando um navegador da web atualizado que ofereça suporte ao ECMAScript 6 (ES6), uma versão avançada do JavaScript. A maioria dos navegadores modernos, como Google Chrome, Mozilla Firefox, Microsoft Edge e outros, oferece suporte ao ECMAScript 6.

### Alternativas a instação manual do PHP e Apache

1. Laragon
2. XAMPP
3. WAMPP
4. EasyPHP

Qualquer um dos programas acima são suficientes para a utilização do PHP e Apache, os quais são configurados automaticamente. No entanto, o arquivo de configuração PHP.ini pode estar configurado para desenvolvimento; portanto, é necessário substituir este arquivo pela versão de produção enviada juntamente com o sistema para instalação.

Além disso, para o funcionamento do sistema, são necessárias as configurações do PHP para rodar com os seguintes módulos:

- CURL
- OpenSSL

Esses módulos devem estar instalados; caso contrário, a aplicação não funcionará. Para realizar a instalação, acesse a página oficial php.net


### Verificação da Configuração

Para verificar se o ambiente foi configurado corretamente, siga os passos a seguir:

1. Inicie o Apache.
2. Coloque os arquivos do sistema web em um diretório acessível pelo Apache.
3. Abra seu navegador da web e acesse o sistema web.

Se o sistema web for carregado com sucesso e funcionar corretamente no seu navegador, significa que a configuração do ambiente foi realizada com êxito.

Lembre-se de que é fundamental seguir as melhores práticas de segurança, como configurar senhas seguras para o Apache e o PHP, e aplicar as atualizações de segurança necessárias em seu sistema web.

Com o ambiente configurado, você estará pronto para executar e testar seu sistema web em sua máquina local.



## Configuração do Sistema para Clientes

Para configurar o sistema para cada cliente, siga os passos a seguir:

1. Acesse a pasta `system` do projeto.

2. Navegue até `system/app/config` e abra o arquivo `config.php`.

3. Dentro do arquivo `config.php`, localize a seção de configuração do IP do cliente.

4. Altere o IP do cliente conforme necessário.

5. Salve o arquivo `config.php`.

6. Reinicie o sistema para aplicar as novas configurações.

7. Após a reinicialização, faça o primeiro acesso ao sistema.

8. Use um usuário master ou administrador para configurar os usuários e níveis de acesso de acordo com as necessidades do cliente.

Isso garantirá que o sistema esteja configurado corretamente e personalizado para atender às especificações de cada cliente.



