### **Initiation au Développement Web avec Gin**

### **Pré-requis :**  
- Installer Gin :  
  ```bash
  go get -u github.com/gin-gonic/gin
  ```

---

## **Chapitre 1 : Premiers pas avec Gin**

### **Exercice 1 : Configuration de base**  
- Implémentez une application simple :  
  - Configurez un serveur Gin avec une route GET `/ping`.  
  - La route doit retourner la réponse JSON suivante :  
    ```json
    {"message": "pong"}
    ```
    (avouez que la blague est drôle)
---

### **Exercice 2 : Paramètres dynamiques**  
- Ajoutez une route GET `/hello/:name`.  
  - La route doit retourner une salutation personnalisée en JSON :  
    ```json
    {"message": "Hello, <name>!"}
    ```  
  - Remplacez `<name>` par le paramètre passé dans l'URL.  

---

### **Exercice 3 : Query Parameters**  
- Ajoutez une route GET `/sum`.  
  - Cette route accepte deux paramètres de requête `a` et `b` (entiers).  
  - Retourne la somme des deux nombres en JSON, ou une erreur si l'un des paramètres est manquant.  

**Exemple :**  
Requête : `/sum?a=10&b=5`  
Réponse :  
```json
{"result": 15}
```

---

## **Chapitre 2 : Sérialisation et gestion des données**

### **Exercice 4 : Création d’un utilisateur**  
- Implémentez une route POST `/users` :  
  - Cette route reçoit un JSON avec les champs `name` et `email`.  
  - Retourne un objet `User` créé avec un ID unique et un message de succès.  

**Exemple de requête :**  
```json
{
  "name": "Alice",
  "email": "alice@example.com"
}
```  

**Exemple de réponse :**  
```json
{
  "id": 1,
  "name": "Alice",
  "email": "alice@example.com",
  "message": "User created successfully"
}
```

---

### **Exercice 5 : Liste des utilisateurs**  
- Implémentez une route GET `/users`.  
  - Retourne la liste des utilisateurs créés sous forme de tableau JSON.  

---

### **Exercice 6 : Récupération d’un utilisateur par ID**  
- Ajoutez une route GET `/users/:id`.  
  - Retourne l'utilisateur correspondant à l’ID fourni.  
  - Si l’utilisateur n’existe pas, retournez une erreur 404 avec un message JSON :  
    ```json
    {"error": "User not found"}
    ```

---

## **Chapitre 3 : Gestion avancée des routes**

### **Exercice 7 : Mise à jour d’un utilisateur**  
- Implémentez une route PUT `/users/:id`.  
  - Permet de modifier les champs `name` et `email` d’un utilisateur existant.  
  - Retourne les données mises à jour ou une erreur si l’utilisateur n’existe pas.  

---

### **Exercice 8 : Suppression d’un utilisateur**  
- Ajoutez une route DELETE `/users/:id`.  
  - Supprime l’utilisateur correspondant à l’ID fourni.  
  - Retourne un message de confirmation ou une erreur si l’utilisateur n’existe pas.  

**Exemple de réponse :**  
```json
{"message": "User deleted successfully"}
```

---

## **Chapitre 4 : Middlewares et erreurs**

### **Exercice 9 : Middleware de journalisation**  
- Ajoutez un middleware qui affiche dans la console les informations suivantes pour chaque requête :  
  - Méthode HTTP (GET, POST, etc.).  
  - Chemin de la route.  
  - Code de statut de la réponse.  

---

### **Exercice 10 : Validation des données**  
- Mettez à jour la route POST `/users` :  
  - Retournez une erreur 400 si les champs `name` ou `email` sont manquants.  
  - Le message d'erreur doit être clair, comme :  
    ```json
    {"error": "Name and email are required"}
    ```

---

## **Chapitre 5 : Cas pratiques**

### **Exercice 11 : Gestion d’un système de tâches**  
- Implémentez un système CRUD pour des tâches (`Task`) avec les routes suivantes :  
  - POST `/tasks` : Crée une tâche.  
  - GET `/tasks` : Liste toutes les tâches.  
  - GET `/tasks/:id` : Récupère une tâche par ID.  
  - PUT `/tasks/:id` : Met à jour une tâche.  
  - DELETE `/tasks/:id` : Supprime une tâche.  

Chaque tâche doit avoir les champs :  
```go
type Task struct {
    ID       int    `json:"id"`
    Title    string `json:"title"`
    Done     bool   `json:"done"`
}
```

---

### **Exercice 12 : Déploiement et test final**  
- Configurez une route GET `/health` pour vérifier si le serveur fonctionne correctement :  
  - Retourne :  
    ```json
    {"status": "OK"}
    ```  
- Déployez l’application localement et testez toutes les routes avec **Postman** ou **cURL**.  

---
