## 📄 Se connecter au serveur

### Objectif

Se connecter au serveur apres un reboot

### Se reconnecter au serveur

<pre>ssh ton_utilisateur@IP_DU_SERVEUR</pre>
exemple:	`ssh ubuntu@54.37.38.46`

### Vérifier l'état du serveur

<pre>uptime
df - h
free -h</pre>

### Vérifier les MAJ de sécurité

<pre>sudo apt update && sudo apt upgrade -y</pre>
*Facultatif si des updates sont faite regulierement.*

### Vérifier que le Firewall est actif

<pre>sudo ufw status</pre>
*il doit être actif.*

#### Activer le firewall (si besoin)

<pre>sudo ufw enable</pre>

### Vérifier que Fail2ban est bien actif (protection brute-force)

<pre>sudo systemctl status fail2ban</pre>
*Il doit être actif*

### Vérifier que SSH fonctionne correctement
#### (Si sshd_config a été modifié)

<pre>sudo systemctl status ssh</pre>

### Vérifier les conteneurs Docker

<pre>sudo docker ps</pre>
si c'est vide -> ils ne sont pas relancés.

#### Lancer manuellement tes conteneurs (si besoin)

<pre>sudo Docker start NOM_DOCKER</pre>
exemple:	`sudo docker start mc-server`