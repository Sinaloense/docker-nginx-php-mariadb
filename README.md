# docker-nginx-php-mariadb

## Requerimientos:
- WSL: https://learn.microsoft.com/en-us/windows/wsl/install
- Docker: https://docs.docker.com/get-docker
- VSCode (Opcional): https://code.visualstudio.com/
- VSCode Docker (Opcional): https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-docker
- PHPMyAdmin (Opcional): https://www.phpmyadmin.net/downloads

## PHPMyAdmin
Se puede descargar PHPMyAdmin y colocarlo en ./www/html/pma/

### Copiar config.sample.inc.php con el nombre de config.inc.php y usar la siguiente configuración
```
/* Authentication type */
$cfg['Servers'][$i]['auth_type'] = 'cookie';
/* Server parameters */
$cfg['Servers'][$i]['host'] = 'mariadb'; // Nombre del servicio colocado en docker-compose.yml
$cfg['Servers'][$i]['compress'] = false;
$cfg['Servers'][$i]['AllowNoPassword'] = true;
```