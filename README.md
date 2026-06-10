
<h1 align='center'>Ransom0</h1>

<p align="center">
 <img src='https://www.codefactor.io/repository/github/hugolb0/ransom0/badge'>
 <img src='https://api.travis-ci.com/hugolb0/ransom0.svg?branch=master'>
 <img src='https://img.shields.io/badge/Windows%2C%20Mac%20%26%20Linux-compatible-brightgreen'>
 <img src='https://img.shields.io/github/release-date/HugoLB0/Ransom0'>
 <img src='https://img.shields.io/github/commit-activity/m/HugoLB0/Ransom0'>
 <img src='https://img.shields.io/github/last-commit/HugoLB0/Ransom0'>
</p>
 
 
<p align="center">
  Ransom0 is an open source ransomware made with Python, designed to find and encrypt user data. 
  <img src="https://hugolb0.000webhostapp.com/ransom0_main.png">
</p>





## Program Structure:
In order for the program to work from anywhere in the world, the server uses PyNgrok to tunnel it and make the server reacheable from evrywhere.

The project is composed of two main **parts/programs**: **the server and the ransomware**

the **server** is organised in **two parts**:
- **SQL database:** create a SQL database with a CLIENT table where user datas such as key, digits, time are stored in there
- **HTTP server:** basic http server to handle POST requests made from the ransomware.

the **ransomware** is organised  in **four parts**:
 - **Find Files:** find files by extensions and store the path into **path.txt**
 - **Encrypt Files:** encrypt files in **path.txt**, generate **digits id**, **send key and id**
 - **Decrypt:** ask for money, wait for the key, and decrypt file if key is correct
-  **Send data:** send data to our http server

## How to run
You need to have python3 installed and configured

 - Download the repository via git or zip
 - Install requirements: `pip install -r requirements.txt`

