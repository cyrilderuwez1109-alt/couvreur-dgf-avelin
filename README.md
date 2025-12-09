# Déploiement sur Netlify — DGF (Entreprise DEGRANDE)

Ce dépôt contient une version prête à être déployée du site statique `index.html`.

Méthode rapide (Netlify Drop)
1. Ouvre https://app.netlify.com/drop
2. Glisse/dépose le fichier `index.html` (ou un dossier contenant `index.html` et `netlify.toml`).
3. Après le déploiement, Netlify te donnera une adresse du type `your-site-name.netlify.app`.

Ajout du domaine personnalisé `couvreur-dgf-avelin.fr`
1. Dans Netlify → ton site → Site settings → Domain management → Add custom domain.
2. Ajoute `couvreur-dgf-avelin.fr` et `www.couvreur-dgf-avelin.fr`.
3. Si tu veux configurer manuellement les enregistrements DNS, ajoute :
   - A record: @ → 75.2.60.5
   - A record: @ → 99.83.190.102
   - CNAME: www → your-site-name.netlify.app (remplace `your-site-name` par le nom Netlify affiché)
4. Après propagation DNS, Netlify provisionnera automatiquement un certificat HTTPS via Let's Encrypt.

Formulaire de contact
- Le formulaire actuel est simulé (alert). Options simples :
  - Netlify Forms: ajouter l'attribut `netlify` au <form> et déployer.
  - Formspree / Getform: config rapide sans backend.
  - Backend personnalisé: fonction serverless ou endpoint pour envoi d'emails.

Si tu veux que je pousse ces fichiers et ouvre la PR automatiquement, donne l'autorisation explicite (réponds ici "OK pousse et ouvre la PR") — sinon copie/colle les fichiers ci‑dessous et suis la procédure Option A ci‑dessus.
