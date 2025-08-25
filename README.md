🚀 Insight Receipts - Projet Open Source

Bienvenue ! Insight Receipts est une application web conçue pour simplifier la gestion de vos factures. Ce projet est open-source, ce qui signifie que vous pouvez le prendre, le modifier et l'adapter à vos propres besoins.

Ce guide a été spécialement conçu pour vous aider à déployer et à vous approprier ce projet en utilisant la plateforme de développement Lovable.

Notre Stratégie : Comment faire fonctionner ce projet sur Lovable ?
💡 Pourquoi cette méthode ?

La plateforme Lovable est fantastique pour développer rapidement, mais pour l'instant, elle ne permet pas d'importer directement un projet qui existe déjà sur GitHub.

Notre plan est donc simple et efficace :

Nous allons demander à Lovable de créer un nouveau projet vide pour nous.

Ensuite, nous allons remplacer le contenu de ce projet vide par le code de Insight Receipts.

Enfin, nous effectuerons une petite configuration finale pour que tout soit parfaitement fonctionnel.

Suivez les étapes ci-dessous, et votre application sera en ligne en quelques minutes !

✅ Prérequis

Avant de plonger dans le code, assurez-vous d'avoir :

💻 Un terminal avec Git et NPM installés.

🐙 Un compte GitHub.

✨ Un compte Lovable.

Guide de Déploiement : Pas à Pas
Étape 1 : Créer la "Coquille Vide" sur Lovable

L'objectif ici est de laisser Lovable préparer un nouvel espace de travail pour nous sur GitHub.

Connectez-vous à votre compte Lovable et créez un nouveau projet vierge.

Dans l'éditeur, suivez la procédure pour connecter ce projet à votre compte GitHub. Lovable va alors créer un nouveau dépôt sur votre GitHub.

Une fois le dépôt créé, rendez-vous sur sa page GitHub. Cliquez sur le bouton vert <> Code et copiez l'URL HTTPS. Gardez-la précieusement !

✅ Résultat attendu : Vous avez l'URL d'un nouveau dépôt GitHub, prêt à accueillir notre code.

Étape 2 : Télécharger les Projets sur Votre Ordinateur

Maintenant, nous allons rapatrier les deux dépôts (le projet original et votre nouvelle coquille vide) sur votre machine.

code
Bash
download
content_copy
expand_less

# 1. Clonez ce projet (Insight Receipts) dans un dossier nommé "projet_original"
git clone https://github.com/juliengrrb/insight-receipts-opensource.git projet_original

# 2. Clonez votre nouveau dépôt créé par Lovable dans un dossier nommé "nouveau_projet_lovable"
# !!! ATTENTION : REMPLACEZ L'URL CI-DESSOUS PAR CELLE QUE VOUS VENEZ DE COPIER !!!
git clone [URL_DE_VOTRE_NOUVEAU_DEPOT_LOVABLE] nouveau_projet_lovable

✅ Résultat attendu : Vous avez deux dossiers sur votre ordinateur : projet_original et nouveau_projet_lovable.

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
# C'est une étape cruciale pour garantir un démarrage propre.
rm -rf ./* .git

# 3. Copiez tout le contenu du projet original dans le dossier où vous vous trouvez
cp -a ../projet_original/. .

✅ Résultat attendu : Votre dossier nouveau_projet_lovable contient maintenant une copie parfaite du code d'Insight Receipts.

Étape 4 : Envoyer le Code sur Votre GitHub

Votre projet est prêt localement. Envoyons-le maintenant sur votre dépôt GitHub pour que Lovable puisse le voir.

code
Bash
download
content_copy
expand_less
IGNORE_WHEN_COPYING_START
IGNORE_WHEN_COPYING_END
# 1. Initialisez un nouveau dépôt Git propre
git init

# 2. Ajoutez tous les fichiers du projet pour que Git les suive
git add .

# 3. Créez un "commit" : un instantané de votre projet avec un message descriptif
git commit -m "Initialisation du projet avec le code Insight Receipts"

# 4. Liez votre dossier local au dépôt distant sur GitHub
# !!! ATTENTION : REMPLACEZ L'URL CI-DESSOUS PAR CELLE DE VOTRE NOUVEAU DEPOT !!!
git remote add origin [URL_DE_VOTRE_NOUVEAU_DEPOT_LOVABLE]

# 5. Renommez la branche par défaut en "main", le standard actuel
git branch -m master main

# 6. Envoyez tous vos fichiers vers GitHub.
git push -u -f origin main
⚠️ Une note sur git push -f (Force Push)

Nous utilisons l'option -f pour forcer le remplacement du projet vide sur GitHub par notre nouvelle version. C'est une opération sûre et nécessaire uniquement dans ce cas précis, car nous remplaçons un contenu sans historique.

✅ Résultat attendu : Votre dépôt GitHub est maintenant à jour avec tout le code d'Insight Receipts.

Étape 5 : La Touche Finale pour Lovable

Votre code est en ligne, mais Lovable a besoin d'un dernier fichier pour savoir comment installer les dépendances du projet : le fameux package-lock.json.

code
Bash
download
content_copy
expand_less
IGNORE_WHEN_COPYING_START
IGNORE_WHEN_COPYING_END
# 1. Générez le fichier lock. Cette commande lit votre package.json et fait le reste.
npm install

# 2. Ajoutez ce nouveau fichier crucial à Git
git add package-lock.json

# 3. Créez un commit pour enregistrer ce changement
git commit -m "Ajout du fichier package-lock.json pour Lovable"

# 4. Envoyez cette dernière modification sur GitHub
git push origin main
🎉 Mission Accomplie !

Félicitations ! Vous avez terminé la partie technique.

Retournez sur la page de votre projet dans Lovable et rafraîchissez la page. L'application va se construire et se lancer correctement.

ACTION REQUISE : Configurez Vos Clés d'API !

Pour que l'application soit pleinement fonctionnelle, vous devez ajouter vos clés personnelles :

URL et clé publique de Supabase

URL de votre webhook N8N

Rendez-vous dans les paramètres de votre projet sur Lovable et ajoutez ces informations dans la section "Secrets" ou "Variables d'environnement".

Bon développement
