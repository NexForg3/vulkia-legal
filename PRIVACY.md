# Politique de confidentialité — Vulkia

*Dernière mise à jour : 13 novembre 2026 (adresse confirmée par un lien à la création du compte, lien de mot de passe oublié, suppression des données depuis Moi → Vulkia Premium)*

Vulkia est une application de suivi de musculation. Ton carnet d'entraînement fonctionne **sans compte** : tes données
restent sur ton téléphone. Le coach IA et l'abonnement **Vulkia Premium** passent par le **service Vulkia**, hébergé
chez Cloudflare, avec un **compte pseudonyme** : un identifiant aléatoire, sans nom, sans e-mail, sans numéro de
téléphone. Pour **t'abonner**, tu relies ce compte à ton **compte Google** ou à ton **adresse e-mail** (voir *Compte
Vulkia avec e-mail ou Google*). Une version de l'app sans service Vulkia (par exemple la version web de test) n'envoie
rien.

## Responsable du traitement
Le responsable du traitement des données décrites ici est l'éditeur de Vulkia : **NexForg3**, société par actions
simplifiée unipersonnelle (SASU) en cours d'immatriculation, joignable à **NexForg3@gmail.com**.

## Données stockées sur ton téléphone
Toutes tes données (séances, routines, salles de sport, mensurations, exercices personnalisés, réglages,
conversations avec le coach) sont enregistrées **sur ton téléphone**, et nulle part ailleurs tant que tu n'as pas de
compte Vulkia (avec un compte, elles passent par la *Synchronisation chiffrée*, voir plus bas). Tu peux les exporter (*Réglages →
Données → Exporter une sauvegarde*) et les supprimer à tout moment (*Réglages → Données → Effacer toutes les données*,
ou en désinstallant l'application). L'app y garde aussi le jeton de ton compte Vulkia (dans le stockage sécurisé du
téléphone) et le dernier état connu de ton abonnement et de tes quotas, pour l'affichage.

## Blessures et maladies (Santé & blessures)
Les blessures et maladies que tu déclares (zone, type, douleurs, symptômes, température, notes) servent uniquement à
adapter tes séances sur l'appareil. Elles **restent sur ton téléphone** : elles ne sont envoyées ni à Health Connect /
Apple Santé ni, en clair, à aucun serveur, et ne sont incluses que dans tes propres sauvegardes (export manuel, ou
sauvegarde automatique dans le dossier que tu as choisi) et, avec un compte Vulkia, dans la *Synchronisation chiffrée*,
où elles ne sont stockées que chiffrées. Un résumé sans tes notes n'accompagne tes demandes au coach IA
**qu'avec ton accord explicite** (voir *Coach IA* ci-dessous). Vulkia adapte ton entraînement, il ne remplace pas un
avis médical.

## Ton compte Vulkia (pseudonyme)
Au premier lancement, l'app obtient du service Vulkia un **compte pseudonyme** : un identifiant aléatoire, lié à
l'identifiant aléatoire de ton installation, sans nom ni e-mail. Ces identifiants ne disent pas qui tu es, mais ils
relient entre elles les données décrites ici : ce sont des données personnelles pseudonymes. Le compte sert à
appliquer ton offre (gratuite, essai ou Premium) et tes quotas du coach IA, et à rattacher ton abonnement. Le serveur
garde cet identifiant, celui de l'installation, la plateforme (Android, iOS), les dates de création et de dernière
visite et, si tu as restauré ton abonnement sur un autre appareil, le lien entre les comptes qui le partagent. **Ton
adresse IP n'est pas enregistrée** : seule une empreinte chiffrée, gardée 2 jours, sert à limiter le nombre de comptes
créés depuis un même réseau.

## Compte Vulkia avec e-mail ou Google
Un abonnement demande un **compte Vulkia relié à ton compte Google ou à ton e-mail** : tu retrouves ainsi ton
abonnement et ton quota du coach IA sur un autre téléphone. C'est facultatif pour tout le reste de l'app.
- **Avec ton e-mail** : le serveur garde ton adresse e-mail et une **empreinte de ton mot de passe** (PBKDF2-SHA256,
  avec un sel aléatoire) — jamais le mot de passe lui-même. Vulkia t'envoie un e-mail seulement quand tu le demandes :
  un **lien** pour confirmer ton adresse à la création du compte (le compte n'existe qu'une fois le lien ouvert et ton
  mot de passe choisi ; sinon l'adresse n'est gardée que 24 heures, le temps de la validité du lien), un lien pour
  choisir un nouveau mot de passe (*Mot de passe oublié*, 30 minutes) ou un code à 6 chiffres pour la validation en
  deux étapes (10 à 15 minutes). Liens et codes ne sont gardés que sous forme d'empreinte et ne servent qu'une fois. Le
  lien passe par une page de nexforg3.fr qui ouvre l'app : la partie du lien qui le rend unique n'est jamais envoyée au
  serveur du site.
- **Validation en deux étapes** (facultative, connexion par e-mail) : un code à chaque connexion, envoyé par e-mail ou
  affiché par ton application d'authentification. Pour cette dernière, le serveur garde la clé partagée avec
  l'application, chiffrée (AES-256-GCM).
- **Avec Google** (« Continuer avec Google », Android) : Google confirme ton identité à Vulkia et lui transmet
  l'**identifiant de ton compte Google**, ton **adresse e-mail** et le fait qu'il l'a vérifiée. Vulkia ne reçoit ni ton
  mot de passe Google, ni tes contacts, ni rien d'autre de ton compte Google.

Le serveur garde aussi les dates de création et de dernière connexion. Pour bloquer les essais de mots de passe, il
compte les **échecs de connexion** par heure, sous une empreinte chiffrée de l'adresse essayée et du réseau (ni
l'adresse ni l'adresse IP en clair), effacée au bout d'un à deux jours. Se déconnecter laisse le compte intact ; ton
téléphone reprend alors un compte pseudonyme, avec les mêmes compteurs d'utilisation du coach IA. Supprimer tes données
du serveur efface aussi tes identifiants de connexion. L'éditeur peut offrir l'accès Premium à certains comptes
(éditeur, testeurs) d'après leur adresse e-mail vérifiée par Google ou leur identifiant de compte.

