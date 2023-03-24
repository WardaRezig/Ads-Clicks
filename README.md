### Objectif du test: 

Le test implique d'entraîner un modèle et de créer une application qui utilisera ce modèle pour servir des utilisateurs non-techniques.

Le problème décrit est de type classification. Il s'agit de datasets tirés du marché réel avec toutes les implications que cela suppose (bruit dans la donnée, valeurs manquantes, mais aussi confidentialité, etc.).
Un composant crucial du test est le choix de la métrique pour évaluer votre modèle.
Vous devez prévoir de justifier votre choix dans la réponse que vous fournirez.
Une fois que vous aurez finalisé le modèle, créer une application Flask pour utiliser ce modèle. L'application affichera un formulaire où un utilisateur pourra rentrer des valeurs de même nature que le dataset que nous mettons à votre disposition, et l'application lui retournera son inférence.
L'application acceptera aussi un fichier CSV et Excel avec le même schème que le dataset de test, et rendra un tableau de résultats d'inférence du modèle.

### Dataset

Le fichier comporte une base de train et de test. Elles comportent
l'historique de pubs (ad_id, format) affichées sur des applications
mobiles (support_type, support_id) à un utilisateur (user_id, device_id,
device_model, device_type, device_os, device_language).
La boite de pub obtient ces emplacements par un système d'enchère (de
type Vickrey auction), nommé RTB.


Voici une petite explication de la signification de certaines variables:


bid_floor: mise minimum


won_price: prix à laquelle l'enchère est remportée


bid_price: prix à laquelle on mise, format 10^11 coût pour mille
impressions.


cpc_price: indique le cout par clic (format 10^8), c'est à dire à
quel prix est vendu le clic à l'annonceur .


verticals_X: sont des colonnes qui réfèrent au "classement" de
l'app, vous pouvez trouver des infos sur le site développer de
google (recherche google:verticals apps)


support_category: est un classement également des support (site où
les pubs sont affichées).


viewability: pourcentage de visibilité (-1 si inconnu)


position: position de l'ad sur la page


#### L'objectif est de trouver les probabilités pour la colonne clicked, omise à dessein. La réponse au test est le code que vous avez écrit pour trouver ces probabilités.

#### Le dataset est localisé à l’emplacement suivant:
https://www.dropbox.com/s/9jmpk7jtvnqzcto/data.tar.gz?dl=1
