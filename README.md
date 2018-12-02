

# Linux-server med Node.js & MySQL
Styresystemet er Centos 7.5 x64

## 0. Installer Nano
Nano er en linux tekst editor, som er rigtig let at bruge.

Installation
```
yum install nano
```

## 1. Installer MySQL
Installation
```
yum install mariadb-server
```
Start/stop/restart
```
systemctl start mariadb
```

Konfigurer MySQL
```
/usr/bin/mysql_secure_installation
```

## 2. Installer Node.js
Tilføj node.js repository
```
yum install -y gcc-c++ make
curl -sL https://rpm.nodesource.com/setup_11.x | sudo -E bash -
```
Installér node.js
```
yum install nodejs
```
Verificér versioner
```
node -v
npm -v
```

## 3. Installer PM2
PM2 er en process manager til Node.js applikationer.

Installation
```
npm install -g pm2
```

Kør PM2 ved startup
```
pm2 startup
```

## 4. Installer Git
Installation
```
yum install git
```

Konfiguration
```
git config --global user.name "Dit navn"
git config --global user.email "din@email.dk"
```

Tjek konfigurationen
```
nano ~/.gitconfig
```

## 5. Opret et nøglesæt til at logge ind på GitHub
Opret nøglesæt
```
ssh-keygen -t rsa
```

Åbn den offentlige nøgle
```
nano ~/.ssh/id_rsa.pub

Kopier indholdet af den offentlige nøgle til GitHub -> Settings -> SSH and GPG keys -> New SSH key
```

## 6. Opret en mappe til din applikation
```
mkdir ~/www
```
Naviger ind i mappen
```
cd ~/www
```

## 7. Klon dit repository fra GitHub
```
git clone git@github.com:brugernavn/repository
```

(og når du har en opdatering, skal du lave et pull)
```
git pull git@github.com:brugernavn/repository
```
