###### *<div align="right"><sub>// by S7lver</sub></div>*
<div align="center">    

<br>

 <div style="border: 2px solid #f39c12; padding: 10px; border-radius: 5px; background-color: #fdf2e9; color: #d35400; font-size: 16px;">
  <strong>⚠️ In Developing:</strong><br>
    This repository is in developing for now. <br>
  If theres a bug, you can report it at: <a href="" style="color: #d35400; text-decoration: underline;">Ollama Server</a> for contribute this project.
</div>

<br>
  <a href="#installation"><kbd><br> Installation <br></kbd></a>&ensp;&ensp;
  <a href="#usage"><kbd><br> Usage <br></kbd></a>&ensp;&ensp;
</div>

<a id="installation"></a>  
---
Make sure you have these settings on your server
- **DISABLED IPV6**, go [here]() to find how you can disable it
- **AT LEAST 8GB RAM**, the model requires at least 8GB, but i recommend **16GB**
- **WSL2**, for docker support, you can find mor info [here]()
- **VIRTUALIZATION ENABLED ON BIOS**, you can know how enable it [here]()

For install it, you need to download the release zip from [HERE]() it is fully tested on windows 11, but **may** can work on [WSL2]().

> [!IMPORTANT]
> You will need to reboot the server many times to install this project
> make sure than all your staff is saved before rebooting

> [!CAUTION]
> **DO NOT USE WINDOWS 7 OR 10**, use 11

To install, follow the next steps:

<h3> step1 </h3>

```shell
# download the .zip
unzip release.zip
cd release
./ollama.exe
# reboot the pc
```
<h3> step2 </h3>

now its time to do some configurations, first we need to **create a enviroment variable**



after that, reboot the computer

when the computer reboot, open task manager

and disable ollama to run as a start program

after that, reboot again

<h3> step3 </h3>

Time to install **Docker Desktop**

```shell
# on the release folder
./DockerDesktop.exe
# reboot the pc
```

later, you can run DockerDesktop as Administrator

<h3> step4 </h3>
time for some command in ps

```powershell
docker run --hostname=a6c857bfa980 --user=0:0 --mac-address=02:42:ac:11:00:02 --env=OLLAMA_BASE_URL=http://<"change this for your ip address, starting for 192.168">:11434 --env=PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin --env=WEBUI_URL=http://0.0.0.0:3000 --env=LANG=C.UTF-8 --env=GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D --env=PYTHON_VERSION=3.11.11 --env=PYTHON_SHA256=2a9920c7a0cd236de33644ed980a13cbbc21058bfdc528febb6081575ed73be3 --env=ENV=prod --env=PORT=8080 --env=USE_OLLAMA_DOCKER=false --env=USE_CUDA_DOCKER=false --env=USE_CUDA_DOCKER_VER=cu121 --env=USE_EMBEDDING_MODEL_DOCKER=sentence-transformers/all-MiniLM-L6-v2 --env=USE_RERANKING_MODEL_DOCKER= --env=OPENAI_API_BASE_URL= --env=OPENAI_API_KEY= --env=WEBUI_SECRET_KEY= --env=SCARF_NO_ANALYTICS=true --env=DO_NOT_TRACK=true --env=ANONYMIZED_TELEMETRY=false --env=WHISPER_MODEL=base --env=WHISPER_MODEL_DIR=/app/backend/data/cache/whisper/models --env=RAG_EMBEDDING_MODEL=sentence-transformers/all-MiniLM-L6-v2 --env=RAG_RERANKING_MODEL= --env=SENTENCE_TRANSFORMERS_HOME=/app/backend/data/cache/embedding/models --env=TIKTOKEN_ENCODING_NAME=cl100k_base --env=TIKTOKEN_CACHE_DIR=/app/backend/data/cache/tiktoken --env=HF_HOME=/app/backend/data/cache/embedding/models --env=HOME=/root --env=WEBUI_BUILD_VERSION=29a271959556743e6deb4d55a5a982983335d7ab --env=DOCKER=true --volume=open-webui:/app/backend/data --network=bridge --workdir=/app/backend -p 3000:8080 --restart=always --label='org.opencontainers.image.created=2024-12-07T08:43:10.932Z' --label='org.opencontainers.image.description=User-friendly AI Interface (Supports Ollama, OpenAI API, ...)' --label='org.opencontainers.image.licenses=MIT' --label='org.opencontainers.image.revision=29a271959556743e6deb4d55a5a982983335d7ab' --label='org.opencontainers.image.source=https://github.com/open-webui/open-webui' --label='org.opencontainers.image.title=open-webui' --label='org.opencontainers.image.url=https://github.com/open-webui/open-webui' --label='org.opencontainers.image.version=main' --runtime=runc -d ghcr.io/open-webui/open-webui:main
```
<h3> step5 </h3>

after running this we can check if some things work, just to be sure we are on the right path

```bash
# open the following link
http://<"change this for your ip address, starting for 192.168">:11434/

# you should see something like this
Ollama is running
```

after that, we finally installed this project

<a id="Usage"></a>

for run ollama, you can use the **custom script**

```powershell
./run.bat
```

for run the frontend, just open DockerDesktop app

> [!IMPORTANT]
> If DockerDesktop app dont open, you need to open it as administrator

after that, you can open the following link and start configuring your new AI
```bash
http://<"change this for your ip address, starting for 192.168">:3000
```

for how to configure the frontend, look at [this](https://docs.openwebui.com/)