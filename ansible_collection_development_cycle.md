Cycle de développement Ansible collection

1. Planification / découpage des taches à développer
Elements à considerer:

OS et version d'OS
Version de python
Version d'Ansible et l'environnement d'exécution
Les entrées
Les roles et les collections Ansible existant
2. Codage
1. Créer et cloner un repo git

2. Checkout dans une branche develop

3. Initialiser la collection (boiler plate) [Creating collections — Ansible Documentation](https://docs.ansible.com/ansible/latest/dev_guide/developing_collections_creating.html#id2)

4. Réaliser le premier commit et push le squelette de la collection au remote repo git

5. Checkout dans une branche feature/feature_name pour commencer à développer votre première fonctionnalité.

3. Build la collection
1. Télécharger tous les dépendances de votre collection [Installing content — Ansible Documentation](https://galaxy.ansible.com/docs/using/installing.html)

2. Supprimer les assets non utilisés (eg: dossier example)

4. Tester la collection
Elements à considerer:

Creator-ee [GitHub - ansible/creator-ee: Ansible Execution environment targeted for content creators. It includes most development tools such ansible-lint, molecule, ...
L'image de l'OS à tester par exemple: RHEL 8, Cisco IOS ...](https://github.com/ansible/creator-ee)
Lancer les tests sur AAP

a. Si les tests ont réussi => Créer une merge request au niveau de GitLab

b. Si les tests ont échoué => Notifier les développeurs

5. Promouvoir un candidat de release
Push la collection dans Automation Hub de l'environnment pré-production avec un tag version et suffix rc (Numéro de candidat de release).

Par exemple: edf.souches-1.0.0-rc0

"entreprise" comme namespace

"souches" comme nom de la collection

"1.0.0" comme version de release

"rc0" comme premier candidat de release

6. Utiliser le candidat de release dans l'environnement pré-production
7. Publier la collection dans Automation hub de production
Obtenir les feedbacks d'utilisateurs et revenir à la première étape pour planifier la prochaine développement
