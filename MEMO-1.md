# MEMO COMMANDE LINUX

### Lecture des logs

Pour voir les logs en temps réel
> tail -f /var/log/*nom_du_service*

### PS AUX | GREP

Permet de voir les processus en cours et trouver la ligne contenant *terme_a_rechercher_string*
> ps aux | grep *apache2*

### Rechercher un fichier

Pour rechercher un fichier par son nom complet ou incomplet avec * 
> find /*localisation_dans_arboresence* *nom_du_fichier* 
> find /*localisation_dans_arboresence* _\*m_du_fichier_imcompl\*_ 

### NETSTAT

Pour Network Statistic affiche les connexions 
> netstat -tpln ou -nly ou -an
> __a__ affiche connexions actives TCP/UDP + port
> __n__ affiche adresse au format numérique

### NMAP

Permet de rechercher les ports en écoute

###