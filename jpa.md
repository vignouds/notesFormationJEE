transient : objet non associé à une table
persist() -> va essayer de le créer dans la table
merge() -> fusionner
persistant : associé à une table

JPQL : on écrit des requêtes sur des objets java, pas sur des tables SQL !

Hors JAVA EE, il est nécessaire de créer une transaction avec :
````
EntityTransaction transac = em.getTransaction();
transac.begin();
````

pour les requêtes jpql simple, pas besoin d'alias
````
Query query = em.createQuery("select livre from Livre livre where livre.titre='Germinal'");
//équivaut à
Query query = em.createQuery("from Livre where titre='Germinal'");
````

//requete criteria qui recupère tous les clients d'une banque

//Join : requete jpql pour recuperer tous les clients qui ont un solde >0
