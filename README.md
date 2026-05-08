# Laboratorio de Teletransportación Digital (SSH y RDP)

Este proyecto documenta la configuración de servicios de acceso remoto (SSH y RDP) utilizando contenedores Docker, realizado como parte del módulo profesional de Desarrollo de Aplicaciones.

Información del Estudiante

Nombre: Joaquin Madrid del Toro   
Institución: Campus Cámara Comercio Sevilla   
Trimestre: 3°

Configuración del Entorno

1. Preparación de Docker
Para iniciar el laboratorio, se realizaron los siguientes pasos iniciales:
Se creó un directorio de trabajo denominado SI_Bitacora4_JoaquinMadridDelToro.  
Se definió un archivo docker-compose.yml con la estructura necesaria para desplegar los servidores de SSH y RDP.  
Se ejecutaron los siguientes comandos para levantar los servicios y verificar su estado
Comando: docker-compose up -d
docker ps
<img width="1398" height="703" alt="image" src="https://github.com/user-attachments/assets/8ca907d3-4438-4882-80b8-3e446cb9f317" />

<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/5636b840-a9f8-4abf-8422-e0bd2612badf" />


3. Acceso Inicial
Se estableció la primera conexión al servidor SSH mediante el puerto mapeado 2222:  
Comando: ssh alumno@127.0.0.1 -p 2222.  
Se aceptó la autenticidad del host y se ingresó la contraseña del usuario alumno
<img width="758" height="168" alt="image" src="https://github.com/user-attachments/assets/74e43095-cc9c-428b-96f8-191be2efb128" />


5. Generación de Claves (SSH Keygen)Para mejorar la seguridad y facilitar el acceso, se generó un par de claves criptográficas:

Comando: ssh-keygen -t ed25519 -C "joaquinmadrid.25@campuscamara.es".  

La clave pública fue almacenada en /config/.ssh/id_ed25519.pub.  
<img width="746" height="267" alt="image" src="https://github.com/user-attachments/assets/7928f913-0c09-4f37-9150-22e7724c240f" />


4. Transferencia de Clave PúblicaSe copió la clave al servidor para permitir el inicio de sesión sin contraseña en el futuro:  Comando: ssh-copy-id -p 2222 alumno@127.0.0.1.
Se confirmó la instalación exitosa de 1 clave en el servidor.

Configuración de Escritorio Remoto (RDP)
<img width="610" height="248" alt="image" src="https://github.com/user-attachments/assets/f092be24-738d-4e3d-8562-57298ab8e681" />


5. Conexión RDPFinalmente, se procedió a probar el acceso gráfico mediante la herramienta Conexión a Escritorio Remoto de Windows:

Equipo/Puerto: 127.0.0.1:3389 (especificado como puerto 3389 en la configuración).  
El sistema queda preparado para solicitar credenciales al momento de la conexión.
<img width="407" height="242" alt="image" src="https://github.com/user-attachments/assets/2ba3fa4f-af84-4614-8c48-d50b436a9b28" />


