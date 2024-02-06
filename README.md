# CodeAlpha_Network_Intrusion_Detection
Here are the steps to install snort on Kali
1.Backup kali's sources.list

mv /etc/apt/sources.list /etc/apt/sources.list.bak

2.Remove updates

find /var/lib/apt/lists -type f -exec rm {} \;

3.Change sources.list content

sudo nano /etc/apt/sources.list
If you are using kali as a virtual machine then paste this instead
As core Ubuntu repositories do not have the ARM repositories in them
deb [arch=arm64] http://ports.ubuntu.com/ubuntu-ports focal main restricted universe multiverse
deb [arch=arm64] http://ports.ubuntu.com/ubuntu-ports focal-updates main restricted universe multiverse
deb [arch=arm64] http://ports.ubuntu.com/ubuntu-ports focal-security main restricted universe multiverse
deb [arch=i386,amd64] http://us.archive.ubuntu.com/ubuntu/ focal main restricted universe multiverse
deb [arch=i386,amd64] http://us.archive.ubuntu.com/ubuntu/ focal-updates main restricted universe multiverse
deb [arch=i386,amd64] http://security.ubuntu.com/ubuntu focal-security main restricted universe multiverse

4. Add the specified public keys

sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 3B4FE6ACC0B21F32
sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 871920D1991BC93C

5. Update

sudo apt update

6. Now install snort

sudo apt install snort
#IDS : intrusion detection System (est un mécanisme destiné à repérer des activités anormales ou suspectes sur la cible analysée un hoté

# ces IDS sont déployés afin de renforcer la sécurité existante, de remonter la source de l'attaque et détecter la technique d'attaques employés

# pour vérifier la configuration IP notre machine on doit saisir la commande "ifconfig"
<img width="650" alt="Capture d’écran 2024-02-06 à 12 54 27" src="https://github.com/abir1234-art/CodeAlpha_Network_Intrusion_Detection/assets/84373316/bdf9c9a5-4e50-4cbc-9291-e178b95cec48">


# Nous avons choisit de traiter un IDS bien particulier il s'agit de l'IDS SNORT

<img width="650" alt="Capture d’écran 2024-02-06 à 12 57 12" src="https://github.com/abir1234-art/CodeAlpha_Network_Intrusion_Detection/assets/84373316/78fd6214-7dc7-476a-9d8a-38b276c89d7f">

# Pour commencer à serveiller contre le Cyberattaques, il faut lancer le snort on utilise cette commande
#snort -A console -c /etc/snort/snort.conf

# Nous allons faire un Test de connectivité, on envoie un paquet ICMP à partir du réseau externe ma machine
<img width="650" alt="Capture d’écran 2024-02-06 à 13 00 11" src="https://github.com/abir1234-art/CodeAlpha_Network_Intrusion_Detection/assets/84373316/bb949765-cc00-4c43-afa7-91bf6a0b1813">

# SNORT affiche un message d'alerte <<Ping issue d'une machine Kali>>

<img width="650" alt="Capture d’écran 2024-02-06 à 12 59 42" src="https://github.com/abir1234-art/CodeAlpha_Network_Intrusion_Detection/assets/84373316/7b2f15b1-c2dd-461b-8a4c-4c4a9f1c40f7">




