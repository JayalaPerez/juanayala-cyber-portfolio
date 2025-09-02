\# Write-up: Máquina RELÁMPAGO (CyberConquer)



\## 📌 Información general

\- \*\*Plataforma:\*\* CyberConquer

\- \*\*Nombre de la máquina:\*\* RELÁMPAGO

\- \*\*Dificultad:\*\* Media

\- \*\*Fecha del laboratorio:\*\* Septiembre 2025

\- \*\*Objetivo:\*\* Captura de flags y explotación de vulnerabilidades



---



\## 🔍 Reconocimiento

```bash

nmap -sC -sV -A -T4 172.17.0.2



Hallazgos:



Puerto 80 abierto → servidor web con base de datos expuesta.



Puerto 22 → ssh.



⚔️ Explotación



Enumeración de rutas con gobuster:



gobuster dir -u http://172.17.0.2 -w /usr/share/wordlists/dirb/common.txt



Descubrimiento de /database/users.



Extracción de credenciales → acceso al panel admin.

