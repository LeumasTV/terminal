# 🖥️ Mon Profil Terminal Windows

Ce projet contient **tout ce qu'il faut savoir** sur mon **profil de Terminal Windows** 🛠️. Si vous êtes curieux de voir ma configuration ou de vous en inspirer, vous êtes au bon endroit ! 🚀

## 🗂️ Contenu du dépôt
- 🎨 **Personnalisation** : Thèmes, couleurs, et styles.
- ⚡ **Alias et fonctions** : Gagnez du temps avec mes raccourcis !
- 🔧 **Outils intégrés** : Tout ce qui améliore l'expérience Terminal.

#!/bin/bash

# 🚀 Installer et configurer votre environnement de Terminal

## 📦 1. Installation de Oh-My-Posh  
➡️ Installation de Oh-My-Posh  
curl -s https://ohmyposh.dev/install.sh | bash -s -- -d /bin  

## 🎨 2. Installation de mon template Oh-My-Posh  
➡️ Installation du thème personnalisé  
wget https://raw.githubusercontent.com/LeumasTV/homelab/refs/heads/main/omp-template.omp.json -P /home/YOUR-USER    

## 🔍 3. Installation de Neofetch  
➡️ Installation de Neofetch  
sudo apt update && sudo apt install neofetch -y  

## 🌟 4. Ajout de votre ASCII Art pour Neofetch  
➡️ Installation de votre ASCII Art  

Générez un ASCII Art basé sur du texte en utilisant ce site :  
https://patorjk.com/software/taag/#p=display&f=Graffiti&t=Type%20Something%20  
Créez un fichier nommé "neo" à la racine de votre utilisateur (nano ~/neo) et collez-y le contenu généré. ✅  

## 🌀 5. Installation de Ble.sh (auto-complétion pour Bash)  
➡️ Installation de Ble.sh !!! Le programme doit être installer sur CHAQUES utilisateurs, l'installation est donc necessaire sur votre compte utilisateur AINSI que le compte ROOT)  
sudo apt install git make gawk -y  
git clone --recursive --depth 1 --shallow-submodules https://github.com/akinomyoga/ble.sh.git  
make -C ble.sh install PREFIX=~/.local  

## 🛠️ 6. Configuration pour ROOT et USER  
➡️ Configuration des sources pour ROOT et USER  
# Ajouter les sources dans .bashrc ROOT  
echo 'source ~/.local/share/blesh/ble.sh' >> /root/.bashrc  
echo 'eval "$(oh-my-posh init bash --config /home/YOUR-USER/omp-template.omp.json)"' >> /root/.bashrc  
echo 'neofetch --source /home/lsnetwork/neo' >> /root/.bashrc  

# Ajouter les sources dans .bashrc USER  
echo 'source ~/.local/share/blesh/ble.sh' >> /home/YOUR-USER/.bashrc  
echo 'eval "$(oh-my-posh init bash --config /home/YOUR-USER/omp-template.omp.json)"' >> /home/YOUR-USER/.bashrc  
echo 'neofetch --source /home/YOUR-USER/neo' >> /home/YOUR-USER/.bashrc  

## 🔄 7. Rechargez les fichiers de configuration  
➡️ Rechargement du fichier .bashrc pour ROOT  
source /root/.bashrc  

## ⚠️ 8. Modifier la configuration PAM  
➡️ Commenter les lignes dans /etc/pam.d/sshd pour désactiver les MOTD dynamiques  
# Les lignes suivantes doivent être commentées :  
# session    optional     pam_motd.so  motd=/run/motd.dynamic  
# session    optional     pam_motd.so noupdate  

✅ Installation et configuration terminées ! 🎉  

