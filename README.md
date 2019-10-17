# Introdução ao Drupal 8
Nesse arquivo temos algumas configurações necessárias antes de começar o treinamento.
Faremos tudo isso no dia, mas fique a vontade caso queira configurar por conta.  

## Ambiente de desenvolvimento:
Primeiro devemos instalar os seguintes programas:

* [Visual Studio 2012 VC 11 x64][vcredist]
* [WampServer 3 x64][wampserver3]
* [Composer][composer]

## Configuring environment:

Adicione os caminhos PHP e MySQL nas variáveis de ambiente:

![Environment variables](https://i.imgur.com/zPKJvNm.png)

Após adicionar os caminhos nas variáveis de ambiente, abra o terminal e verifique a versão do PHP:

![PHP](https://i.imgur.com/Rvq81Y1.png)

Verifique também se consegue entrar no MySQL (por padrão a senha é vazia):

![MySQL](https://i.imgur.com/Edj9M60.png)

Verificar se o módulo/extensão estão habilitados:

* modrewrite (Apache)
* OPcache (PHP)

## Addons

Exemplo de configuração do VirtualHost:
```
<VirtualHost *:80>
  ServerName drupal.local
  ServerAlias drupal.local
  DocumentRoot "${INSTALL_DIR}/www/drupal"
  <Directory "${INSTALL_DIR}/www/drupal">
    Options +Indexes +Includes +FollowSymLinks +MultiViews
    AllowOverride All
    Require local
  </Directory>
</VirtualHost>
```

Lembre-se de colocar isso no arquivo _hosts_ localizado em "_C:/Windows/system32/drivers/etc/hosts_": 
```
# Drupal
127.0.0.1 drupal.local
```

[vcredist]: <http://www.microsoft.com/en-us/download/details.aspx?id=30679>
[wampserver3]: <https://sourceforge.net/projects/wampserver/files/WampServer%203/WampServer%203.0.0/wampserver3.1.9_x64.exe/download>
[composer]: <https://getcomposer.org/Composer-Setup.exe>
