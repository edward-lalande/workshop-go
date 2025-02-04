### **Programmation Orientée Objet en Go**

### **Chapitre 1 : Introduction à la structuration des données**
1. **Créer une structure basique :**
   - Créez une struct appelée `Person` avec les champs `Name` et `Age`.
   - Implémentez une méthode `Introduce` qui renvoie une phrase comme : *"Bonjour, je m'appelle X et j'ai Y ans."*.

2. **Encapsulation :**
   - Ajoutez un champ `password` (non exporté).
   - Implémentez des méthodes pour définir et valider un mot de passe.

---

### **Chapitre 2 : Héritage via la composition**
3. **Ajout de spécialisation :**
   - Créez une struct `Employee` qui "hérite" de `Person` (via la composition).
   - Ajoutez un champ `Position` et une méthode `Work` qui affiche : *"Je travaille en tant que X."*

4. **Polymorphisme de base :**
   - Créez une interface `Worker` avec une méthode `DoWork()`.
   - Faites en sorte que `Employee` implémente cette interface.

---

### **Chapitre 3 : Interfaces et abstractions**
5. **Modélisation d'un système :**
   - Implémentez une interface `Shape` avec une méthode `Area()`.
   - Créez deux structs `Rectangle` et `Circle` qui implémentent `Shape`.

6. **Gérer une collection polymorphe :**
   - Écrivez une fonction qui prend une liste de `Shape` et affiche l'aire de chaque élément.

---

### **Chapitre 4 : Méthodes et constructeurs**
7. **Constructeurs personnalisés :**
   - Implémentez un constructeur pour `Person` qui initialise `Name` et `Age` par défaut.

8. **Méthodes liées aux structs :**
   - Ajoutez une méthode `Birthday` à `Person` qui incrémente l'âge.

---

### **Chapitre 5 : Conception avancée et patterns**
9. **Pattern Factory :**
   - Implémentez une fonction `NewEmployee(name string, position string)` qui retourne un `Employee` avec des champs initialisés.

10. **Pattern Singleton :**
    - Créez une struct `Database` avec un champ `connections` (liste chaînés).
    - Implémentez un singleton pour gérer les connexions à une base de données simulée.

11. **Décorateurs avec composition :**
    - Implémentez un système pour décorer un `Worker` avec des rôles additionnels (par ex., un `Manager` qui ajoute des responsabilités).

---

### **Chapitre 6 : Cas d'application final**
12. **Système complet :**
    - Créez un petit programme simulant une entreprise :
      - Employés spécialisés (`Developer`, `Manager`).
      - Une méthode pour assigner des tâches et afficher les résultats.
      - Une gestion polymorphe des employés à travers une liste.

---
