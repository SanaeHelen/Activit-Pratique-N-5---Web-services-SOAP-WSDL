# Activit-Pratique-N-5---Web-services-SOAP-WSDL

1. Création d'un we service  :
     Tout d'abord, nous avons créé un projet Java avec IntelliJ. Dans le répertoire Java, nous avons créé le package `ws`, dans lequel nous avons défini deux classes : la classe `Compte` et la classe `BanqueService`.
   

     ![image](https://github.com/SanaeHelen/Activit-Pratique-N-5---Web-services-SOAP-WSDL/assets/136022070/9dba1f8a-33ae-48c4-a44d-82aa7effdc27)


   - La classe Compte :
     
     ![image](https://github.com/SanaeHelen/Activit-Pratique-N-5---Web-services-SOAP-WSDL/assets/136022070/a139892c-6f97-43e2-8341-827e2ac35b45)
     ![image](https://github.com/SanaeHelen/Activit-Pratique-N-5---Web-services-SOAP-WSDL/assets/136022070/c74c7884-ca95-45be-a064-0328823d6cdb)

   - La classe BanqueService :
     
       Dans la classe `BanqueService`, nous avons créé les méthodes suivantes :

     
     • Convertir un montant de l’euro en DH :
     
        ![image](https://github.com/SanaeHelen/Activit-Pratique-N-5---Web-services-SOAP-WSDL/assets/136022070/0b3c12a1-5a5b-4971-83cf-fc1466247348)

     • Consulter un Compte :
     
       ![image](https://github.com/SanaeHelen/Activit-Pratique-N-5---Web-services-SOAP-WSDL/assets/136022070/cd6b3d52-c8a0-46fd-a40f-fd58ad726eb3)

     • Consulter une Liste de comptes :
     
       ![image](https://github.com/SanaeHelen/Activit-Pratique-N-5---Web-services-SOAP-WSDL/assets/136022070/6aceed36-e610-41de-be0e-ea66f30e69b0)

2. Déployement du Web service avec un simple Serveur JaxWS :

    ![image](https://github.com/SanaeHelen/Activit-Pratique-N-5---Web-services-SOAP-WSDL/assets/136022070/f2ae38b9-d37e-4f6f-93d5-455b5310ea71)
    ![image](https://github.com/SanaeHelen/Activit-Pratique-N-5---Web-services-SOAP-WSDL/assets/136022070/6fee4002-e218-4bf6-88ee-f4f96274126e)
    
      
3. Consultation et analyse de WSDL avec un Browser HTTP :
   
    ![image](https://github.com/SanaeHelen/Activit-Pratique-N-5---Web-services-SOAP-WSDL/assets/136022070/98495054-54eb-4401-a8fc-f5bfec0c209f)
    ![image](https://github.com/SanaeHelen/Activit-Pratique-N-5---Web-services-SOAP-WSDL/assets/136022070/0ff89fcb-e5e5-4ed2-99e5-2e5b81457df1)
    ![image](https://github.com/SanaeHelen/Activit-Pratique-N-5---Web-services-SOAP-WSDL/assets/136022070/2284b58c-1e63-4678-a4a4-db92a1b19c29)

    Ce fichier XML est une définition WSDL (Web Services Description Language) pour le service web "BanqueWS". Voici une analyse en bref des principaux composants de ce fichier :
     
     - En-tête et Métadonnées :
     
         - Le fichier est généré par XML-WS Runtime version 4.0.2.
           
         - Il utilise plusieurs espaces de noms (namespaces) pour la sécurité, les politiques web, l'adressage, le schéma XML, et les spécifications WSDL.
           
     - Types :
     
         - Définit un schéma XML (xsd:schema) qui importe un autre schéma situé à http://localhost:9090/?xsd=1.
           
     - Messages :
     
          - getCompte et getCompteResponse: Messages pour l'opération de récupération d'un compte.
            
          - listComptes et listComptesResponse: Messages pour l'opération de liste des comptes.
            
          - ConversionEuroToDH et ConversionEuroToDHResponse: Messages pour l'opération de conversion de l'euro au dirham.
            
     - PortType :
     
          - BanqueService: Définit trois opérations disponibles sur le service :
            
               - getCompte: Récupération d'un compte.
                 
               - listComptes: Liste des comptes.
                 
               - ConversionEuroToDH: Conversion de l'euro au dirham.
                 
          - Chaque opération a des messages d'entrée et de sortie définis.
            
     - Binding :

          - BanqueServicePortBinding: Spécifie comment les opérations du service sont liées au protocole SOAP.
            
               - Utilise le transport HTTP pour SOAP.
                 
               - Chaque opération utilise un style "document" et un "literal" encoding pour les messages.
            
     - Service :
     
          - BanqueWS: Définit le service web.
            
          - BanqueServicePort: Définit le port du service, qui est lié à BanqueServicePortBinding.
            
          - L'adresse du service est http://localhost:9090/.

            
   
5. Teste des opérations du web service avec un outil comme SoapUI ou Oxygen :
   
     Après avoir installé l'outil SoapUI, nous avons créé un projet pour tester les opérations conversionEuroToDH avec différentes valeurs de montants, ainsi que 
    l'opération getCompte en fournissant des valeurs pour le code. Nous avons également consulté la liste des comptes.
   
    ![image](https://github.com/SanaeHelen/Activit-Pratique-N-5---Web-services-SOAP-WSDL/assets/136022070/eca728d9-112b-4795-b324-ab742e3cb457)
   
    ![image](https://github.com/SanaeHelen/Activit-Pratique-N-5---Web-services-SOAP-WSDL/assets/136022070/a1461381-3b6c-4e73-a33c-b26d3d6b18eb)

    ![image](https://github.com/SanaeHelen/Activit-Pratique-N-5---Web-services-SOAP-WSDL/assets/136022070/efef1bd0-63f1-4777-b31a-6d4fb9805273)
   
    ![image](https://github.com/SanaeHelen/Activit-Pratique-N-5---Web-services-SOAP-WSDL/assets/136022070/23d084e0-be48-4424-80a8-0f9eeeb946bd)
   
    ![image](https://github.com/SanaeHelen/Activit-Pratique-N-5---Web-services-SOAP-WSDL/assets/136022070/a306cb46-8a6e-4091-8d8f-bd1612ee4f7b)
   

    ![image](https://github.com/SanaeHelen/Activit-Pratique-N-5---Web-services-SOAP-WSDL/assets/136022070/80e261f8-ef26-43f6-a033-c47c77bd2ec1)
    ![image](https://github.com/SanaeHelen/Activit-Pratique-N-5---Web-services-SOAP-WSDL/assets/136022070/0ec735e4-bc18-480d-882d-b03f6d39cc82)

    ![image](https://github.com/SanaeHelen/Activit-Pratique-N-5---Web-services-SOAP-WSDL/assets/136022070/c37229d4-c98f-42e7-89fc-f1e30df10b37)

    
7. Créer un Client SOAP Java :
   
      - Générer le Stub à partir du WSDL :

         Dans le projet, nous avons créé un module intitulé : client-soap-java :
        
           ![image](https://github.com/SanaeHelen/Activit-Pratique-N-5---Web-services-SOAP-WSDL/assets/136022070/bb949d05-f5b0-47db-9e61-c5c66ccebfe1)

        
          Génération du proxy :

           ![image](https://github.com/SanaeHelen/Activit-Pratique-N-5---Web-services-SOAP-WSDL/assets/136022070/64e9b7b9-2be8-4c34-8119-42e85aa5bad2)
          
      - Créer un client SOAP pour le web service

         ![image](https://github.com/SanaeHelen/Activit-Pratique-N-5---Web-services-SOAP-WSDL/assets/136022070/96cc9268-5eb0-4fc0-a2ba-6d62aa2cfb3c)
         ![image](https://github.com/SanaeHelen/Activit-Pratique-N-5---Web-services-SOAP-WSDL/assets/136022070/49a1e0ac-12a9-4cfa-84ed-571d0aadf1df)























