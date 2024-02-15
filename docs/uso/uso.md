![EMAUTO Web](https://www.emsoft.inf.br/wp-content/uploads/2018/08/logo_horizontal_160x40.png)
# Documentação EMAutoWeb
## Instruções para Primeiro Acesso e Solução de Problemas de Login

Após realizar as configurações de ambiente e alteração do IP do cliente, é necessário realizar o primeiro acesso como usuário master para iniciar as próximas configurações.

Se encontrar dificuldades para realizar o login, pode haver vários fatores impedindo o acesso. Siga os seguintes passos em ordem, e se um dos passos resolver o problema, não será necessário continuar com os próximos:

1. Verifique se o usuário e a senha estão corretos no banco de dados.
2. Acesse a pasta `system/app` e modifique as permissões da pasta `temp`, permitindo que todos os usuários possam criar e excluir arquivos.
3. Limpe os cookies do sistema e reinicie o Apache.
4. Verifique se o cache do navegador está desativado. Caso contrário, ative-o.
5. Verifique se todas as extensões necessárias do sistema foram instaladas. Caso contrário, realize a instalação.

Se nenhuma das alternativas acima funcionar, verifique possíveis erros através do acesso à pasta `temp/erros_logs/`.
