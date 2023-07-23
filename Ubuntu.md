# Cards Ubuntu

## Atualizar aplicativos
```
$ sudo apt update
$ sudo apt upgrade
```

## XAMPP
- Instalação
```
// Após download do XAMPP do site: 
// https://www.apachefriends.org/pt_br/download.html

$ sudo ./xampp-linux-x64-8.2.4.0-installer.run
```
- Local de instalação
```
/opt/lampp
```

- Executar XAMPP no terminal
```
$ sudo /opt/lampp/manager-linux-x64.run
```

## Alterar htdocs
- Alterar o caminho do DocumentRoot no arquivo arquivo httpd.conf para:
```
DocumentRoot "/home/{user-name}/htdocs"
<Directory "/home/{user_name}/htdocs">
```
- Alterar as seguintes linhas arquivo arquivo httpd.conf para:
```
<IfModule unixd_module>
   User {user_name}
   Group nogroup
</IfModule>
```
- Reiniciar o XAMPP