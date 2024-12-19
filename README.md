**Cahier des Charges**

---

### **Projet : Application de Vérification d'Existence et Informations sur les Entreprises**

#### **1. Introduction**
Le projet consiste à développer une application web permettant de vérifier l’existence d’une entreprise et d’obtenir des informations à son sujet via l’API Sirene V3 fournie par le gouvernement français. L’application utilisera Java avec Spring Boot pour le backend et React pour le frontend.

---

#### **2. Objectifs du Projet**
1. Offrir une interface intuitive pour rechercher une entreprise par son SIRET ou son nom.
2. Consommer l’API Sirene V3 pour vérifier l’existence de l’entreprise.
3. Afficher les informations pertinentes sur l’entreprise telles que :
   - Nom de l’entreprise.
   - Adresse.
   - Activité principale (Code NAF).
   - Date de création.
4. Garantir une expérience utilisateur fluide avec une architecture respectant les bonnes pratiques.

---

#### **3. Périmètre Fonctionnel**

##### **3.1. Frontend (React)**
1. Page d'accueil avec un champ de recherche (SIRET ou nom de l'entreprise).
2. Affichage des résultats sous forme de tableau ou de carte.
3. Gestion des erreurs d’entrée utilisateur (validation des SIRET, gestion des noms incomplets, etc.).
4. Notifications pour indiquer les états de chargement, erreurs ou succès.

##### **3.2. Backend (Spring Boot)**
1. Point d’entrée principal pour recevoir les requêtes du frontend.
2. Connexion à l'API Sirene V3 pour récupérer les informations.
3. Validation et traitement des données avant envoi au frontend.
4. Gestion des erreurs (API non disponible, requêtes incorrectes, etc.).

---

#### **4. User Stories**

**US01**
- **En tant que** visiteur,
- **Je veux** pouvoir rechercher une entreprise par son numéro SIRET,
- **Afin de** vérifier si elle existe.

**Critères d’acceptation :**
- Le champ de recherche accepte uniquement un numéro SIRET valide.
- En cas de numéro invalide, un message d’erreur clair est affiché.

---

**US02**
- **En tant que** visiteur,
- **Je veux** rechercher une entreprise par son nom,
- **Afin de** trouver des entreprises correspondantes.

**Critères d’acceptation :**
- La recherche retourne une liste d’entreprises correspondantes avec leurs SIRET.
- Les entreprises sont affichées par pertinence.

---

**US03**
- **En tant que** utilisateur,
- **Je veux** consulter les détails d'une entreprise,
- **Afin de** mieux comprendre ses activités et son adresse.

**Critères d’acceptation :**
- Les détails incluent le nom, l’adresse, le code NAF et la date de création.
- Les informations sont présentées de manière lisible.

---

#### **5. Contraintes Techniques**
1. **Backend :**
   - Langage : Java avec Spring Boot.
   - Respecter une architecture en couches (Controller, Service, Repository).
2. **Frontend :**
   - Langage : JavaScript.
   - Framework : React.
3. **API :**
   - Intégration avec l’API Sirene V3 (documentation : https://api.gouv.fr/les-api/sirene_v3).
   - Gestion des clés d’API et quotas.
