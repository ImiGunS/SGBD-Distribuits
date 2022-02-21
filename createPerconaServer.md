# Creació Percona Server
En aquest apartat crearem el nostre Percona Server dins d'una màquina CentOS 7.

# Passos a seguir

1. Actualitzar equip <br>
  Actualitzem l'equip abans de fer res.
  
  ![image](https://user-images.githubusercontent.com/79653853/153276736-433a5e20-f3ab-4193-a6d7-5160be7535f5.png)

2. Afegir repositori yum <br>
  Afegirem el repositori yum de percona per després procedir amb la instal·lació del nostre SGBD.
  
  ![image](https://user-images.githubusercontent.com/79653853/153276810-b7b5938d-ace0-429b-ae31-692d1fb9535e.png)

  
3. Comprovar repositori <br>
  Seguidament,  comprovarem que la instal·lació del repositori ha sigut un èxit.
  
  ![image](https://user-images.githubusercontent.com/79653853/153276828-22ebc1de-f51e-42c6-9baa-9d36c4bead96.png)

  
4. Habilitar repositori <br>
  Ara habilitarem el repositori de percona per tal de procedir amb la instal·lació
  
  ![image](https://user-images.githubusercontent.com/79653853/153277191-e4160d74-093e-43e8-8a83-598dc62098b5.png)

5. Instal·lar Percona Server <br>
  Finalment instal·larem el nostre percona server per mysql 8.0. Per fer aquesta acció, necessitarem executar un seguit de comandes.
  
  ![image](https://user-images.githubusercontent.com/79653853/153277497-895dda75-7870-4061-8f15-42866dcb91b8.png)
  
  ![image](https://user-images.githubusercontent.com/79653853/153277526-d686cbeb-b868-477c-93e8-6cbde0c8e420.png)

6. Comprovar instal·lació <br>
  Comprovarem la instal·lació del nostre percona server amb mysql 8.0
  
  ![image](https://user-images.githubusercontent.com/79653853/153277852-df8a6137-f03c-41b2-94a8-2d748fafbb5d.png)

7. Inicialitzar servei <br>
  Comprovarem la instal·lació del nostre percona server amb mysql 8.0
  
  ![image](https://user-images.githubusercontent.com/79653853/153278216-3991c592-054d-40ec-b5ce-a0fe9d490e4a.png)

  
8. Comprovar servei <br>
  Farem la comprovació que el servei mysql està corrent
  
  ![image](https://user-images.githubusercontent.com/79653853/153278341-6b4ed0e3-9110-45b7-9aea-72826815eb6e.png)

  
9. Finalitzar instal·lació <br>
  Ara que finalment tenim el nostre servei operatiu, copiarem la contrasenya temporal i executarem l’script d’instal·lació segura.
  
  ![image](https://user-images.githubusercontent.com/79653853/153278734-fbd6c215-c08a-4cca-b611-50c58ee5ea66.png)

  ![image](https://user-images.githubusercontent.com/79653853/153278743-d1ea04a9-04a4-4c35-a4b6-349954527530.png)

  ![image](https://user-images.githubusercontent.com/79653853/153278766-247c0501-2451-4f5d-9f19-3c3d236c8f74.png)

  ![image](https://user-images.githubusercontent.com/79653853/153278784-cf006221-8da0-4fa3-ab80-eb7cf1e0d5b8.png)

  ![image](https://user-images.githubusercontent.com/79653853/153278815-94917996-7a77-4e51-a8d4-3e3c840fcc8f.png)
  
  
# PREGUNTES  

1. Un cop realitzada la instal·lació realitza una securització de la mateixa. Quin programa
realitza aquesta tasca? Realitza una securització de la instal·lació indicant que la
contrasenya de root sigui patata. <br>

La securització ha sigut feta en un pas anterior, amb els paràmetres ja demanats

2. Quines són les instruccions per arrancar / verificar status / apagar servei de la base de
dades de Percona Server en el CentOS 7 <br>

  2.1 Arrancar Servei <br>
  
  ![image](https://user-images.githubusercontent.com/79653853/154350140-e53937a0-9f55-4c61-b245-783edc2cf69c.png)
  
  2.2 Verificar Servei <br>
  
  ![image](https://user-images.githubusercontent.com/79653853/154350097-50d3f171-afe3-44ea-866a-3f5e491d89a2.png)
  
  2.3 Parar Servei <br>
  
  ![image](https://user-images.githubusercontent.com/79653853/154350069-65b67d5a-860f-4d8f-8266-85236cc326d1.png)

  
3. A on es troba i quin nom rep el fitxer de configuració del SGBD Percona Server? <br>

Aquest fitxer es troba a `/etc` i rep el nom de `my.cnf`

4. A on es troben físicament els fitxers de dades (per defecte). Com ho has sabut? <br>

Si ens fixem en l'arxiu de configuració, podem veure que aquests fitxers es desen a `/var/lib/mysql`

![image](https://user-images.githubusercontent.com/79653853/154870284-fde22bcb-7447-49b0-9a17-14e729c081f8.png)


5. Crea un usuari anomenat asix en el sistema operatiu i en SGBD de tal manera que aquest
usuari del sistema operatiu no hagi d'introduir l'usuari i password cada vegada que cridem
al client mysql? <br>
  5.1 https://dev.mysql.com/doc/refman/8.0/en/password-security-user.html <br>
  5.2 Usuari SO-→ asix / patata <br>
    sudo useradd asix
    sudo passwd asix
  5.3 Usuari MySQL → asix / patata <br>
    Escriure les següents linies al `my.conf`
  ![image](https://user-images.githubusercontent.com/79653853/154870812-4dc7439d-c0fd-4d98-8cc9-7c98145a45c1.png)
    Fer restart del servei


6. El servei de MySQL (mysqld) escolta al port 3306. Quina modificació/passos caldrien fer
per canviar aquest port a 33306 per exemple? <br>

  6.1 Anar al fitxer de configuració `my.cnf` <br>
  6.2 Afegir les linies `port=33306` <br>
  6.3 Fer restart del servei `sudo systemctl restart mysql` <br>

7. Important: No realitzis els canvis. Només indica els passos que faries. <br>

8. Ensenya al professor que us podeu connectar al SGBD. <br>



