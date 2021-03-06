![Git logo](images/logos/logo-git.png)

# Git Interview Questions

Q. How does Git differ from SVN?

<details><summary>Answer</summary>

Subversion(SVN) is a centralized version control system. This means that the remote repository is the only true central place of storage and exchange. The project's commit history is saved there - and only there! In cases when this central remote repository is not available (offline or broken), people will not be able to work.

Git is a distributed version control system. This means that every developer / collaborator has a full-blown version of the project on their machine, including all commit history. With a decentralized VCS, you can work offline and make commits to your own local repository - and then decide when you want to share and upload your work to a shared remote repository.

![image](images/004.png)

</details>

---

Q. Are Git and GitHub the same thing?

<details><summary>Answer</summary>

Not quite. Git is installed locally, whereas GitHub is a web-based hosting service for git repositories. GitHub also offers additional features such as issue tracking, user management, and hosting web pages.

</details>

---

Q. What is the difference between `git pull` and `git fetch`?

<details><summary>Answer</summary>

`git fetch` is the command that tells your local git repository to retrieve the latest metadata info from a remote repository, but it doesn't integrate any of this new data into your working files. It's more like just checking to see if there are any changes available. `git pull` on the other hand does that AND brings a copy of those changes from the remote repository and updates your current HEAD branch.

</details>

---
