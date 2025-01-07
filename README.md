

# Script de connexion automatique

Ce script JavaScript permet d'injecter un token d'authentification dans le stockage local du navigateur (localStorage) pour se connecter automatiquement à une application web.  

## ⚠️ Avertissement

**L'utilisation de ce script peut enfreindre les conditions d'utilisation des services concernés ou être illégale. Assurez-vous d'avoir l'autorisation explicite avant d'utiliser ce script.** L'utilisation abusive de ce code peut entraîner des sanctions. Ce script est présenté à des fins éducatives uniquement.  

---

## 📜 Description

Ce script exécute les étapes suivantes :  
1. Crée une `iframe` et modifie le `localStorage` du navigateur à l'intérieur de cette iframe.  
2. Injecte un token d'authentification dans le `localStorage`.  
3. Recharge automatiquement la page pour appliquer le token et simuler une connexion.

---

## 🛠️ Fonctionnement

Voici le code du script :  

```javascript
let token = "token";

function login(token) {
    setInterval(() => {
      document.body.appendChild(document.createElement `iframe`).contentWindow.localStorage.token = `"${token}"`
    }, 50);
    setTimeout(() => {
      location.reload();
    }, 2500);
  }

login(token);
```

---

## 🚀 Utilisation

1. Remplace `"token"` par ton token d'authentification dans le script.  
2. Copie-colle le script dans la console JavaScript de ton navigateur (accessible via les outils de développement).  
3. Exécute le script.  
4. La page se rechargera automatiquement et le token sera injecté dans le `localStorage`.  

---

## 🔒 Sécurité

- Ce script accède directement au `localStorage` du navigateur, ce qui peut être détecté par certains systèmes de sécurité.
- L'utilisation d'un script d'injection peut être surveillée et signalée par les administrateurs des sites concernés.

---

## 💡 Note

Utilisez ce script avec précaution et uniquement à des fins légitimes. Toute responsabilité liée à l'utilisation de ce code incombe à l'utilisateur.  

--- 
