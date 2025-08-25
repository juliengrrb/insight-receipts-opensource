Je comprends 👍 Là, ton README apparaît comme un **gros bloc de code** au lieu d’un vrai document avec titres, paragraphes et blocs de code séparés.
Le problème vient du fait que tu avais mis ton texte entier **entre balises `markdown ... `**, ce qui le rend monolithique.

👉 La solution : écrire ton README directement en **Markdown brut** (sans le bloquer dans un seul `markdown`), en utilisant des titres (`#`, `##`), du gras (`**texte**`), et des blocs de code uniquement pour les commandes.

Voici la version corrigée et jolie, qui s’affichera correctement sur GitHub :

---

# 🚀 Insight Receipts - Gestionnaire de Factures Open Source

![GitHub Stars](https://img.shields.io/github/stars/juliengrrb/insight-receipts-opensource?style=social)

Bienvenue sur **Insight Receipts**, une application web conçue pour simplifier l'upload, l'analyse et la gestion de vos factures.
Ce projet est **entièrement open-source** : prenez-le, modifiez-le et adaptez-le à vos propres besoins !

---

## ✨ Aperçu de l'Application

<img width="1918" height="990" alt="image" src="https://github.com/user-attachments/assets/11f2806a-d75f-4c38-b0c6-4ed280a20850" />


---

## 📊 Fonctionnalités Principales

* **📈 Tableau de Bord Intuitif :** Visualisez vos dépenses mensuelles, leur répartition par catégorie et l'évolution dans le temps.
* **🧾 Upload Simplifié :** Téléchargez facilement vos factures une par une.
* **🤖 Analyse par IA :** Extraction automatique des informations clés de vos factures.
* **📁 Export des Données :** Exportez vos données de factures pour votre comptabilité.
* **🌙 Thème Clair & Sombre :** Adaptez l'interface à votre préférence.

---

## 🛠️ Stack Technique

* **Frontend :** Vite, React, TypeScript, Tailwind CSS, Shadcn/ui
* **Backend & Base de Données :** Supabase
* **Workflow d'Analyse IA :** n8n
* **Plateforme de Déploiement :** Lovable

---

## 🚀 Guide de Déploiement sur Lovable

Ce guide explique comment déployer votre propre version du projet sur [Lovable](https://lovable.dev).

> 💡 **Pourquoi cette méthode ?**
> Lovable ne permet pas encore d’importer directement un dépôt GitHub existant. On va donc contourner cela facilement !

---

### ✅ Prérequis

* **💻 Terminal** avec **Git** et **NPM** installés
* **🐙 Compte GitHub**
* **✨ Compte Lovable**

---

### Étape 1 : Créer la Coquille Vide sur Lovable

1. Connectez-vous à **Lovable** et créez un **nouveau projet vierge**.
2. Associez-le à GitHub → Lovable crée un **nouveau dépôt**.
3. Copiez l’URL HTTPS de ce dépôt depuis GitHub.

---

### Étape 2 : Cloner les Dépôts

```bash
# Clonez ce projet (Insight Receipts)
git clone https://github.com/juliengrrb/insight-receipts-opensource.git projet_original

# Clonez le dépôt créé par Lovable
git clone [URL_DE_VOTRE_NOUVEAU_DEPOT_LOVABLE] nouveau_projet_lovable
```

---

### Étape 3 : Remplir la Coquille

```bash
cd nouveau_projet_lovable

# Supprimer le contenu initial
rm -rf ./* .git

# Copier le code du projet original
cp -a ../projet_original/. .
```

---

### Étape 4 : Envoyer le Code sur GitHub

```bash
git init
git add .
git commit -m "Initialisation du projet avec Insight Receipts"
git remote add origin [URL_DE_VOTRE_NOUVEAU_DEPOT_LOVABLE]
git branch -m master main
git push -u -f origin main
```

⚠️ `git push -f` force l’envoi → Ici, c’est **normal et sûr** car on remplace un dépôt vide.

---

### Étape 5 : Générer le `package-lock.json`

```bash
npm install
git add package-lock.json
git commit -m "Ajout du package-lock.json pour Lovable"
git push origin main
```

---

## 🔑 Configuration des Clés d’API

Ajoutez vos variables dans `.env.local` (via les *Secrets* de Lovable), en vous basant sur `.env.example` :

```ini
# Supabase
VITE_SUPABASE_URL=VOTRE_URL_SUPABASE
VITE_SUPABASE_ANON_KEY=VOTRE_CLE_PUBLIQUE_SUPABASE

# Webhook n8n
VITE_N8N_WEBHOOK_URL=VOTRE_URL_WEBHOOK_N8N
```

---

## 🤝 Contribution

Les contributions sont **les bienvenues** ! Forkez le dépôt, proposez vos améliorations et soumettez une Pull Request.

---
