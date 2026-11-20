# G2 Réussite — projet Netlify

Cette version est un **prototype de départ**, pas encore l'application complète du programme de Seconde G2.

## Contenu
- `index.html` : interface de l'application et fiches introductives.
- `manifest.webmanifest` et `sw.js` : installation PWA et cache de base.
- `netlify/functions/assistant.mjs` : fonction serveur qui appelle l'API OpenAI.
- `netlify.toml` : configuration Netlify.

## Déploiement
1. Importer ce dépôt GitHub dans Netlify.
2. Dans Netlify, ouvrir Site configuration / Project configuration > Environment variables.
3. Ajouter `OPENAI_API_KEY` avec la clé API fournie et gérée par un parent/tuteur.
4. Ajouter `G2_ACCESS_CODE` avec un code secret long choisi par le responsable et communiqué uniquement aux utilisateurs autorisés.
5. Redéployer le site après l'ajout des variables.

Ne jamais écrire la clé API dans `index.html`, GitHub, un fichier public ou une conversation.

## Sécurité et coûts
Le code d'accès partagé constitue une protection élémentaire, pas une authentification forte. Avant une diffusion publique, le responsable doit ajouter une authentification individuelle et une limitation de débit côté serveur, surveiller l'utilisation et configurer les limites/alertes de dépenses OpenAI. Un code partagé peut circuler. Ne pas rendre le site public avec l'API activée sans ces protections.

L'API OpenAI est facturée séparément de l'abonnement ChatGPT. Un parent/tuteur doit gérer le compte, le paiement et les limites de dépenses.

## Limites actuelles
- Les matières sont des fiches de départ, pas les 13 leçons complètes de comptabilité ni un programme complet.
- L'assistant nécessite une clé API et les variables Netlify ci-dessus.
- L'assistant accepte une image ou un PDF de taille limitée.
- Le cache hors connexion est basique : ouvrir une première fois le site avec Internet avant de tenter le mode hors connexion.
