**Nom :** AMPEAU, CHEVEAU

**Groupe :** groupe 14

**Année :** 1ère

**IUT Le Havre - Cours GIT**

### Compte-rendu TP3 Introduction GIT

TP 3 : Travailler en équipe sur un dépôt GitHub distant

Objectifs du TP 3 :
- Inviter des collaborateurs dans un dépôt personnel
- Développement d’un projet Java en équipe
- Gérer des nouvelles fonctionnalités à l’aide des branches

1. Inviter des collaborateurs dans un dépôt personnel
- Athos crée un dépôt "tp3" sur son compte GitHub.
- Dans "Settings > Manage access", il invite Porthos.
- Porthos accepte l'invitation via e-mail.
- Les deux clonent le dépôt dans ~/courseGIT :
  `git clone git@github.com:<utilisateur_de_athos>/tp3.git`
- Porthos copie les fichiers de tp2 (README.md, src/Cryptomonnaie.java) dans tp3 sans le dossier .git et synchronise.
- Athos fait un `git pull` pour récupérer les changements.

2. Développement d’un projet Java en équipe
- Objectif : compléter une application de marché de crypto-monnaie.
- Portefeuille.java : gère les jetons d'un utilisateur.
- CryptoMarche.java : gère tous les portefeuilles et le capital total.

Tâches :
- Athos : implémenter `capitalEnEuros(String proprietaire)` et `capitalMonneaie(Cryptomonnaie monnaie)` dans CryptoMarche.java.
- Porthos : implémenter `transfertDevise(Portefeuille dest, double montantJetons)` et `achatDevise(double montantEuros)` dans Portefeuille.java.

Tests attendus :
```
Test Portefeuille transfertDevise        ... OK
Test Portefeuille achatDevise            ... OK
Test CryptoMarche capitalEnEuros         ... OK
Test CryptoMarche capitalMonneaie        ... OK
```

3. Gérer des nouvelles fonctionnalités à l’aide des branches

3.1. Test de branche :
- Créer une branche `test` : `git checkout -b test`
- Ajouter `test.txt`, le valider.
- Revenir à `main`, modifier README.md.
- Visualiser avec : `git log --graph --oneline --all --decorate --topo-order`

3.2. Fusion :
- Sur `main`, faire `git merge test`
- Supprimer test.txt : `git rm test.txt`, puis commit.

Exercice final :
- Athos crée branche AthosCoin, Porthos crée PorthosCoin.
- Ajouter une classe de crypto personnalisée :
```java
public class AramisCoin extends Cryptomonnaie {
    public AramisCoin() {
        super("ARA", 1000);
    }
}
```
- Fusionner les branches dans main, synchroniser sur GitHub.

Fin du TP 3.

