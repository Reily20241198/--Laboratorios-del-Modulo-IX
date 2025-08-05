# --Laboratorios-del-Modulo-IX
Practica 3: Instalación de Ansible (1pts)
# Comandos y su significado - Práctica Ansible y Terraform

1. sudo dnf install -y epel-release
   - Instala el repositorio EPEL en CentOS para poder acceder a paquetes adicionales como Ansible.

2. sudo dnf install -y ansible
   - Instala Ansible y todas sus dependencias en la máquina controladora.

3. ssh-keygen -t rsa -b 4096 -f ~/.ssh/id_rsa_ansible
   - Genera un par de llaves SSH RSA para usar con el usuario ansible (sin contraseña para acceso automático).

4. ssh-copy-id -i ~/.ssh/id_rsa_ansible.pub ansible@IP_REMOTA
   - Copia la llave pública SSH al host remoto para permitir acceso SSH sin contraseña.

5. net user ansible "P@ssw0rd123" /add
   - Crea un usuario llamado ansible en Windows con la contraseña P@ssw0rd123.

6. net localgroup Administradores ansible /add
   - Agrega el usuario ansible al grupo de administradores locales en Windows (permiso de administrador).

7. Set-Item -Path WSMan:\localhost\Service\Auth\Basic -Value $true
   - Habilita la autenticación básica en WinRM (Windows Remote Management).

8. Set-Item -Path WSMan:\localhost\Service\AllowUnencrypted -Value $true
   - Permite comunicación sin cifrado en WinRM (necesario para Ansible en entornos de prueba).

9. winrm quickconfig
   - Configura el servicio WinRM para habilitar la administración remota en Windows.

10. ansible -m ping grupo_o_host
    - Usa el módulo ping de Ansible para probar conectividad y autenticación con los hosts definidos en inventario.

11. ansible win -m win_ping
    - Módulo Ansible específico para probar conexión con hosts Windows vía WinRM.

12. terraform init
    - Inicializa el entorno de trabajo de Terraform, descarga plugins y prepara la configuración.

13. terraform plan
    - Muestra un plan de acciones que Terraform realizará para ajustar la infraestructura.

14. terraform apply
    - Aplica la configuración de Terraform y crea/modifica recursos en la nube.

15. ssh-copy-id -f -i ~/.ssh/id_rsa_ansible.pub ansible@IP_REMOTA
    - Forzar copia de llave pública SSH, útil si ya está copiada pero quieres actualizar.

