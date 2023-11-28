VIAUD Benjamin
LAIR Arthur

# TP1

### 1) "Files Deletion Bug in Windows 10 October 2018 Update"

Source : https://www.askvg.com/reason-behind-users-files-deletion-bug-in-windows-10-october-2018-updte/
https://www.extremetech.com/computing/279368-windows-10-1809-may-have-another-file-deleting-bug-problem

Un exemple de bug informatique est le bug de Windows 10 connu sous le nom de "File Deletion Bug" qui est apparu en octobre 2018 avec la mise à jour de Windows 10 version 1809.

Le bug de suppression de fichiers survenu avec la mise à jour de Windows 10 version 1809 peut être considéré comme un problème à portée mondiale (global) car il a touché de nombreux utilisateurs qui ont effectué la mise à jour vers cette version spécifique du système d'exploitation Windows 10.

Description du bug : Ce bug a provoqué la suppression involontaire de fichiers lors de la mise à jour vers la version 1809 de Windows 10. Il était lié à la fonctionnalité de "Known Folder Redirection" (Redirection de dossiers connus), qui déplaçait certains dossiers spéciaux vers un autre emplacement. Lors de la mise à jour, cette fonctionnalité pouvait renommer l'ancien dossier, mais ne créait pas correctement le nouveau dossier dans l'emplacement de redirection, entraînant la perte apparente de fichiers.

Répercussions pour les clients/utilisateurs : Les utilisateurs affectés par ce bug ont subi des pertes de données importantes, parfois la suppression de dossiers entiers ou de fichiers critiques sans avertissement préalable.

Répercussions pour l'entreprise (Microsoft) : Ce bug a eu des conséquences préoccupantes pour Microsoft. La réputation de l'entreprise a été entachée, et elle a dû faire face à des critiques pour la qualité de ses mises à jour logicielles. En plus de l'impact sur la confiance des utilisateurs, cela a entraîné des efforts supplémentaires de la part de Microsoft pour résoudre le problème, émettre des correctifs et mettre en place des processus de test plus rigoureux pour éviter de tels problèmes à l'avenir.

Tests pour découvrir le bug : Des scénarios de test plus approfondis, notamment en simulant des migrations de données et des scénarios de redirection de dossiers connus variés, auraient pu potentiellement aider à identifier ce bug avant le déploiement de la mise à jour 1809 de Windows 10. Des tests plus exhaustifs sur la gestion des données pendant les mises à jour auraient pu contribuer à découvrir et à résoudre ce bug avant sa sortie auprès du grand public.

### 3) Netflix

Concrètement, les expériences de Chaos Engineering décrites dans l'article sont variées et se concentrent sur des scénarios de défaillance simulée ou réelle dans les systèmes distribués de Netflix. Quelques exemples d'expériences réalisées incluent :

    Chaos Monkey : Cette expérimentation consiste à arrêter aléatoirement des instances de machines virtuelles hébergeant des services en production pendant les heures de travail pour tester la résilience des systèmes face à de telles défaillances.

    Chaos Kong : Ces exercices simulent la défaillance d'une région entière d'Amazon EC2 pour évaluer la capacité de Netflix à basculer efficacement vers d'autres régions en cas de panne.

    Tests d'injection de défaillance (FIT) : Ils consistent à rendre intentionnellement défaillantes les requêtes entre les services Netflix pour vérifier la dégradation contrôlée du système.

Les exigences pour ces expériences incluent la capacité à réaliser des tests en production, à simuler des défaillances de manière contrôlée et à observer les métriques et indicateurs clés qui reflètent la stabilité et la fiabilité du système. Parmi les variables observées, on retrouve des métriques telles que le nombre de démarrages de streaming par seconde (SPS) pour évaluer l'état de santé global du système.

Les principaux résultats obtenus par ces expériences sont l'amélioration de la conception des services Netflix pour résister aux défaillances individuelles, l'identification de mécanismes de dégradation contrôlée en cas de panne et l'augmentation de la confiance dans la capacité du système à maintenir son comportement en cas de perturbation.

Netflix n'est pas la seule entreprise à réaliser de telles expériences. L'article mentionne également Amazon, Google, Microsoft et Facebook comme d'autres entreprises appliquant des techniques similaires pour tester la résilience de leurs systèmes.

Ces expériences pourraient être menées dans d'autres organisations en adaptant les types d'expériences aux services spécifiques qu'elles offrent. Par exemple, dans une organisation de commerce électronique, des expériences pourraient être menées pour simuler des défaillances dans le processus de paiement en observant des métriques telles que le nombre de transactions réussies par seconde. De manière générale, les variables observées pendant les expériences doivent être des métriques représentatives du comportement normal du système et de son état de santé global. Les expériences devraient également tenir compte des interactions entre les différents composants du système pour évaluer la résilience de l'ensemble du système.

### 5) Isabelle

