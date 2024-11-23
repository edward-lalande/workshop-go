## **Création d'une messagerie en Go**

---

### **1. Initialisation du projet**
1. Créez un nouveau projet :
   ```bash
   mkdir simple-messaging-app
   cd simple-messaging-app
   go mod init simple-messaging-app
   go get github.com/gin-gonic/gin
   go get github.com/google/uuid
   ```

2. Structurez le projet :
   ```plaintext
   simple-messaging-app/
   ├── main.go
   ├── handlers/
   ├── models/
   ├── db/
   └── routes/
   ```

3. Ajoutez les structures de données dans `models/` :

   #### **models/user.go**
   ```go
   package models

   type User struct {
       ID       string `json:"id"`
       Username string `json:"username"`
       Password string `json:"password"`
   }
   ```

   #### **models/message.go**
   ```go
   package models

   type Message struct {
       ID         string `json:"id"`
       SenderID   string `json:"sender_id"`
       ReceiverID string `json:"receiver_id"`
       Content    string `json:"content"`
       Timestamp  string `json:"timestamp"`
   }
   ```

---

### **2. Configurer une base de données simple**
1. Créez une base de données en mémoire dans `db/`. Implémentez des fonctions pour :
   - Ajouter un utilisateur.
   - Ajouter un message.
   - Récupérer les utilisateurs et messages.

---

### **3. Configurer les routes**
1. Créez un fichier `routes/routes.go` pour définir toutes les routes de l'application :
   - **POST /register** : Inscription d'un utilisateur.
   - **POST /login** : Authentification (pas de jeton dans ce workshop, mais vérifiez les identifiants).
   - **POST /messages** : Envoyer un message.
   - **GET /messages/:receiver_id** : Récupérer les messages entre l'utilisateur connecté et un autre.

2. Utilisez **Gin** pour relier chaque route à une fonction handler.

---

### **4. Implémenter les handlers**
1. **Inscription et connexion** (`handlers/user.go`) :
   - Implémentez un handler pour **POST /register** qui crée un utilisateur avec un UUID unique.
   - Implémentez un handler pour **POST /login** qui valide les identifiants.

2. **Envoi de messages** (`handlers/message.go`) :
   - Implémentez un handler pour **POST /messages** :
     - Validez que l'utilisateur existe.
     - Créez un message avec un UUID unique et un horodatage.
     - Ajoutez-le à la base de données.

3. **Récupération des messages** (`handlers/message.go`) :
   - Implémentez un handler pour **GET /messages/:receiver_id** :
     - Filtrez les messages pour n’afficher que ceux entre l’utilisateur actuel et le destinataire.

---

### **5. Ajouter la logique de validation**
1. Ajoutez des vérifications dans vos handlers :
   - Validez les données reçues (ex. : utilisateur existe-t-il ?).
   - Gérez les erreurs avec des réponses JSON claires.

---

### **6. Configurer et démarrer le serveur**
1. Dans `main.go` :
   - Chargez les routes avec `routes.SetupRouter()`.
   - Démarrez le serveur sur un port spécifique.

---

### **7. Tester l’API**
1. Utilisez **Postman** ou **cURL** pour tester les fonctionnalités :
   - Inscription d’un utilisateur.
   - Connexion.
   - Envoi de messages entre deux utilisateurs.
   - Récupération des conversations.

---

### **Étapes supplémentaires possibles**
1. **Persistance des données** : Passez d'une base en mémoire à SQLite ou PostgreSQL.
2. **Authentification JWT** : Ajoutez des jetons JWT pour sécuriser les endpoints.
3. **WebSocket** : Transformez la messagerie en temps réel avec WebSocket.

