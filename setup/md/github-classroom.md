Guide pour accepter un devoir et cloner un dépôt Github Classroom.
> Rassurez vous d'avoir un compte Github au préalable.

## Etapes à suivre

1. **Acceptez le devoir** 
- Suivez ce [lien](https://classroom.github.com/a/gdTCbQm4)
- Cherchez votre nom dans la liste des étudiants et sélectionnez le
- Acceptez ensuite l'assignement
- Un dépôt de code va s'auto-générer avec votre nom d'utilisateur Github comme préfixe.
    Ex(cf. Image): `https://github.com/nosql-esigelec/hello-world-bricefotzo`
![accpet](../../assets/images/accept-assignment.png)
 
2. **Cloner votre dépôt d'assignement** :
   
   - **Méthode 1**: Cliquez sur le bouton `Open in Visual Studio Code` pour ouvrir le projet directement dans votre IDE Visual Studio Code.
   
   - **Méthode 2**: Si la première ne fonctionne pas, cliquez sur le lien qui mène à votre dépôt Github en ligne. Il s'agit de `https://github.com/nosql-esigelec/username-file-{username}`.
   Une fois sur la page de votre dépôt, récupérer le lien(SSH) de clonage de votre dépôt au
    Récupérez le lien(SSH) de clonage de votre dépôt Github Classroom et clonez-le sur votre machine locale à l'aide de la commande suivante :
     ```
     git clone [lien-du-dépôt]
     ```
     > PS: Rassurez vous avant d'avoir généré une clé SSH sur votre poste local, que vous avez ajouté sur votre compte Github.
     > Ce tutoriel [How to generate SSH keys for Github](https://medium.com/@kiran.jasvanee/the-process-to-generate-ssh-key-and-add-it-on-github-ba7139c07daf) vous indique comment faire.
     > Si vous rencontrez une difficulté avec la commande ssh-keygen sur Windows, consultez ce [tutoriel](https://phoenixnap.com/kb/generate-ssh-key-windows-10)
