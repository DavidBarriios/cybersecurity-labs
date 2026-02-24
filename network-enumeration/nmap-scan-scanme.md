<img width="652" height="408" alt="image" src="https://github.com/user-attachments/assets/fa1bc42d-b1a9-48e5-907c-4abca3749af3" />Enumeración Inicial de Servicios con Nmap

Objetivo
Identificar puertos TCP abiertos y versiones de servicios en un objetivo autorizado para práctica de ciberseguridad.

Objetivo analizado:
scanme.nmap.org


Herramienta utilizada
Nmap (Network Mapper)

Versión:
7.98

Sistema:
Kali Linux

Comando ejecutado

nmap -sV scanme.nmap.org



Resumen de resultados


El host se encuentra activo con una latencia aproximada de 3.3 segundos.

Puertos abiertos detectados:

- 22/tcp → SSH (OpenSSH 6.6.1p1 Ubuntu)
- 80/tcp → HTTP (Apache 2.4.7 Ubuntu)
- 9929/tcp → Nping echo
- 31337/tcp → tcpwrapped

Puertos filtrados:

- 25/tcp (SMTP)
- 514/tcp

La mayoría de los demás puertos se encuentran cerrados.


Análisis técnico

• El puerto 22 indica acceso remoto mediante SSH.  
• El puerto 80 confirma la presencia de un servidor web Apache.  
• Los puertos filtrados sugieren la existencia de reglas de firewall.  
• El parámetro -sV permitió identificar versiones específicas de los servicios.

Las versiones detectadas (OpenSSH 6.6.1p1 y Apache 2.4.7) no son actuales, por lo que podrían investigarse en bases de datos de vulnerabilidades (CVE) para determinar posibles riesgos.


Conclusion

La enumeración es la primera fase crítica en un proceso de pruebas de penetración.  
La detección de versiones permite identificar posibles vectores de ataque.  
Los puertos filtrados indican que existen mecanismos de control de acceso implementados.

Este ejercicio demuestra la importancia de la fase de reconocimiento y recopilación de información en ciberseguridad.

