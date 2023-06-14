# Ejercicio CiberKillChain - Ataque

## Alumno

Jonathan Cagua O.

## Trabajo práctico

El sistema está compuesto por un módulo IoT diseñado para medir la humedad, temperatura y calidad del aire en un ambiente cerrado. Los datos capturados por este módulo se envían a través de un protocolo propietario, donde son recibidos, almacenados y visualizados en la plataforma.

Además, el equipo ofrece opciones de configuración y lectura a través de BLE (Bluetooth Low Energy), lo que permite una comunicación segura con los servicios correspondientes. También se incluyen alertas personalizadas que se ajustan a cada cliente.


## Objetivo del Ataque

El objetivo final del ataque es la manipulación de datos, para dejar fuera de linea a los dispositivos.

1. Reconnaisssance

    - [[T1592] Gather Victim Host Information ](https://attack.mitre.org/techniques/T1592/)
        Obtener informacion sobre el dispositivo y ver repositorios sobre el dispositivo, si es  hardware abierto para ver puertos disponibles.

    - [[T1046] Network Service Scanning ](https://attack.mitre.org/techniques/T1046/)
        Utilizar herramientas de escaneo de BLE, como "hcitool" para identificar dispositivos BLE cercanos y recopilar información sobre ellos y servicios disponibles.
    - Analizar los mensajes de anuncio (advertisement) enviados por dispositivos BLE para obtener información sobre los     nombres de los dispositivos y los servicios que ofrecen.

    - Examinar los perfiles de servicios BLE disponibles públicamente para identificar vulnerabilidades conocidas

2. Weaponization 

    - Desarrollaria malware específico para dispositivos BLE que aproveche vulnerabilidades conocidas, como un malware diseñado para explotar la vulnerabilidad BlueBorne que afecta a dispositivos BLE y Wi-Fi.
    - Crear herramientas de inyección de paquetes personalizadas que permitan la manipulación de las comunicaciones BLE, como enviar paquetes maliciosos para forzar una desconexión o enviar comandos de control falsos.

3. Delivery

    - Enviar paquetes maliciosos a través de una conexión BLE establecida para explotar vulnerabilidades específicas de un dispositivo BLE y entregar el malware.
    - Aprovechar vulnerabilidades en la configuración o en el emparejamiento de dispositivos BLE para establecer una conexión maliciosa y entregar el malware.


4. Exploitation

    - Inyectar malware en la memoria de un dispositivo BLE comprometido, aprovechando vulnerabilidades de desbordamiento de búfer o inyección de comandos para lograr la persistencia en el dispositivo.
    - Explotar una vulnerabilidad en la actualización o en el proceso de carga de firmware del dispositivo BLE para instalar un firmware modificado o malicioso.
        
5. Installation
    - Inyectar malware en la memoria de un dispositivo BLE comprometido: Esto se puede lograr aprovechando vulnerabilidades de desbordamiento de búfer o inyección de comandos en el firmware o en la aplicación del dispositivo BLE. Al explotar estas vulnerabilidades, se puede inyectar código malicioso en la memoria del dispositivo.
    - Explotar una vulnerabilidad en la actualización o en el proceso de carga de firmware del dispositivo BLE: Al encontrar y aprovechar una vulnerabilidad en el proceso de actualización o carga de firmware del dispositivo BLE, se puede reemplazar o modificar el firmware del dispositivo con una versión modificada o maliciosa. Esto puede permitir el control completo del dispositivo y la ejecución de acciones maliciosas.

6. Command & Control 

    - Establecer una conexión encubierta a través de canales BLE para enviar comandos y recibir información de los dispositivos comprometidos, utilizando técnicas de ocultación y cifrado para evadir la detección.


7. Actions on Objectives

    - Robo de datos: Se puede datos sensibles almacenados en el dispositivo BLE, como información personal, credenciales de acceso o datos confidenciales.
    - Manipulación de comunicaciones: se puede manipular las comunicaciones BLE entre el dispositivo comprometido y otros dispositivos conectados, lo que puede permitir realizar ataques de intermediario o modificar los datos transmitidos.
    - Control remoto: se puede ejercer control remoto sobre el dispositivo BLE comprometido, lo que puede implicar la ejecución de comandos arbitrarios, la activación de funciones no autorizadas o el uso del dispositivo comprometido como punto de acceso para realizar ataques adicionales a otros dispositivos.
