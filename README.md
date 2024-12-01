## SteganoMafia

    SteganoMafia est une application qui permet aux utilisateurs de cacher des messages dans des images, d'envoyer ces images via des liens sécurisés et d'extraire les messages cachés.

## Installation

    1. Assurez-vous d'avoir Python 3.12.0 ou une version ultérieure installée.
    2. Installez les dépendances nécessaires en exécutant la commande suivante dans le terminal :
        pip install -r steganoandmafia\back\requirements.txt

## Fonctionnalités
    Cacher un message dans une image :

        Téléchargez une image depuis votre ordinateur personnel.
        Écrivez le texte que vous souhaitez cacher et sélectionnez un niveau de sécurité.
        Soumettez votre demande pour recevoir un lien de téléchargement pour l'image, une clé pour le destinataire et l'option d'envoyer l'image via un lien sécurisé.

    Lien sécurisé :

        Si l'utilisateur choisit d'envoyer l'image via un lien sécurisé de l'application, il doit définir un mot de passe.
        Un lien unique sera généré pour le destinataire, qui devra fournir le même mot de passe pour télécharger l'image.

    Extraire un message :

        Pour extraire le message caché, l'utilisateur doit télécharger l'image encodée et fournir la clé obtenue lors du processus de dissimulation.
        Le message sera alors décrypté et affiché.

## Exécution de l'application

    Pour exécuter l'application, suivez ces étapes :

        Naviguez vers le répertoire correct :
            Exécutez la commande suivante :

    python .\steganoandmafia\Back\app.py

    Alternativement, naviguez dans le dossier SteganoMafia\steganoandmafia\Back\ et exécutez :

            python app.py

    ## Prérequis de l'application

        Python : 3.12.0
        Dépendances :
            stegano : 0.11.4
            flask : 3.0.3
            itsdangerous : 2.2.0
            cryptography : 43.0.3

## Dépannage

    Q : Je reçois une erreur lors de l'exécution de l'application. Que dois-je faire ?
    R : Vérifiez que toutes les dépendances sont installées et que vous utilisez Python 3.12.0 ou une version ultérieure. Consultez le message d'erreur pour plus de détails.

    Q : Comment récupérer une clé secrète perdue ?
    R : Pour garantir la sécurité, les clés secrètes ne peuvent pas être récupérées une fois la page réinitialisée. Si vous l'oubliez, vous devez recommencer le processus de dissimulation d'un message dans une image.

    Q : Je n'arrive pas à insérer une image. Que faire ?
    R : Assurez-vous que l'image sélectionnée n'a jamais été utilisée auparavant. Une même image ne peut pas être utilisée plusieurs fois. Vérifiez également qu'elle est dans un format de fichier compatible avec l'application (par exemple : PNG).

    Q : Comment réinitialiser le mot de passe pour un lien sécurisé ?
    R : Pour garantir la sécurité, les mots de passe ne peuvent pas être réinitialisés. Si vous l'oubliez, vous devez générer un nouveau lien sécurisé et un nouveau mot de passe.

    Q : Que se passe-t-il si la clé que j'insère pour extraire un message est incorrecte ?
    R : Si la clé est incorrecte, l'application ne pourra pas déchiffrer le message. Vérifiez la clé et réessayez.

    Q : Pourquoi mon message caché ne s’affiche-t-il pas après extraction ?
    R : Assurez-vous que l'image que vous avez téléchargée n'a pas été modifiée après le processus de dissimulation. Toute modification (compression, redimensionnement, filtres, etc.) peut altérer les données cachées.

    Q : Puis-je cacher plusieurs messages dans une seule image ?
    R : Non, chaque image peut contenir un seul message caché. Si vous souhaitez cacher plusieurs messages, utilisez des images différentes.


## Structure
    "steganoandmafia\back\encoded" contient les images apres encodage
    "steganoandmafia\back\uploads" contient les images envoye vers l'application
    "steganoandmafia\back\templates" contient les pages html
    "steganoandmafia\back\static" contient les fichier css et les images statiques
    "steganoandmafia\back\_pycache_ , links" dossier necessaire pour le fonctionement de flask
    "steganoandmafia\back\requirements" fichier contenant les depandance de l'application
    "steganoandmafia\back\app.py" l'application principale flask
    "steganoandmafia\back\stegano_services" librairie contenant des fonction utilise par app.py



