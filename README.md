# 🚀 Insight Receipts 

Bienvenue sur **Insight Receipts**, une application web conçue pour simplifier l'upload, l'analyse et la gestion de vos factures. Ce projet est entièrement open-source : prenez-le, modifiez-le et adaptez-le à vos propres besoins !

---

### Aperçu de l'Application
*Insérez ici une capture d'écran de votre tableau de bord pour un impact visuel maximal !*
![Aperçu de l'application Insight Receipts](https://i.ibb.co/L5QyL3T/image.png)

## ✨ Fonctionnalités Principales

*   **📊 Tableau de Bord Intuitif :** Visualisez vos dépenses mensuelles, leur répartition par catégorie et l'évolution dans le temps.
*   **🧾 Upload Simplifié :** Téléchargez facilement vos factures une par une.
*   **🤖 Analyse par IA :** Extraction automatique des informations clés de vos factures.
*   **📁 Export des Données :** Exportez vos données de factures pour votre comptabilité.
*   **🌙 Thème Clair & Sombre :** Adaptez l'interface à votre préférence.

## 🛠️ Stack Technique

*   **Frontend :** Vite, React, TypeScript, Tailwind CSS, Shadcn/ui
*   **Backend & Base de Données :** Supabase
*   **Workflow d'Analyse IA :** n8n
*   **Plateforme de Déploiement Ciblée :** Lovable

---

## 🚀 Guide de Déploiement sur Lovable

Ce guide vous explique comment déployer votre propre version de ce projet sur la plateforme [Lovable](https://lovable.dev).

> #### **💡 Pourquoi cette méthode ?**
> La plateforme Lovable est fantastique pour développer rapidement, mais pour l'instant, elle ne permet pas d'importer un projet qui existe déjà sur GitHub. Nous allons donc utiliser une méthode de contournement simple et efficace !

### ✅ Prérequis

Avant de commencer, assurez-vous d'avoir :
*   💻 Un **terminal** avec **Git** et **NPM** installés.
*   🐙 Un compte **GitHub**.
*   ✨ Un compte **Lovable**.

### Étape 1 : Créer la "Coquille Vide" sur Lovable

L'objectif ici est de laisser Lovable préparer un nouvel espace de travail pour nous sur GitHub.

1.  Connectez-vous à **Lovable** et créez un **nouveau projet vierge**.
2.  Dans l'éditeur, suivez la procédure pour **connecter ce projet à votre compte GitHub**. Lovable va alors créer un **nouveau dépôt** pour vous.
3.  Une fois le dépôt créé, rendez-vous sur sa page GitHub. Cliquez sur le bouton vert **`<> Code`** et **copiez l'URL HTTPS**.

### Étape 2 : Cloner les Dépôts

Ouvrez votre terminal et téléchargez une copie locale des deux dépôts.

```bash
# 1. Clonez ce projet (Insight Receipts)
git clone https://github.com/juliengrrb/insight-receipts-opensource.git projet_original

# 2. Clonez votre nouveau dépôt créé par Lovable
# !!! ATTENTION : REMPLACEZ L'URL CI-DESSOUS PAR CELLE QUE VOUS VENEZ DE COPIER !!!
git clone [URL_DE_VOTRE_NOUVEAU_DEPOT_LOVABLE] nouveau_projet_lovable
