# Creació MySQL Server
En aquest apartat crearem el nostre MySQL Server dins d'una màquina CentOS 7.

# Passos a seguir

1. Actualitzar equip <br>
  Actualitzem l'equip abans de fer res.
  `sudo yum update`
  
2. Afegir repositori

  ![image](https://user-images.githubusercontent.com/79653853/154885430-245abb78-915e-4df1-b61f-e584500a7b28.png)
  ![image](https://user-images.githubusercontent.com/79653853/154885561-d861d783-7f3b-4e83-b459-6d33337ebc2a.png)

3. Prepararem el repositori

  ![image](https://user-images.githubusercontent.com/79653853/154885671-6ec5a88f-3047-49a9-9074-79f86ad9cb5c.png)

5. Instal·lar MySQL 8.0

  ![image](https://user-images.githubusercontent.com/79653853/154885705-db3cc3c4-3c8a-4aae-ad86-37ef89230aac.png)
  
  
# PREGUNTES

1. A on es troben físicament els fitxers de dades?  <br>
  `/var/lib/mysql`
2. A on es troba el fitxer de configuració? Quin és el seu contingut? <br>
  Es troba a `/etc/mysql`
3. El procés de mysqld escolta al port 3306. Quina modificació/passos caldrien fer per canviar aquest port a 33306 per exemple? Important: No realitzis els canvis. Només indica els passos que faries. <br>
  Anar al fitxer de configuració my.cnf 6.2 Afegir les linies port=33306 6.3 Fer restart del servei sudo systemctl restart mysql
4. Un cop finalitzada la instal·lació i veure que funciona, mostra el resultat de la comanda: <br>
5. ps -ef | grep mysql <br>
6. Quines són les característiques principals que ofereix MySQL 8.0 enfront de la 5.7. <br>
  La versió 8.0 ofereix les CTE (Common Table Expressions), regexp, windows functions, invisible indexes, unicode suport i noves mesures de seguretat
8. Ensenya al professor que us podeu connectar al SGBD. <br>

## TODO
  
  Secure installation
  
