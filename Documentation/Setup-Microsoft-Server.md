![logo](https://eliasdh.com/assets/media/images/logo-github.png)
# 💙🤍Setup Microsoft Server🤍💙

## 📘Table of Contents

1. [📘Table of Contents](#📘table-of-contents)
2. [🖖Introduction](#🖖introduction)
3. [✨Steps](#✨steps)
    1. [👉Step 1: TODO](#👉step-1-todo)
    2. [👉Step 2: Extra](#👉step-2-extra)
4. [🔗Links](#🔗links)

---

## 🖖Introduction

This tutorial explains how to install a Microsoft server on Ubuntu 24.04 LTS. This server is a Minecraft server that allows you to play Minecraft with your friends. The installation and configuration of the server is explained in this tutorial.

## ✨Steps

### 👉Step 1: TODO
```bash
sudo apt update && sudo apt upgrade -y
sudo apt install -y openjdk-17-jre-headless screen
mkdir -p /minecraft && cd /minecraft
wget https://piston-data.mojang.com/v1/objects/84194a2f286ef7c14ed7ce0090dba59902951553/server.jar
java -Xmx1G -Xms1G -jar server.jar nogui
echo "eula=true" > eula.txt
cat << EOF > server.properties
gamemode=creative
difficulty=normal
motd=Welcome to EliasDH Minecraft Server
pvp=true
spawn-protection=0
EOF
sudo ufw allow 25565/tcp
screen -S minecraft -d -m java -Xmx1G -Xms1G -jar server.jar nogui
screen -r minecraft
```

### 👉Step 2: Extra
```bash
hostname -I

screen -r minecraft

stop

exit
```

## 🔗Links
- 👯 Web hosting company [EliasDH.com](https://eliasdh.com).
- 📫 How to reach us elias.dehondt@outlook.com