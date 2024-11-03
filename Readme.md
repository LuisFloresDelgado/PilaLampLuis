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
![Captura de pantalla 2024-11-03 141829](https://github.com/user-attachments/assets/4869516d-8bcd-4f60-8193-e873cf6d0413)

También tendremos que tener los scripts de aprovisionamiento.

- Script de máquina apache
![Captura de pantalla 2024-11-03 142000](https://github.com/user-attachments/assets/954dbd18-2dda-4555-b12c-84cc754d69ba)

- Script de Mysql

![Captura de pantalla 2024-11-03 142028](https://github.com/user-attachments/assets/f1ffbd66-6a37-4d40-b2b6-81b6448cba91)

Realizamos un `vagrant up` y un `vagrant provision` para cargar las máquinas y los scripts de aprovisionamiento.

## Máquina Apache

1. **Comprobamos que Apache está activo**.
![Captura de pantalla 2024-11-03 142040](https://github.com/user-attachments/assets/956a8883-bfca-462a-82e6-f27c38d9c62f)

3. **Clonamos el repositorio de GitHub**:
![Captura de pantalla 2024-11-03 142055](https://github.com/user-attachments/assets/ab18e5a6-ab8e-4ec4-8997-2af066dd5655)
5. **Creamos directorio para mover los archivos**.
![Captura de pantalla 2024-11-03 142109](https://github.com/user-attachments/assets/a2992e68-690d-425f-8372-e6f8cd091bb4)
![Captura de pantalla 2024-11-03 142123](https://github.com/user-attachments/assets/5b7331c0-f664-4b0f-8a2c-95ce91b75823)

7. **En `sites-available`, copiamos el `000-conf` a uno nuevo para editarlo más fácilmente**.
![Captura de pantalla 2024-11-03 142140](https://github.com/user-attachments/assets/a5a39c53-af89-4e8e-be65-eca296892610)

9. **Editamos y ponemos la carpeta que hemos creado anteriormente**.
10. **Ahora la habilitamos y deshabilitamos el otro**.
![Captura de pantalla 2024-11-03 142201](https://github.com/user-attachments/assets/9bc29649-ddb9-43fa-ae4b-85a852879f5f)

12. **Editamos el `config.php` y ponemos la IP de la máquina**.
![image](https://github.com/user-attachments/assets/07212b97-4be9-4516-91ed-745016f7e5f9)

## Máquina Mysql

1. **Nos metemos en `/etc/mysql/mariadb.conf.d` y editamos el archivo `50-server.cnf` dejándolo así (con la IP de la máquina de Apache)**.
![Captura de pantalla 2024-11-03 142243](https://github.com/user-attachments/assets/a783040c-d169-4a09-bdc5-dce7eee3dfb4)

3. **Creamos un usuario con todos los privilegios**:
![Captura de pantalla 2024-11-02 171424](https://github.com/user-attachments/assets/b38ba8e4-1b83-4248-a5e3-13f8bfb3a5db)

4. **Clonamos los archivos del repositorio de GitHub**.
![Captura de pantalla 2024-11-02 172115](https://github.com/user-attachments/assets/1084d47b-d008-43c4-81d5-b7febc76e561)

5. **Cargamos la base de datos**.
![Captura de pantalla 2024-11-02 172414](https://github.com/user-attachments/assets/6b0559be-1fa1-427f-91de-2c3ded4c9298)

## Comprobación

En la máquina Apache, verificamos que todo está funcionando correctamente.
![Captura de pantalla 2024-11-03 135219](https://github.com/user-attachments/assets/64b3bda3-544e-47a2-b1d6-a797dfe27c51)

También nos metemos en google y ponesmos la siguiente ip y nos saldra la La Lamp web
![image](https://github.com/user-attachments/assets/95fe119e-a685-4c5a-b227-d38c5b42222e)