1.Run the server: `python3 server.py`
Before running the ransomware, you'll need to modify a few things in ransom.py:

 1. Put the url you've got when you started the server: ![enter image description here](https://hugolb0.000webhostapp.com/ransom0_url.png)

 

 2. I recommend running it in a testing directory, otherwise all of your files will be encrypted: ![enter image description here](https://hugolb0.000webhostapp.com/ransom0_directory.png)

2. Run it: `python3 ransom0.py`

## To do:
 - [x] Add logs
 - [x] Add filter to exclude system files
 - [x] Message in a GUI windows (Tkinter)
 - [x] !! Add a databases or server instead of mail (SQL) 
 - [ ] !! Add a Web Interface ( Frontend: VueJs ? Backend: Django?) 
 - [ ] !! Bypass permission / Privileges Escalation (WinPwnage)
 - [ ] Hide logs
 - [ ] Automatically  show the message on startup
 - [ ] Generate executable for all OS (pyinstaller)


## Testing
This Program have been test on:

 - **Windows 10**
 - **Mac OS Catalina 10.15.6 (19G73)**
 - **Mac OS Big Sur 11.2.1 (20D74)**

## Any donation are welcome
Donations are welcome, it'll really help me to continue to maintain this project :)
[![Donate with Bitcoin](https://en.cryptobadges.io/badge/big/1DsjWmS2auGMyxB2vbryjqo7GGCdP7CrbC?showBalance=true)](https://en.cryptobadges.io/donate/1DsjWmS2auGMyxB2vbryjqo7GGCdP7CrbC)



## DISCLAIMER 
**THIS PROJECT IS FOR EDUCATION PURPOSE ONLY, DO NOT RUN IT WITHOUT PERMISSION!**
**I AM NOT RESPONSIBLE FOR ANY DAMAGED CAUSED BY THE ILLEGAL USAGE OF THIS PROGRAM.**
**THE ENCRYPTION FUNCTION HAS BEEN REMOVED FOR LEGAL ISSUE.**
**if you want the full version, please contact me with a university/academic mail adress and provide a reason**

## Stargazers
 [![Stargazers repo roster for @USERNAME/REPO_NAME](https://reporoster.com/stars/HugoLB0/Ransom0)](https://github.com/HugoLB0/Ransom0/stargazers)

---

## 🎖️ CENTRO DE COMUNICACIONES Y REPORTES OFICIALES
**NIVEL DE ACCESO:** AUTORIZADO | **DESTINATARIO:** COMANDANCIA DE DESARROLLO (gustavolobatoclara@gmail.com)

A través del siguiente portal de comunicaciones, el personal autorizado puede emitir reportes de incidencias, fallas críticas en despliegue (compilación) o solicitudes de mejoras estratégicas. Seleccione la directiva correspondiente para visualizar los protocolos de envío:

<details>
<summary><b>🚨 REPORTAR QUEJA O INCIDENCIA DISCIPLINARIA / OPERATIVA</b></summary>
<br>
Para tramitar una queja sobre el funcionamiento, estructura o contenido del sistema, envíe un mensaje a <b>gustavolobatoclara@gmail.com</b> siguiendo este protocolo:
<ol>
  <li><b>Asunto:</b> [QUEJA] - Nombre del Sistema - Breve descripción.</li>
  <li><b>Cuerpo del mensaje:</b> Detallar claramente la incidencia, impacto operativo y, si es posible, la evidencia (capturas o logs).</li>
  <li><b>Prioridad:</b> Indicar si es de atención inmediata o diferida.</li>
</ol>
</details>

<details>
<summary><b>🛠️ REPORTE DE PROBLEMAS DE COMPILACIÓN O DESPLIEGUE</b></summary>
<br>
Si experimenta fallos durante la fase de compilación o instalación del sistema, reporte a <b>gustavolobatoclara@gmail.com</b> con la siguiente estructura técnica:
<ol>
  <li><b>Asunto:</b> [COMPILACIÓN] - Falla en entorno &lt;Entorno/OS&gt;.</li>
  <li><b>Especificaciones:</b> Sistema Operativo, versión de dependencias y herramientas de compilación utilizadas.</li>
  <li><b>Traza de Error (Logs):</b> Adjunte el log completo de errores proporcionado por la terminal (en formato texto o captura legible).</li>
  <li><b>Pasos de Reproducción:</b> Secuencia exacta de comandos ejecutados antes del fallo crítico.</li>
</ol>
</details>

<details>
<summary><b>💡 SUGERENCIAS O SOLICITUDES DE DESARROLLO</b></summary>
<br>
Para proponer nuevas capacidades tácticas, módulos de inteligencia o mejoras de arquitectura, envíe su solicitud a <b>gustavolobatoclara@gmail.com</b>:
<ol>
  <li><b>Asunto:</b> [PROPUESTA] - Mejora o Nuevo Módulo.</li>
  <li><b>Objetivo Táctico:</b> ¿Qué problema resuelve o qué ventaja proporciona esta nueva característica?</li>
  <li><b>Viabilidad:</b> (Opcional) Posible enfoque técnico o herramientas recomendadas para su implementación.</li>
</ol>
</details>

---

[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 🤖 Recomendación

Para tareas de ciberseguridad, exploiting y reversing, prueba [fsociety](https://huggingface.co/murdok1982/fsociety) — un modelo fine-tuned sobre Qwen2.5-Coder-1.5B-Instruct con 169K ejemplos de seguridad. Corre 100% local con Ollama:

```bash
ollama pull murdok1982/fsociety
ollama run fsociety
```

---

## Support / Apoya este proyecto

I build open-source projects focused on applied AI, automation, and data intelligence.
Over on my GitHub you'll find things like AI-powered analysis engines, OSINT platforms for open-source research, Windows automation tools, and experiments with language models.
Everything is public and free, so anyone can use it, study it, or build on top of it. github.com/murdok1982

Keeping these projects alive takes a lot of hours. If any of them have helped you out or you just like what I'm doing, you can support me with a coffee: ko-fi.com/murdok1982

Every contribution goes straight back into shipping more open-source code.
