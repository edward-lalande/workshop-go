### **Initiation au GoLang avec Gestion des Erreurs**  

## **Chapitre 1 : Premiers pas avec les fonctions**

### **Exercice 1 : Addition sécurisée**
- Créez une fonction `Add(a int, b int) (int, error)` :  
  - Retourne la somme de `a` et `b`.  
  - Retourne une erreur si l'un des nombres est négatif.  

**Exemple :**
```go
result, err := Add(5, -3)
```

---

### **Exercice 2 : Division avec gestion des erreurs**
- Implémentez une fonction `Divide(a float64, b float64) (float64, error)` :  
  - Retourne le résultat de `a / b`.  
  - Retourne une erreur si `b` est égal à zéro.  

---

### **Exercice 3 : Longueur d’une chaîne**
- Créez une fonction `StringLength(s string) (int, error)` :  
  - Retourne la longueur de la chaîne.  
  - Retourne une erreur si la chaîne est vide.  

---

## **Chapitre 2 : Gestion des erreurs et types personnalisés**

### **Exercice 4 : Vérification d’âge**
- Implémentez une fonction `CheckAge(age int) (bool, error)` :  
  - Retourne `true` si l’âge est supérieur ou égal à 18.  
  - Retourne une erreur si l’âge est négatif.  

---

### **Exercice 5 : Récupération d’un élément dans un tableau**  
- Implémentez une fonction `GetElementAtIndex(arr []int, index int) (int, error)` :  
  - Retourne l’élément à l’index spécifié.  
  - Retourne une erreur si l’index est hors limites.  

---

### **Exercice 6 : Conversion d’un entier en chaîne**  
- Créez une fonction `IntToString(n int) (string, error)` :  
  - Retourne la représentation en chaîne de `n`.  
  - Retourne une erreur si `n` est négatif.  

---

## **Chapitre 3 : Applications pratiques**

### **Exercice 7 : Calcul de la moyenne d’une liste de nombres**  
- Implémentez une fonction `Average(numbers []float64) (float64, error)` :  
  - Retourne la moyenne des nombres donnés.  
  - Retourne une erreur si la liste est vide.  

---

### **Exercice 8 : Vérification d’un mot de passe**  
- Créez une fonction `ValidatePassword(password string) (bool, error)` :  
  - Retourne `true` si le mot de passe a au moins 8 caractères.  
  - Retourne une erreur si le mot de passe contient des espaces.  

---

### **Exercice 9 : Recherche d’une valeur dans un tableau**  
- Implémentez une fonction `FindInArray(arr []string, target string) (int, error)` :  
  - Retourne l’index de la première occurrence de `target`.  
  - Retourne une erreur si `target` n’est pas trouvé.  

---

## **Chapitre 4 : Fonctionnalités avancées**

### **Exercice 10 : Lecture d’un fichier**  
- Implémentez une fonction `ReadFile(filepath string) ([]byte, error)` :  
  - Lit le contenu d’un fichier et le retourne sous forme de tableau d’octets.  
  - Retourne une erreur si le fichier n’existe pas.  

---

### **Exercice 11 : Recherche d’un mot clé dans un fichier**  
- Créez une fonction `SearchInFile(filepath string, keyword string) (bool, error)` :  
  - Retourne `true` si le mot clé est trouvé dans le fichier.  
  - Retourne une erreur si le fichier est vide.  

---
