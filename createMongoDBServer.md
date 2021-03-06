# Creació MongoDB Server
En aquest apartat crearem el nostre MongoDB Server dins d'una màquina CentOS 7.

# Passos a seguir

1. Actualitzar equip <br>
  Actualitzem l'equip abans de fer res. En aquest cas, ja el tenim actualitzat.
  
 ![image](https://user-images.githubusercontent.com/79653853/154332241-584e0402-0a36-48b3-9f7b-454abb1b8bb5.png)

2. Creació fitxer repositori Mongo <br>
  Ara, crearem el un fitxer on guardarem tota la conf.
  
  ![image](https://user-images.githubusercontent.com/79653853/154334269-24e952cd-fd67-423a-a26a-baef4b68d257.png)

  Amb el següent text
  
  ![image](https://user-images.githubusercontent.com/79653853/154335136-d5e43769-285a-41e0-8130-9fa0d7a17bb3.png)

3. Actualizem llista de paquets
  Actualizem la llista de paquets de forma que poguem descarregar MongoDB pròximament.
  
  ![image](https://user-images.githubusercontent.com/79653853/154335529-7ca41322-22ed-4693-b1fd-35dcc3fc9809.png)


4. Instal·lem MongoDB Server
  
  ![image](https://user-images.githubusercontent.com/79653853/154336436-324a6267-9734-4b40-9432-5282791eccc8.png)

  ![image](https://user-images.githubusercontent.com/79653853/154336488-f654cb19-906f-407a-b0cc-2349c86d5e29.png)

5. Comprobarem l'estatus del servei
  
  ![image](https://user-images.githubusercontent.com/79653853/154336707-4d2c5e9b-2fed-465e-ab98-db6a31e0f422.png)

6. Iniciem el servei de mongo

  ![image](https://user-images.githubusercontent.com/79653853/154336815-dcb30685-e3fb-408a-a762-6ed717f1c119.png)


7. Farem iniciar el servei en l'arrencada del SO

  ![image](https://user-images.githubusercontent.com/79653853/154336944-64b7937c-ab1d-4168-9025-4b30977aa333.png)
 
8. Securitzarem el nostre MongoDB mitjançant una contrasenya.
  Anirem a /etc/mongod.conf i buscarem la directiva `security`.
  
  ![image](https://user-images.githubusercontent.com/79653853/154883610-e5819a20-7586-4dbe-9269-fdbe42e6ab20.png)
  
9. Reiniciar servei

  ![image](https://user-images.githubusercontent.com/79653853/154883848-756a14cb-4a98-4f65-b280-2739ea112b0a.png)

10. Creació usuari
  10.1 Accedim al SGBD mitjançant la comanda `mongo`
  10.2 Crearem l'usuari `asix` i donarem els permissos necessaris
  
  ![image](https://user-images.githubusercontent.com/79653853/154884158-f5c74155-057f-49c7-96a4-94c01e0c8dc3.png)
  
  10.3 Accedim amb l'usuari

  ![image](https://user-images.githubusercontent.com/79653853/154884261-cd26ca7b-f0f5-48f8-a34a-811f6fd5034f.png)

11. Configuració Firewall
  
  ![image](https://user-images.githubusercontent.com/79653853/154884417-63592d0b-c436-4fcf-be56-282279f8049f.png)


Finalment, tenim al nostre SGBD MongoDB instal·lat i securitzat.
