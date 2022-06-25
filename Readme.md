En el siguiente ejemplo se realizará una conexión a un servidor Linux por ssh y se podrá ver en tiempo real el resultado de ejecutar el comando **uname -a** que muestra la versión del sistema operativo.

Para realizar la conexión **ssh** se necesitará el nombre del host, el usuario con acceso a ese servidor y la contraseña. Posteriormente se podrá reemplazar el primer argumento del método exec_command por el comando Linux que se necesite ejecutar en el servidor. Por ejemplo, si fuera una distribución basada en **Redhat** se podría escribir **yum -y update** para actualizarla, **yum -y install vim** para instalar el editor Vim, **cat /etc/fstab**, etc.

Para teclear la contraseña, es interesante importar **getpass** que posibilitará hacer un input de la misma, pero sin salida por la consola para que nadie vea lo escrito. Para conseguir esto se usa getpass.getpass().