## Données reçues de Google (« Continuer avec Google »)
Cette section décrit l'usage des données que Vulkia reçoit des services d'API Google quand tu choisis de te connecter
avec ton compte Google.
- **Données consultées** : l'**identifiant de ton compte Google**, ton **adresse e-mail** et l'information que Google
  l'a vérifiée (champs d'application `openid` et `email`). Le jeton d'identité remis par Google peut aussi contenir ton
  nom et ta photo de profil : Vulkia ne les lit pas et ne les enregistre pas. Vulkia ne demande accès ni à ton Gmail,
  ni à ton Drive, ni à tes contacts, ni à ton agenda, ni à aucune autre donnée de ton compte Google, et ne reçoit
  jamais ton mot de passe Google.
- **Utilisation** : uniquement pour créer ton compte Vulkia et t'y connecter, retrouver sur un autre téléphone ton
  abonnement, ton quota du coach IA et tes données synchronisées, t'identifier si tu nous écris, et, pour une adresse
  vérifiée figurant sur la liste de l'éditeur (éditeur, testeurs), offrir l'accès Premium. Ces données ne servent
  **jamais** à la publicité (ciblée, personnalisée, de reciblage ou par centres d'intérêt), au profilage, à la
  constitution de bases de données, à l'évaluation de la solvabilité ou à des fins de prêt, ni à développer, améliorer
  ou entraîner des modèles d'IA ou d'apprentissage automatique.
- **Partage** : ces données ne sont **ni vendues, ni louées, ni partagées**, ni transmises à des courtiers en données ou à
  des revendeurs d'informations ; seuls y accèdent l'hébergeur du service Vulkia (Cloudflare, sous-traitant, qui les
  stocke pour l'éditeur) et, si la loi l'impose, les autorités compétentes.
- **Stockage et protection** : sur le serveur Vulkia chez Cloudflare (base D1, chiffrée au repos par l'hébergeur),
  transmises uniquement par des connexions chiffrées (HTTPS) et des requêtes signées par l'app ; des procédures de
  sécurité protègent leur confidentialité (accès réservé à l'éditeur, secrets du service séparés de la base, limitation
  des tentatives de connexion).
- **Conservation et suppression** : tant que ton compte existe, pour te permettre de t'y connecter ; elles sont
  effacées dès que tu supprimes ton compte depuis l'app (*Moi → Vulkia Premium → Supprimer mes données du serveur*) ou
  dans le mois qui suit ta demande à **NexForg3@gmail.com**. Tu peux
  aussi retirer à tout moment l'accès de Vulkia à ton compte Google sur
  [myaccount.google.com/permissions](https://myaccount.google.com/permissions).
- **Utilisation limitée** : l'utilisation et le transfert vers toute autre application des informations reçues des API
  Google par Vulkia respectent les [Règles relatives aux données utilisateur des services d'API
  Google](https://developers.google.com/terms/api-services-user-data-policy?hl=fr), y compris les exigences
  d'utilisation limitée.

## Synchronisation chiffrée (avec un compte)
Avec un compte Vulkia relié à Google ou à ton e-mail, tes séances, routines et dossiers, salles, mensurations, exercices
personnalisés, conversations avec le coach, blessures et maladies (avec leurs notes), photos de progression (images
comprises) et réglages sont **chiffrés sur ton téléphone** (XChaCha20-Poly1305, clé aléatoire de 256 bits propre à ton
compte) avant d'être envoyés au service Vulkia, qui les stocke chez Cloudflare (D1 et R2) pour tes autres téléphones :
tu les retrouves en te connectant à ton compte, sans code à retenir.

La clé de ton compte est gardée par le service Vulkia, elle-même chiffrée (AES-256-GCM) par une clé secrète du
service, distincte de la base de données ; elle n'est remise qu'à un téléphone connecté à ton compte. La base de
données ne contient donc que des blocs chiffrés : une personne qui la volerait ne pourrait pas les lire. Ce n'est en
revanche **pas** un chiffrement de bout en bout : l'éditeur, qui administre le service et sa clé secrète, a
techniquement les moyens de déchiffrer ces données. Il s'interdit de le faire, sauf obligation légale. Le serveur voit
aussi le nombre de blocs, leur taille et leurs dates d'envoi, rattachés à ton compte.

La synchronisation fait partie du compte Vulkia : elle s'active d'elle-même quand tu crées ton compte ou t'y
connectes, ce que l'écran de création du compte annonce avant que tu le fasses. Créer ou connecter ce compte est donc
ton choix explicite, y compris pour tes informations de santé (blessures, maladies, photos) : base légale, ton
consentement explicite (article 9.2.a du RGPD) et l'exécution du service demandé. Tu le retires à tout moment : la
déconnexion du compte cesse les envois de ce téléphone, et *Supprimer mes données du serveur* efface les données
synchronisées avec ton compte.

## Coach IA
Quand tu utilises le coach IA (création de séance ou de programme, discussion), l'app envoie au service Vulkia ta
demande et le contexte nécessaire : profil d'entraînement, résumé de tes séances et records, matériel de tes salles.
**Jamais ton nom.** La demande est envoyée avec ton compte. Le modèle d'IA (Cloudflare Workers AI) la traite sans la
conserver ni l'utiliser pour s'entraîner.

**Tes informations de santé ne partent qu'avec ton accord explicite** : un résumé de tes blessures et maladies
déclarées (zone, type, phase, douleur, symptômes, sans tes notes) et les douleurs ou zones à ménager indiquées dans
une demande de séance. L'app te le demande avant la première demande qui en contiendrait ; tu peux donner ou retirer
cet accord à tout moment dans *Réglages → Données → Confidentialité*. Sans accord, le coach répond sans ces
informations et l'app adapte quand même tes séances à tes blessures, sur ton téléphone. Ce que tu écris toi-même dans
la discussion est envoyé tel quel : n'y mets que ce que tu veux partager.

Le serveur **ne garde pas le texte** de tes demandes ni des réponses, à une exception près : une copie des séances et
programmes générés est gardée **15 minutes**, pour te les renvoyer si la connexion a coupé pendant la réponse (jamais
la discussion). Il garde en revanche :
- des **compteurs** de messages, de séances et de programmes utilisés, et du coût de l'IA, par jour, par mois et, pour
  la séance découverte, au total ;
- un **journal technique** de chaque demande, sans texte : type (message, séance, programme), offre, statut, modèle
  utilisé, nombre de tokens, coût, dates.

Les clés API des anciennes versions sont supprimées de ton téléphone.

## Conseil du coach IA (remplacement d'un exercice)
Quand tu touches **« Conseil du coach IA »** (pour remplacer un exercice), l'app envoie au service Vulkia :
l'exercice, les exercices équivalents possibles, ton objectif d'entraînement, la langue et, si une blessure concerne
cet exercice **et que tu as donné ton accord** (voir *Coach IA*), sa zone et son niveau de douleur (léger ou modéré).
**Jamais ton nom, tes notes ni ton historique** ; sans ton accord, ou pour une douleur forte (7/10 ou plus), le
conseil lié à une douleur est calculé sur ton téléphone et rien n'est envoyé. La demande porte l'**identifiant aléatoire de ton
installation** et, quand l'app l'a déjà, le jeton de ton compte : ils servent à limiter le nombre de demandes et le
coût de l'IA (en essai ou Premium, ce coût est compté sur ton compte, sinon sur ton installation) : compteurs du jour
gardés 7 jours, compteur de coût du mois 13 mois, journal technique sans texte 35 jours. La réponse est gardée en
cache 60 jours **sans ces identifiants**, pour être resservie à quelqu'un qui fait la même demande. Le modèle d'IA
(Cloudflare Workers AI) n'utilise pas ces données pour s'entraîner. Sans réseau, ou quand le quota du jour est
atteint, le conseil est calculé sur ton téléphone et rien n'est envoyé.

## Abonnement Vulkia Premium
Les achats se font dans **Google Play** ou l'**App Store** : la boutique ne transmet jamais à Vulkia ton moyen de
paiement, ton nom ni ton e-mail. Pour gérer les abonnements, l'app utilise le service **RevenueCat**, qui traite l'historique de tes achats
dans l'app transmis par la boutique et le relie à l'identifiant de ton compte Vulkia
([politique de confidentialité de RevenueCat](https://www.revenuecat.com/privacy)). RevenueCat informe le service
Vulkia de chaque changement. Le serveur Vulkia garde l'**état de ton abonnement** (produit, boutique, période d'essai
ou non, achat réel ou de test, dates d'achat et de fin, renouvellement, période de grâce) et un journal de ces
notifications (identifiant et type de l'événement, identifiant de ton compte, dates) pendant 90 jours. Ton offre est
déduite de cet état vérifié, jamais d'une information envoyée par ton téléphone.

« Restaurer mes achats » rattache ton abonnement au compte de l'appareil utilisé ; le serveur enregistre alors que ce
compte et celui qui avait l'abonnement le **partagent** : Premium reste actif sur chacun de ces appareils, avec les
mêmes quotas, y compris quand tu supprimes les données du serveur sur l'un d'eux. Après « Supprimer mes données du
serveur », l'app demande à RevenueCat de rattacher ton abonnement en cours à ton nouveau compte (synchronisation des
achats de la boutique).

## Statistiques d'usage
Pour savoir si Premium intéresse, l'app envoie quelques **compteurs d'événements** : paywall affiché ou fermé, achat
commencé, réussi, annulé, en attente ou échoué, restauration, limite du coach atteinte ou refus du serveur, premier
résultat du coach IA, choix du moteur intégré, écran Abonnement ouvert, fonction Premium affichée, avec l'écran
d'origine choisi dans une liste fixe (par exemple « discussion » ou « bilan de la semaine »). Le serveur n'en garde
que des **totaux par jour** (jour, événement, écran, offre, plateforme, nombre), **sans identifiant** de compte ni
d'appareil et sans texte, pendant 400 jours. L'identifiant de l'installation sert seulement à limiter le nombre
d'événements acceptés par jour (compteur gardé 8 jours).

## Supprimer tes données du serveur
*Moi → Vulkia Premium → Supprimer mes données du serveur* efface du serveur ton compte (ses identifiants, la
plateforme, les dates, ton adresse e-mail, l'identifiant Google et l'empreinte du mot de passe s'il y en a), tes données synchronisées (chiffrées) et la clé de ton compte, tes réglages de validation en deux étapes et tes codes en cours, l'état de ton abonnement enregistré par Vulkia et le journal technique de tes demandes
terminées : celles faites avec ce compte (y compris celles comptées sur le compte que partagent tes appareils) et
celles faites par ton installation sans compte. **Cela ne résilie pas ton abonnement** : gère-le dans Google Play ou
l'App Store ; s'il est en cours, l'app le rattache à ton nouveau compte.

Si d'autres appareils partagent ton abonnement et que c'est le compte de cet appareil qui le détient (le dernier à
l'avoir restauré), l'effacer couperait Premium sur les autres. Le serveur en garde alors, pour eux, une trace réduite
au minimum : un **identifiant opaque** (sans lien avec ton installation ni ton appareil), ses dates de création et de
suppression, son **lien avec le groupe** de tes appareils et l'**état de l'abonnement**, jusqu'à ce que cet abonnement
ne donne plus accès depuis 30 jours (puis tout est effacé). Ce compte ne sert plus à rien d'autre : aucune
installation ne le retrouve et sa session est refusée (exécution du contrat : garder ton abonnement sur tes autres
appareils).

**Tes compteurs d'utilisation du coach IA ne sont pas remis à zéro** (messages, séances et programmes utilisés, coût
de l'IA, séance découverte) : sinon, supprimer ses données suffirait pour obtenir de nouveau la séance découverte ou
l'enveloppe du mois (intérêt légitime : prévenir les abus). Ils sont gardés sous une **empreinte** de l'identifiant de
l'installation qui demande la suppression (et de celle qui avait créé le compte, si c'en est une autre), calculée avec
une clé secrète du serveur (l'identifiant ne peut pas être retrouvé à partir d'elle), et le prochain compte créé sur
cette installation les reprend. Ils sont conservés comme les autres compteurs (jour 8 jours, mois 13 mois) ; le
compteur « au total » est effacé après 400 jours sans utilisation de l'installation. Si d'autres appareils partagent
ton abonnement, ces compteurs restent aussi avec leur compte.

Restent aussi jusqu'à la fin de leur durée de conservation : les demandes encore en cours au moment de la suppression
et celles des autres appareils qui partagent ton abonnement (journal technique, 35 jours), les compteurs liés à ton
installation (conseil de remplacement, statistiques), le journal des notifications d'abonnement (90 jours),
l'empreinte d'adresse IP (2 jours) et les totaux sans identifiant. Les notifications de la boutique qui arrivent
ensuite pour le compte supprimé ne recréent rien ; celles d'un abonnement partagé mettent à jour l'état gardé dans sa
trace. Pour effacer aussi tes données d'achat chez RevenueCat, écris-nous (voir *Contact*) ; la boutique garde
ses propres données selon sa politique. Désinstaller l'app efface les données du téléphone, pas celles du serveur :
supprime-les d'abord depuis l'app.

## Durées de conservation (serveur Vulkia)

| Donnée | Durée |
|---|---|
| Compte (identifiants aléatoires, plateforme, dates, lien avec les comptes qui partagent ton abonnement) | jusqu'à ce que tu le supprimes depuis l'app |
| Identifiants de connexion (adresse e-mail, identifiant Google, empreinte du mot de passe, dates) | jusqu'à ce que tu supprimes ton compte depuis l'app |
| Données synchronisées (blocs chiffrés sur ton téléphone, clé du compte gardée chiffrée par le service) | jusqu'à ce que tu supprimes tes données du serveur |
| État de ton abonnement | jusqu'à la suppression |
| Trace du compte supprimé d'un appareil qui détenait un abonnement partagé (identifiant opaque, dates de création et de suppression, lien avec le groupe, état de l'abonnement) | jusqu'à 30 jours après la fin de cet abonnement |
| Compteurs du jour (coach, conseil, statistiques) | 8 jours |
| Compteurs du mois (unités et coût de l'IA) | 13 mois, y compris après la suppression du compte |
| Compteur de la séance découverte (« au total ») | tant que le compte existe ; après sa suppression, jusqu'à sa reprise par le prochain compte de l'installation, ou 400 jours sans utilisation ; celui d'une installation qui utilise le coach sans compte : 400 jours sans utilisation |
| Journal technique des demandes à l'IA (sans texte) | 35 jours |
| Copie d'une séance ou d'un programme générés | servie 15 minutes, puis effacée (au plus tard au nettoyage quotidien) |
| Empreinte d'adresse IP (création de comptes) | 2 jours |
| Compteurs d'échecs de connexion (empreintes de l'adresse essayée et du réseau) | 1 à 2 jours |
| Codes envoyés par e-mail (empreinte seulement) | 10 à 30 minutes, effacés au plus tard le lendemain |
| Réglage de la validation en deux étapes (méthode, clé de l'application d'authentification chiffrée) | jusqu'à ce que tu la désactives ou supprimes ton compte |
| Journal des notifications d'abonnement | 90 jours |
| Compteurs quotidiens du conseil de remplacement | 7 jours |
| Réponses du conseil en cache (sans identifiant) | 60 jours |
| Statistiques d'usage (totaux sans identifiant) | 400 jours |

## Bases légales

| Traitement | Base légale |
|---|---|
| Compte (et sa connexion par e-mail ou Google), offre et quotas, coach IA et conseil de remplacement à ta demande, abonnement (état vérifié, RevenueCat, appareils qui le partagent, trace gardée pour eux après une suppression) | exécution du contrat : les conditions d'utilisation et d'abonnement (article 6.1.b du RGPD) |
| Informations de santé jointes à une demande (résumé des blessures et maladies, douleurs indiquées, niveau de douleur) | ton consentement explicite (article 9.2.a du RGPD), demandé dans l'app avant le premier envoi et retirable à tout moment dans *Réglages → Données → Confidentialité* ; le retrait vaut pour les demandes suivantes |
| Limites contre les abus (empreinte d'adresse IP, compteurs d'échecs de connexion, quotas par installation, compteurs gardés après une suppression) et sécurité du service (signatures, journal technique) | intérêt légitime de l'éditeur : protéger le service, son budget et l'offre gratuite contre le contournement des limites (article 6.1.f) |
| Statistiques d'usage (totaux sans identifiant) | intérêt légitime de l'éditeur : savoir si l'offre intéresse et l'améliorer (article 6.1.f) |
| Health Connect / Apple Santé | ton consentement, donné et retiré dans les autorisations du système |

## Prestataires

| Prestataire | Rôle | Données | Pays |
|---|---|---|---|
| Cloudflare, Inc. (Workers, D1, R2, Workers AI) | héberge le service Vulkia et exécute les modèles d'IA | demandes au coach et au conseil, compte, compteurs, journal technique ; données synchronisées, chiffrées (illisibles pour lui sans la clé secrète du service) | États-Unis (réseau mondial) |
| RevenueCat, Inc. | gestion des abonnements | identifiant du compte, historique des achats dans l'app | États-Unis |
| Google Play, Apple App Store | paiement et facturation, sous leur propre responsabilité | selon leurs propres politiques (ton compte Google ou Apple) | — |
| Service d'envoi d'e-mails choisi par l'éditeur : Gmail (Google LLC, depuis le compte Gmail de l'éditeur), Brevo SAS ou Resend, Inc. | envoie les codes de réinitialisation et de validation | ton adresse e-mail et le code envoyé | États-Unis (Google, Resend) ou Union européenne (Brevo) |
| Google (connexion avec Google, si tu la choisis) | confirme ton identité, sous sa propre responsabilité ([règles de confidentialité de Google](https://policies.google.com/privacy)) | il transmet à Vulkia l'identifiant de ton compte Google et ton adresse e-mail | — |

Si d'autres prestataires d'IA étaient utilisés, cette politique serait mise à jour avant.

## Transferts hors de l'Union européenne
Cloudflare, Inc. et RevenueCat, Inc. sont établis aux États-Unis : tes données peuvent y être traitées. Ces transferts
sont encadrés par les garanties du RGPD : Cloudflare est certifié au cadre de protection des données UE–États-Unis
(*EU-U.S. Data Privacy Framework*) et son contrat de sous-traitance comprend aussi les clauses contractuelles types de
la Commission européenne ; le contrat de sous-traitance de RevenueCat repose sur ces clauses contractuelles types. Tu
peux en obtenir une copie auprès de l'éditeur.

## Health Connect / Apple Santé (optionnel)
Avec ton autorisation explicite (chaque type de donnée peut être refusé séparément), Vulkia peut :
- **écrire** tes séances d'entraînement (type, durée), les **calories actives** estimées de chaque séance, et les
  pesées que tu saisis dans l'app (**poids**, **masse grasse**, **masse maigre**), pour que tes autres applications
  santé en profitent ;
- **lire** ton **poids**, ta **taille**, ta **masse grasse**, ta **masse maigre**, ta **masse osseuse**, ton **eau
  corporelle** et ton **métabolisme de base**, enregistrés par ta balance connectée ou d'autres applications, pour
  afficher ta composition corporelle, calculer ton IMC / FFMI et suivre ta progression dans l'écran *Corps*.

Ces données ne sont utilisées que pour ces fonctionnalités, restent sur l'appareil et ne sont ni vendues, ni
partagées, ni utilisées à des fins publicitaires. Tu peux retirer l'autorisation à tout moment dans Health Connect
ou Apple Santé.

## Vidéos de démonstration (YouTube)
Quand tu touches **Vidéo** sur un exercice, l'app ouvre le lecteur YouTube **dans l'app**, depuis le domaine à
confidentialité renforcée `youtube-nocookie.com`. Google (YouTube) reçoit alors ton adresse IP et des informations
techniques sur ton appareil, et peut enregistrer des données sur ton téléphone pendant la lecture, sous sa propre
responsabilité ([règles de confidentialité de Google](https://policies.google.com/privacy)). La vidéo peut contenir des
publicités ajoutées par YouTube. Vulkia ne lui transmet ni ton compte, ni tes séances, et rien n'est chargé tant que tu
n'ouvres pas une vidéo.

## Ce que Vulkia ne fait pas
Aucune publicité, aucun traceur publicitaire, aucune revente de données. Aucun nom demandé ; ton e-mail seulement si
tu crées un compte pour t'abonner, et jamais pour de la prospection. Les statistiques d'usage sont des totaux sans
identifiant.

## Notifications
Les notifications (fin du temps de repos, séance IA prête) sont locales et générées par l'application.

## Tes droits
Tu disposes d'un droit d'accès, de rectification, d'effacement, de limitation du traitement, à la portabilité de tes
données et d'opposition aux traitements fondés sur l'intérêt légitime ; tu peux retirer à tout moment un
consentement donné (le partage de ta santé avec le coach IA dans *Réglages → Données → Confidentialité*, les
autorisations Health Connect / Apple Santé) et définir des directives sur le sort
de tes données après ton décès. L'essentiel se fait depuis l'app : exporter ou effacer les données du téléphone
(*Réglages → Données*), supprimer tes données du serveur (*Moi → Vulkia Premium*). Pour toute autre demande, contacte
l'éditeur (voir *Contact*) : sans compte relié à ton e-mail ou à Google, Vulkia ne connaît ni ton nom ni ton e-mail et
le serveur ne peut retrouver tes données qu'à partir de ton appareil ; l'éditeur te répond dans un délai d'un mois et t'indique comment relier ta
demande à ton compte, sans te demander plus que nécessaire. Tu peux aussi adresser une réclamation à la CNIL (www.cnil.fr) ou à l'autorité de
protection des données de ton pays.

## Contact
Par e-mail à **NexForg3@gmail.com**. Tu peux aussi contacter l'éditeur depuis la fiche Google Play de
l'application.

---

# Privacy policy — Vulkia (English)

The French version above prevails.

**Controller.** The controller of the data described here is the publisher of Vulkia: **NexForg3**, a French
simplified joint-stock company (SASU) being registered, reachable at **NexForg3@gmail.com**.

**On your device.** Your training log works **without an account**: workouts, routines, gyms, measurements, custom
exercises, settings and coach conversations are stored **on your device**, and nowhere else unless you have a Vulkia
account (then they go through *Encrypted sync*, below); export or delete them anytime from *Settings → Data*. Injuries and illnesses you declare (zone, type,
pain, symptoms, temperature, notes) are only used to adapt your workouts on the device: they **stay on your phone**,
are never sent in readable form to a server nor to Health Connect / Apple Health, and are only included in your own
backups and, with a Vulkia account, in the encrypted sync where they are only stored encrypted; a summary without your notes goes with your AI coach
requests **only with your explicit consent**. Vulkia adapts your training; it does not replace medical advice.

**Encrypted sync (with an account).** With a Vulkia account linked to Google or to your email, your workouts, routines
and folders, gyms, measurements, custom exercises, coach conversations, injuries and illnesses (with their notes),
progress photos (images included) and settings are **encrypted on your phone** (XChaCha20-Poly1305, random 256-bit key
of your account) before being sent to the Vulkia service, which stores them at Cloudflare (D1, R2) for your other
phones: you get them back by signing in, with no code to remember. Your account's key is kept by the Vulkia service,
itself encrypted (AES-256-GCM) by a secret key of the service kept apart from the database, and only given to a phone
signed in to your account: the database only holds encrypted blocks that someone who stole it could not read. It is
**not** end-to-end encryption: the publisher, who runs the service and its secret key, technically could decrypt
this data; the publisher refrains from doing so, except where the law requires it. The server also sees the number,
size and upload dates of the blocks, linked to your account. Sync is part of the Vulkia account and starts by itself
when you create the account or sign in, which the account screen says before you do: creating or signing in to the
account is your explicit choice, health information included (explicit consent, GDPR art. 9(2)(a), and performance of
the requested service). You withdraw it anytime: signing out stops this phone's uploads, and *Delete my data from the
server* erases the synced data with your account. Kept until you delete your server data.

**Your pseudonymous account.** The AI coach and **Vulkia Premium** use the Vulkia service hosted by Cloudflare with a
**pseudonymous account**: a random id bound to the random id of your installation (no name, no email, no phone
number). These ids do not say who you are, but they link the data below together: they are pseudonymous personal
data. The server keeps them, the platform, the creation and last-seen dates and, when you restored your subscription
on another device, the link between the accounts that share it. Your IP address is not stored, only a keyed hash kept
2 days to limit account creation.

**Vulkia account with email or Google.** A subscription needs a **Vulkia account linked to your Google account or to
your email address**, so you find your subscription and AI quota again on another phone (optional for everything
else). With your email, the server keeps your address and a **hash of your password** (PBKDF2-SHA256, random salt),
never the password itself. Vulkia sends you an email only when you ask for it: a **link** to confirm your address when
you create the account (the account exists only once the link is opened and your password chosen; otherwise the address
is kept only 24 hours, while the link is valid), a link to choose a new password (*Forgot your password*, 30 minutes) or
a 6-digit code for two-step verification (10 to 15 minutes); links and codes are only kept as a hash and work once. The
link goes through a nexforg3.fr page that opens the app: the part of the link that makes it unique is never sent to the
site's server.
**Two-step verification** (optional, email sign-in): a code at each sign-in, sent by email or shown by your
authenticator app; for the latter, the server keeps the key shared with the app, encrypted (AES-256-GCM), until you
turn it off or delete your account. With Google ("Continue with Google", Android), Google confirms your
identity and gives Vulkia your **Google account id**, your **email address** and whether it verified it — nothing else
from your Google account. The server also keeps the creation and last sign-in dates, and counts **failed sign-ins** per
hour under keyed hashes of the address tried and of the network (1 to 2 days). Signing out keeps the account; your
phone goes back to a pseudonymous account with the same AI usage counters. Deleting your data from the server also
erases your sign-in details (until then they are kept). The publisher may give Premium to some accounts (publisher,
testers) from their Google-verified email address or account id. Legal basis: performance of the contract (failed
sign-in counters: legitimate interest, abuse prevention). Google acts under its own privacy policy.

**Google user data ("Continue with Google").** When you choose to sign in with Google, Vulkia receives from Google
APIs only your **Google account id**, your **email address** and whether Google verified it (scopes `openid` and
`email`). The identity token Google gives may also contain your name and profile picture: Vulkia neither reads nor
stores them. Vulkia does not ask for access to your Gmail, Drive, contacts, calendar or any other data of your Google
account, and never receives your Google password. This data is used **only** to create your Vulkia account and sign
you in, to find your subscription, AI quota and synced data again on another phone, to identify you if you write to
us, and to give Premium to a verified address on the publisher's list (publisher, testers); **never** for advertising
(targeted, personalized, retargeted or interest-based), profiling, creating databases, determining credit-worthiness or
lending, nor to develop, improve or train AI or machine-learning models. It is **not sold, rented or shared**, nor
given to data brokers or information resellers; only the host of the Vulkia service (Cloudflare, processor, storing it
for the publisher) accesses it and, where the law requires it, the competent authorities. It is stored on the Vulkia
server at Cloudflare (D1 database, encrypted at rest by the host), only sent over encrypted connections (HTTPS) in
requests signed by the app; security procedures protect its confidentiality (access restricted to the publisher,
service secrets kept apart from the database, limits on sign-in attempts). It is kept as long as your account exists,
to let you sign in, and erased as soon as you delete your account in the app (*Me → Vulkia Premium → Delete my
data from the server*) or within a month of your request to **NexForg3@gmail.com**; you can also
remove Vulkia's access to your Google account anytime at
[myaccount.google.com/permissions](https://myaccount.google.com/permissions). **Limited Use:** Vulkia's use and transfer
to any other app of information received from Google APIs will adhere to the [Google API Services User Data
Policy](https://developers.google.com/terms/api-services-user-data-policy), including the Limited Use requirements.

**AI coach and replacement advice.** The AI coach sends your request and the needed context (training profile, workout
summary, gym equipment; never your name) with your account; Workers AI neither stores nor trains on it. **Your health
information is only sent with your explicit consent**: a summary of the injuries and illnesses you declared (without
your notes) and the pain or areas to protect named in a workout request. The app asks before the first request that
would contain some; give or withdraw it anytime in *Settings → Data → Privacy*. Without it, the coach answers without
this information and the app still adapts your workouts on your phone. What you type in the chat is sent as is. The server keeps **no request or answer
text**, except a 15-minute copy of generated workouts / programs (never chat) to resend them after a lost connection;
it keeps usage counters (day: 8 days, month: 13 months, the free discovery workout as long as the account exists) and
a technical log without text (kind, plan, status, model, tokens, cost, dates: 35 days). When you tap "AI coach advice"
(replacing an exercise), the app sends the exercise, the possible equivalents, your training goal, the language and,
if an injury concerns this exercise **and you gave your consent**, its area and pain level (mild or moderate) — never
your name, notes or history; without consent, or for strong pain (7/10 or more), pain advice is computed on the phone
and nothing is sent. The random id of your installation, and your account token when the
app already has it, are used for the request and cost limits (daily counters 7 days, monthly cost 13 months, log
without text 35 days); answers are cached 60 days without them. Offline or over the daily limit, the advice is
computed on the phone and nothing is sent.

**Subscription.** Purchases are made in **Google Play** or the **App Store**: the store never gives Vulkia your payment
method, name or email. **RevenueCat** processes your in-app purchase history and links it to your Vulkia account id; the Vulkia
server keeps the state of your subscription (product, store, trial, test or real purchase, dates, renewal, grace
period) until deletion and a log of the store notifications (event id and type, account id, dates) for 90 days. Your
plan is derived from this verified state, never from your phone. "Restore purchases" attaches your subscription to the
account of the device used, and the server records that this account and the one that had the subscription share it:
Premium stays active on each of those devices, with the same quotas.

**Usage statistics.** The app sends a few **aggregate event counters** (paywall, purchases, coach limits and server
refusals, first AI coach result, with the screen of origin from a fixed list): the server only keeps daily totals per
event, screen, plan and platform, without any account or device id, for 400 days.

**Deleting your data from the server.** *Me → Vulkia Premium → Delete my data from the server* erases your
account (with your sign-in details, synced data and its key, two-step verification settings), the subscription state Vulkia stored and the technical log of your finished requests. It does not cancel the
subscription (manage it in your store); an active subscription is attached to your next account by the app. Your AI
coach usage counters are **not reset** (units used, AI cost, the discovery workout): otherwise deleting would be a way
to get the discovery workout or the month's envelope again (legitimate interest: preventing abuse). They are kept
under a hash of your installation id computed with a secret key of the server (the id cannot be recovered from it) and
the next account created on that installation takes them over; they are kept like other counters (day 8 days, month
13 months), and the "ever" counter is erased after 400 days without use of the installation. Requests still running
at deletion time, the counters bound to your installation (replacement advice, statistics), the store notification
log (90 days), the IP hash (2 days) and the aggregate totals stay until their retention ends. Write to us to also
erase your purchase data at RevenueCat; the store keeps its own data under its own policy.

**Legal bases.** Performance of the contract (terms of use and subscription, GDPR art. 6(1)(b)): account, plan and
quotas, AI coach and replacement advice at your request, subscription. Health information attached to a request
(summary of injuries and illnesses, pain named, pain level): your explicit consent (art. 9(2)(a)), asked in the app
before the first request and withdrawable anytime in *Settings → Data → Privacy*, for the following requests. Legitimate interest (art. 6(1)(f)): abuse limits (IP hash, quotas per
installation, counters kept after a deletion), security of the service (signatures, technical log) and aggregate
usage statistics. Consent, given and withdrawn in the system permissions: Health Connect / Apple Health.

**Processors and transfers outside the EU.** Processors: Cloudflare, Inc. (hosting, AI models), RevenueCat, Inc.
(subscriptions), both established in the United States, and the email service chosen by the publisher to send the
codes (Gmail of Google LLC from the publisher's account, Brevo SAS in France, or Resend, Inc.: your email address and
the code); Google Play and Apple handle payment under their own
responsibility. **Transfers outside the EU** to these processors rely on the GDPR safeguards: Cloudflare is certified
under the EU-U.S. Data Privacy Framework and its data processing addendum also includes the European Commission's
standard contractual clauses; RevenueCat's data processing addendum relies on those standard contractual clauses. A
copy is available from the publisher.

**Demonstration videos (YouTube).** Tapping **Video** on an exercise plays it in the app from YouTube's
privacy-enhanced domain (`youtube-nocookie.com`): Google receives your IP address and technical device information and
may store data on your phone during playback, under its own privacy policy; the video may contain ads added by YouTube.
Vulkia sends it neither your account nor your workouts, and nothing loads until you open a video.

**Health Connect / Apple Health.** With your explicit permission (each data type can be refused separately), Vulkia
writes workouts (type, duration), estimated active calories and the weigh-ins you enter (weight, body fat, lean mass)
to Health Connect / Apple Health, and reads weight, height, body fat, lean mass, bone mass, body water and basal
metabolic rate recorded by your smart scale or other apps, to show your body composition, compute BMI / FFMI and track
progress; this data stays on the device and is never sold, shared or used for advertising. No ads, no advertising
trackers, no sale of data.

**Your rights.** You have the right of access, rectification, erasure, restriction of processing, data portability
and objection to processing based on legitimate interest; you can withdraw a consent at any time and set directives
on what happens to your data after your death. Most of it is done in the app (*Settings → Data*, *Settings →
Subscription*); for anything else, contact the publisher: without an account linked to your email or Google, Vulkia
knows neither your name nor your email and the server can only find your data from your device; the publisher answers within one month and tells you how to link
your request to your account, without asking for more than needed. You can lodge a complaint with the CNIL (www.cnil.fr) or with the data protection authority
of your country.

**Contact.** By email at **NexForg3@gmail.com**, or through the app's Google Play listing.
