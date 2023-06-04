# Ejercicio CiberKillChain - Ataque

## Alumno

Jonathan Cagua O.

## Trabajo práctico

El sistema está compuesto por un módulo IoT diseñado para medir la humedad, temperatura y calidad del aire en un ambiente cerrado. Los datos capturados por este módulo se envían a través de un protocolo propietario, donde son recibidos, almacenados y visualizados en la plataforma.

Además, el equipo ofrece opciones de configuración y lectura a través de BLE (Bluetooth Low Energy), lo que permite una comunicación segura con los servicios correspondientes. También se incluyen alertas personalizadas que se ajustan a cada cliente.


## Objetivo del Ataque

El objetivo final del ataque es ataque de manipulacion de datos.


1. Reconnaisssance

    - [[T1590] Gather Victim Network Information](https://attack.mitre.org/techniques/T1590/)
        - [[.001] Domain Properties](https://attack.mitre.org/techniques/T1590/001): "Busqueda de información técnica" Esto puede incluir buscar en motores de búsqueda, consultar documentos técnicos disponibles públicamente, explorar sitios web relacionados con la organización, buscar en repositorios de código abierto y otros recursos en línea.

        - [[.003] Domain Properties](https://attack.mitre.org/techniques/T1590/003):"Exploración de dominios y subdominios": En esta sub-técnica, se enfoca en explorar los dominios y subdominios asociados con el objetivo. Utiliza herramientas de búsqueda y exploración de dominios para identificar posibles subdominios, recopilar información sobre servicios, servidores, direcciones IP, registros DNS y otros detalles técnicos relevantes.

2. Weaponization 

    - [[T1505] Custom Command and Control Protocol](https://attack.mitre.org/techniques/T1505/)

        Crear un programa o código malicioso diseñado específicamente para el sensor IoT, con el objetivo de realizar acciones no autorizadas como la manipulación de datos, el control remoto del dispositivo o la extracción de información sensible.

3. Delivery

    - [[T1195] Compromiso de la cadena de suministro](https://attack.mitre.org/techniques/T1195/)

        Identificar y aprovechar vulnerabilidades en la cadena de suministro del sensor IoT, como proveedores de hardware, firmware o software, para modificar componentes o software del dispositivo.
    - [[T1478] Inyección de malware en el firmware ](https://attack.mitre.org/techniques/T1478/)

        Inyección de malware en el firmware (T1478): Introducir código malicioso o malware en el firmware del sensor IoT, ya sea reemplazando firmware legítimo o aprovechando vulnerabilidades en el proceso de actualización del firmware.


4. Exploitation

    - [[T1435] Wireless Protocol Decryption](https://attack.mitre.org/techniques/T1435/)
    
        Intentar interceptar y descifrar las comunicaciones cifradas utilizadas por el sensor IoT en canales Wi-Fi y BLE para obtener acceso a los datos transmitidos.
    - [[T1600] Exploit Weakness in Cryptography](https://attack.mitre.org/techniques/T1600/)
        Identificar y aprovechar debilidades en la implementación del cifrado utilizado por el sensor IoT. Esto puede implicar explotar vulnerabilidades en algoritmos de cifrado, claves débiles o problemas en la generación o gestión de claves de cifrado.


5. Installation

    - [[T1574] Hijack Execution Flow](https://attack.mitre.org/techniques/T1574/)

        Manipulación del proceso de actualización del firmware o manipulacion de configuracion: Interceptar o modificar las actualizaciones de firmware inalámbricas para instalar firmware malicioso en el dispositivo o intersectar configuracion y alterarlas.

6. Command & Control 

    - [[T1572] Communication Through Removable Media](https://attack.mitre.org/techniques/T1572/)

        La técnica de uso de medios extraíbles implica utilizar dispositivos USB o tarjetas SD para establecer una comunicación encubierta con un sensor IoT y enviar comandos de control. Esto puede incluir el uso de programas maliciosos en los dispositivos que se comunican con el sensor a través de Wi-Fi o BLE, así como la implementación de un protocolo de comunicación personalizado que oculte la naturaleza maliciosa de las interacciones.

7. Actions on Objectives

    - [[T1565] Data Manipulation](https://attack.mitre.org/techniques/T1565/)

        La técnica de Manipulación de Datos se refiere a la alteración de los datos almacenados o transmitidos por un sensor IoT con el fin de lograr objetivos maliciosos. Para un sensor IoT, esto puede incluir la manipulación de datos en tiempo real, como cambiar los valores de humedad, temperatura o calidad del aire para mostrar información falsa. También implica la modificación de la configuración del sensor, como cambiar umbrales de alerta o desactivar medidas de seguridad. Además, se puede manipular la visualización de datos en la nube o en las aplicaciones asociadas al sensor, presentando información falsa o ocultando datos reales.

