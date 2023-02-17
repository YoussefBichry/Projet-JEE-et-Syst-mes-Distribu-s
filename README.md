# Projet-JEE-et-Syst-mes-Distribu-s
### Première partie du Projet :
###Créer une application basée sur une architecture micro-service qui permet de gérer les factures contenant des produits et appartenant à un client.

#### 1.Créer le micro-service customer-service qui permet de gérer les client :
![Capture d’écran 2022-12-08 150515](https://user-images.githubusercontent.com/75500068/206467993-6cee1c2e-bbcd-4f1c-b6f8-49dccd80aa7e.png)


  #####  . Les dependances :Spring Web,Spring Data JPA,H2DataBase,Lombook,Rest Repositories,Eureka Discovery Client,Spring Boot Actuator.
  #####  . Notre Base de donnees :
  
  ![Capture d’écran 2022-12-08 152209](https://user-images.githubusercontent.com/75500068/206470669-b5e46d2f-6c4c-4689-851f-d398f37a0fa3.png)

  #####  . Pour le test :http://localhost:8081/customers :
				
![Capture d’écran 2022-12-08 151637](https://user-images.githubusercontent.com/75500068/206469157-c9985eb0-993d-4a3b-a520-8465f19997fd.png)

#### 2.Créer le micro-service inventory-service qui permet de gérer les produits :

![Capture d’écran 2022-12-08 152910](https://user-images.githubusercontent.com/75500068/206472268-5e2bc872-8292-4f30-b657-1ccfa0b2ab0b.png)

  #####  . Les dependances :Spring Web,Spring Data JPA,H2DataBase,Lombook,Rest Repositories,Eureka Discovery Client,Spring Boot Actuator.
  #####  . Notre Base de donnees :
  
  ![Capture d’écran 2022-12-08 153043](https://user-images.githubusercontent.com/75500068/206472729-607c5606-6981-42e6-b646-40b051f8179e.png)

   #####  . Pour le test :http://localhost:8082/products :
   
   ![Capture d’écran 2022-12-08 153245](https://user-images.githubusercontent.com/75500068/206473252-0077eb3c-297f-49e3-b4c7-d953230fab9a.png)

#### 3. Créer la Gateway Spring cloud Gateway avec une Configuration statique du système de routage :

![Capture d’écran 2022-12-08 154038](https://user-images.githubusercontent.com/75500068/206475279-a9301f64-7488-498b-9d44-5aa7249e36e4.png)
 
   #####  . Les dependances :GateWay,Eureka Discovery Client,Spring Boot Actuator.
#### 4. Créer l'annuaire Eureka Discrovery Service :

![Capture d’écran 2023-02-17 175124](https://user-images.githubusercontent.com/75500068/219714994-5f4ab25d-be2a-4374-ba51-d311a1bc70d5.png)

![Capture d’écran 2023-02-17 175206](https://user-images.githubusercontent.com/75500068/219715046-36fcba4b-2249-482f-888d-e1da26dc48ac.png)

    #####  . Pour le test :http://localhost:8761 :
    ![206577335-3bb77244-86f3-4690-b852-9ef0edbbfbc6](https://user-images.githubusercontent.com/75500068/219715765-88778354-cd39-42d3-b771-3c921efc3955.png)
    
#### 5. Faire une configuration dynamique des routes de la gateway
![Capture d’écran 2023-02-17 175124](https://user-images.githubusercontent.com/75500068/219716109-78941b77-716e-4be4-9455-26e231571912.png)

#### 6. Créer le service de facturation Billing-Service en utilisant Open Feign
![bill1](https://user-images.githubusercontent.com/75500068/219718412-6d541a67-3536-487e-919b-c5050848f9fd.png)
![bill2](https://user-images.githubusercontent.com/75500068/219718453-bb448548-c2af-45af-9f7a-f11f9c6b469b.png)
    
     #####  . Pour le test :http://localhost:8083/bills
  
#### 7. Créer un client Web Angular (Clients, Produits, Factures)
  ![an1](https://user-images.githubusercontent.com/75500068/219720036-77be1389-7ad3-4fec-a2c0-be7fbb55dbdc.png)
  ![ang2](https://user-images.githubusercontent.com/75500068/219720051-0d6e93cc-cdf2-4db4-86a3-2839e4ce3445.png)

     #####  . Pour l'affichag
 ![Capture d’écran 2023-02-17 181753](https://user-images.githubusercontent.com/75500068/219720584-50ff511a-2038-4868-92b7-a3567ca11ff3.pnge :http://localhost:4200
     
#### 8. Déployer le serveur keycloak :
![Capture d'écran_20230119_145602](https://user-images.githubusercontent.com/75500068/219721639-16f0c477-e242-43ca-8723-83d5c80a455c.png)

  #####  - Créer un Realm
![Capture d'écran_20230119_150206](https://user-images.githubusercontent.com/75500068/219732331-fba2e53a-7d87-4565-a593-dfc38216c7ff.png)
 
  ##### - Créer un client à sécuriser
![Capture d'écran_20230119_151156](https://user-images.githubusercontent.com/75500068/219733007-193f41b7-ddf8-4e1b-95d0-7c670622ddde.png)
![Capture d'écran_20230119_151350](https://user-images.githubusercontent.com/75500068/219733375-eb9e5bb4-133e-4c04-b8c4-291c9a0cc5bc.png)
![Capture d'écran_20230119_151734](https://user-images.githubusercontent.com/75500068/219733461-7e79a186-8602-4e17-aabe-510a35c0a337.png)

  #####  - Créer des utilisateurs
![Capture d'écran_20230119_153149](https://user-images.githubusercontent.com/75500068/219733608-84e1bef8-98a5-449c-b350-ad087b39bf4a.png)

 ##### - Créer des rôles
![Capture d'écran_20230119_154107](https://user-images.githubusercontent.com/75500068/219733888-ccba580b-ee9f-4770-98b5-b86fcf090490.png)

  ##### - Affecter les rôles aux utilisateurs
![Capture d’écran 2023-02-17 185037](https://user-images.githubusercontent.com/75500068/219735646-bfc2dfc8-caf7-4226-9772-cebf249e79a8.png)

  ##### - Tester les différents modes d'authentification avec Postman en montrant les contenus de Access-Token, Refresh Token 
  ###### Authentification avec mot de passe.
  ![KeycloakPassword](https://user-images.githubusercontent.com/75500068/219737297-c457004e-de65-4407-82aa-ae2f27c71ac8.png)
###### Analyse du contenu des deux JWT AccessToken et Refresh Token.
![token](https://user-images.githubusercontent.com/75500068/219737783-9f0d8551-c4f8-4d58-a96e-f0fa53d1f37e.png)
 ###### Authentification avec le jeton de rafraîchissement.
 ![KeycloakRefreshToken](https://user-images.githubusercontent.com/75500068/219738145-29a1b262-55e7-4b1b-ae54-7d0e3227f2b2.png)
  ###### Authentification avec ID client et secret client.
![KeycloakSecretKey](https://user-images.githubusercontent.com/75500068/219738656-e5562de8-1a08-4571-a98b-4b3a08952a30.png)

#### 9. Sécuriser les micro-services et le frontend angular en déployant les adaptateurs Keycloak
 ##### Page de connexion
![w1](https://user-images.githubusercontent.com/75500068/219740649-3ccd84d7-a2e9-403b-a61c-f95cb37a93c6.png)
 ##### Interface utilisateur normale
 ![w3](https://user-images.githubusercontent.com/75500068/219741551-271d112e-dc12-43a2-bf66-bed4237a1a84.png)
