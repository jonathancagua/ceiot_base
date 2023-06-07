# Ejercicio CiberKillChain - Ataque

## Alumno

Jonathan Cagua O.

## Trabajo práctico

El sistema está compuesto por un módulo IoT diseñado para medir la humedad, temperatura y calidad del aire en un ambiente cerrado. Los datos capturados por este módulo se envían a través de un protocolo propietario, donde son recibidos, almacenados y visualizados en la plataforma.

Además, el equipo ofrece opciones de configuración y lectura a través de BLE (Bluetooth Low Energy), lo que permite una comunicación segura con los servicios correspondientes. También se incluyen alertas personalizadas que se ajustan a cada cliente.


## Objetivo del Ataque

El objetivo final del ataque es la manipulación de datos, con el fin de alterar la información del firmware o visualizar las opciones de configuración que se envían desde el servidor o hacia el servidor, con el propósito de enviar información incorrecta.


1. Reconnaisssance

    - [[T1592] Gather Victim Host Information ](https://attack.mitre.org/techniques/T1592/)
        Obtener informacion sobre el dispositivo y ver repositorios sobre el dispositivo, revisar la mac y ver informacion tecnica en el internet.

    - [[T1046] Network Service Scanning ](https://attack.mitre.org/techniques/T1046/)
        Obtener sobre los servicios y dispositivos BLE disponibles, identificando los perfiles y características admitidos por el dispositivo IoT.

2. Weaponization 

    - [[T1200] Hardware Additions](https://attack.mitre.org/techniques/T1200/)

        Hardware Additions (T1200): Agregar hardware adicional al dispositivo IoT para interceptar o manipular el tráfico BLE, como dispositivos de captura de paquetes.

3. Delivery

    - [[T1414] Deliver Malicious App via Authorized App Store](https://attack.mitre.org/techniques/T1414/)
        Distribuir una aplicación BLE maliciosa a través de una tienda de aplicaciones autorizada para que los usuarios la descarguen e instalen en sus dispositivos IoT.
    - [[T1203] Phishing for Hardware](https://attack.mitre.org/techniques/T1203/)    
        Engañar a los propietarios de dispositivos IoT para que descarguen e instalen aplicaciones maliciosas a través de técnicas de phishing, utilizando sitios web falsos o mensajes de correo electrónico fraudulentos.


4. Exploitation

    - [[T1588] Obtain Capabilities: Exploits ](https://attack.mitre.org/techniques/T1588/)
        Explorar vulnerabilidades entre la aplicacion movil y el modulo IOT para ver fallas de seguridad en el login y manipular su trafico. Se pueden usar herramientas y sniffer de trafico hasta encontrar un patron.
        


5. Installation
    - [[T1014] Rootkit ](https://attack.mitre.org/techniques/T1014/)
        Instalar un rootkit en el firmware del dispositivo IoT para obtener acceso y control persistente, lo que permitira interceptar el tráfico BLE.
    - [[T1601] Modify System Image ](https://attack.mitre.org/techniques/T1601/)
        Modificar la imagen del sistema del dispositivo IoT para incluir código malicioso que intercepte o manipule el tráfico BLE.
        Y buscar credenciales en Flash del dispositivo o certificados.

6. Command & Control 

    - [[T1040] Network Sniffing](https://attack.mitre.org/techniques/T1040/)
        Realizar un análisis pasivo de la red para capturar, analizar el tráfico BLE y extraer los datos.


7. Actions on Objectives

    - [[T1583] Acquire Infrastructure](https://attack.mitre.org/techniques/T1583/)
        Obtener la infraestructura necesaria, para recibir y almacenar los datos interceptados entre la aplicación BLE y el dispositivo IoT.
    - [[T1030] Data Transfer Size Limits ](https://attack.mitre.org/techniques/T1030/)
        Limitar el tamaño de los paquetes de datos transferidos entre la aplicación BLE y el dispositivo IoT para evitar la detección y el análisis.

