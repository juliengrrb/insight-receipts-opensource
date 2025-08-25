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


Étape 3 : Remplir la Coquille avec le Bon Code

Il est temps de transférer le code d'Insight Receipts dans votre nouveau projet.

code
Bash
download
content_copy
expand_less
IGNORE_WHEN_COPYING_START
IGNORE_WHEN_COPYING_END
# 1. Entrez dans le dossier de votre nouveau projet
cd nouveau_projet_lovable

# 2. Supprimez absolument TOUT le contenu initial (fichiers et historique Git)
rm -rf ./* .git

# 3. Copiez tout le contenu du projet original dans le dossier où vous vous trouvez
cp -a ../projet_original/. .
Étape 4 : Envoyer le Code sur Votre GitHub

Votre projet est prêt localement. Envoyons-le sur votre dépôt GitHub pour que Lovable puisse le voir.

code
Bash
download
content_copy
expand_less
IGNORE_WHEN_COPYING_START
IGNORE_WHEN_COPYING_END
# 1. Initialisez un nouveau dépôt Git propre
git init

# 2. Ajoutez tous les fichiers du projet
git add .

# 3. Créez un "commit" : un instantané de votre projet
git commit -m "Initialisation du projet avec le code Insight Receipts"

# 4. Liez votre dossier local au dépôt distant sur GitHub
# !!! ATTENTION : REMPLACEZ L'URL CI-DESSOUS PAR CELLE DE VOTRE NOUVEAU DEPOT !!!
git remote add origin [URL_DE_VOTRE_NOUVEAU_DEPOT_LOVABLE]

# 5. Renommez la branche par défaut en "main"
git branch -m master main

# 6. Envoyez tous vos fichiers vers GitHub.
git push -u -f origin main
⚠️ Une note sur git push -f (Force Push)

Nous utilisons l'option -f pour forcer le remplacement du projet vide sur GitHub par notre nouvelle version. C'est une opération sûre et nécessaire uniquement dans ce cas précis.

Étape 5 : La Touche Finale pour Lovable

Lovable a besoin du fichier package-lock.json pour savoir comment installer les dépendances du projet.

code
Bash
download
content_copy
expand_less
IGNORE_WHEN_COPYING_START
IGNORE_WHEN_COPYING_END
# 1. Générez le fichier lock.
npm install

# 2. Ajoutez ce nouveau fichier crucial à Git
git add package-lock.json

# 3. Créez un commit pour enregistrer ce changement
git commit -m "Ajout du fichier package-lock.json pour Lovable"

# 4. Envoyez cette dernière modification sur GitHub
git push origin main
🎉 Mission Accomplie !

Félicitations ! Votre projet est maintenant prêt sur Lovable.

ACTION REQUISE : Configurez Vos Clés d'API !

Pour que l'application soit pleinement fonctionnelle, vous devez ajouter vos clés personnelles. Créez un fichier .env.local à la racine du projet sur Lovable (via les "Secrets") et remplissez-le en vous basant sur le modèle .env.example :

code
Ini
download
content_copy
expand_less
IGNORE_WHEN_COPYING_START
IGNORE_WHEN_COPYING_END
# Clés pour la connexion à Supabase
VITE_SUPABASE_URL=VOTRE_URL_SUPABASE
VITE_SUPABASE_ANON_KEY=VOTRE_CLE_PUBLIQUE_SUPABASE

# Webhook pour les workflows N8N
VITE_N8N_WEBHOOK_URL=VOTRE_URL_WEBHOOK_N8N
🤝 Contribution

Les contributions sont les bienvenues ! Si vous souhaitez améliorer ce projet, n'hésitez pas à forker le dépôt et à soumettre une Pull Request.
