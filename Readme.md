# IAW
## ASIR 2
### Práctica 1

## Índice

1. [Archivo VagrantFile](#archivo-vagrantfile)
2. [Máquina Apache](#máquina-apache)
3. [Máquina Mysql](#máquina-mysql)
4. [Comprobación](#comprobación)

## Archivo VagrantFile

Configuramos el Vagrantfile de la siguiente manera para tener las dos máquinas, una apache y otra con mysql.

También tendremos que tener los scripts de aprovisionamiento.

- Script de máquina apache
- Script de Mysql

Realizamos un `vagrant up` y un `vagrant provision` para cargar las máquinas y los scripts de aprovisionamiento.

## Máquina Apache

1. **Comprobamos que Apache está activo**.
2. **Clonamos el repositorio de GitHub**:
    ```bash
    sudo git clone https://github.com/josejuansanchez/iaw-practica-lamp.git
    ```
3. **Creamos directorio para mover los archivos**.
4. **En `sites-available`, copiamos el `000-conf` a uno nuevo para editarlo más fácilmente**.
5. **Editamos y ponemos la carpeta que hemos creado anteriormente**.
6. **Ahora la habilitamos y deshabilitamos el otro**.
7. **Editamos el `config.php` y ponemos la IP de la máquina**.

## Máquina Mysql

1. **Nos metemos en `/etc/mysql/mariadb.conf.d` y editamos el archivo `50-server.cnf` dejándolo así (con la IP de la máquina de Apache)**.
2. **Creamos un usuario con todos los privilegios**:
3. ![Captura de pantalla 2024-11-02 171424](https://github.com/user-attachments/assets/b38ba8e4-1b83-4248-a5e3-13f8bfb3a5db)

    ```sql
    grant all privileges on lamp_db.* to 'luis'@'192.168.4.10';
    ```
4. **Clonamos los archivos del repositorio de GitHub**.
5. **Cargamos la base de datos**.

## Comprobación

En la máquina Apache, verificamos que todo está funcionando correctamente.
También nos metemos en google y ponesmos la siguiente ip y nos saldra la La Lamp web
![image](https://github.com/user-attachments/assets/95fe119e-a685-4c5a-b227-d38c5b42222e)


