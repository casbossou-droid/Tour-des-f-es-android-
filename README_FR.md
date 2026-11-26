# Tour des Fées — projet Android

Ce projet encapsule le jeu web fourni dans une application Android plein écran.

## Générer l'APK et l'AAB

1. Installe Android Studio sur un ordinateur.
2. Ouvre le dossier `TourDesFeesAndroid` dans Android Studio.
3. Laisse Gradle synchroniser le projet (connexion Internet nécessaire la première fois).
4. Pour tester : **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
5. Pour Google Play : **Build > Generate Signed Bundle / APK > Android App Bundle**.
6. Crée une clé de signature privée et conserve-la en lieu sûr. Ne la partage jamais.
7. Renseigne les informations de l'application et exporte le fichier `.aab`.

## Identifiants actuels

- Nom : Tour des Fées
- Identifiant Android : `com.tourdesfees.app`
- Version : 1.0 (code 1)
- Orientation : portrait

## Important

Le ZIP contient le projet Android prêt à ouvrir, pas encore les fichiers APK/AAB compilés.
La compilation et la signature nécessitent Android Studio/Android SDK et une clé de signature.
Avant publication, vérifie également les exigences Google Play (fiche de l'application, politique de confidentialité si nécessaire, classification du contenu et tests).

## Compilation depuis un téléphone (sans ordinateur)

Le dépôt contient un workflow GitHub Actions (`.github/workflows/android-build.yml`).
Depuis le navigateur du téléphone :
1. Crée un dépôt GitHub et téléverse le contenu de ce dossier.
2. Ouvre l'onglet **Actions** du dépôt.
3. Sélectionne **Build Tour des Fees Android**, puis **Run workflow**.
4. Quand le travail est terminé, ouvre-le et télécharge l'artefact **Tour-des-Fees-Android**.
5. Dans l'archive téléchargée, le fichier APK debug permet d'installer et tester le jeu.

Le fichier AAB produit par ce workflow est un bundle de compilation non signé. Google Play exige un AAB signé pour la mise en ligne. Il faudra configurer une clé de signature privée et les secrets GitHub avant la publication. Ne partage jamais cette clé ni son mot de passe.
