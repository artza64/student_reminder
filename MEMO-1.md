# MEMO COMMANDE LINUX

### Lecture des logs

Les logs sont stockés dans /var/log
> cat affiche le contenu du fichier en integralité <br>
> less affiche le fichier en laissant la possibilité de naviguer dans le contenu

Pour voir les logs en temps réel 
> tail -f /var/log/*nom_du_service*

### PS AUX | GREP

Permet de voir les processus en cours et trouver la ligne contenant *terme_a_rechercher_string*
> ps aux | grep *apache2*

### Rechercher un fichier

Pour rechercher un fichier par son nom complet ou incomplet avec * 
> * find /*localisation_dans_arboresence* -name *nom_du_fichier* 
> * find / -name sources.list
> * find /*localisation_dans_arboresence* -name _\*m_du_fichier_imcompl\*_ 
> * find /etc -name '\*resolv.\*' 

### NETSTAT

Pour Network Statistic affiche les connexions 
> * netstat -tpln ou -nlt ou -an
> * __a__ affiche connexions actives TCP/UDP + port
> * __n__ affiche adresse au format numérique

### NMAP | SS

Permet de rechercher les ports en écoute
>nmap -p 80 IP_XXX.XXX.XXX.XXX

### CONFIGURATION RESEAU

Pour la configuration réseau 
> /etc/network/interfaces
Pour un serveur 
> allow netplug auto <br>
>   iface inet static <br>
>   address IP_XXX.XXX.XXX.XXX/XX <br>
>   gateway IP_XXX.XXX.XXX.XXX

Pour la configuration des DNS 
> /etc/resolv.conf

Toujours recharger le service aprés modif 
> systemctl reload *nom_du_service* <br>
> systemctl status *nom_du_service*

### EMPLACEMENTS UTILES

* /etc = tout ce qui concerne configuration
* /home = dossier utilisateur
* /etc/password = liste des utilisateurs
* /etc/group = liste des groupes
* /etc/network/interfaces = configuration réseaux
* /etc/resolv.conf = configuration des DNS
* /etc/apt/sources.list = liste repo debian

### APT

Pour voir le détail d'un paquet 
> apt show *NOM_DU_PAQUET*

Pour chercher un paquet
> apt search -n *TERME_A_CHERCHER*

Si plusieurs termes 
> apt search -n *TERME_1* -n *TERME_2*

### HTTPS SSL-TLS / AUTO CERTIFICATION / CERTIFICAT 

Certificat = fichier__.crt__
Clé privée = fichier__.key__