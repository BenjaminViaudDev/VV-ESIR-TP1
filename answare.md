-2
    lien : https://issues.apache.org/jira/projects/COLLECTIONS/issues/COLLECTIONS-826?filter=doneissues
    
    Bug :
        BloomFilter: move CountingLongPredicate

    Explication du bug:

        Le bug se situe dans la classe CountingLongPredicate dans la méthode forEachRemaining. Cette méthode devrait être un détail d'implémentation, mais elle est actuellement déclarée comme package private dans une interface, ce qui la rend accessible publiquement.

        Si la méthode func.test renvoie false dans la boucle while de forEachRemaining, la boucle se termine avant que idx n'atteigne la longueur de ary. Cependant, cela permet à forEachRemaining d'être appelé à nouveau, réutilisant la même position dans le tableau. Si cette méthode était publique, elle pourrait être invoquée plusieurs fois, entraînant un comportement indéfini, surtout étant donné l'absence de commentaire sur ce point.

        De plus, une variable idx est initialisée à zéro, mais cette initialisation est redondante et peut être supprimée.
    
    Global ou local ?

        Le bug est plutôt local, car il concerne spécifiquement la méthode forEachRemaining de la classe CountingLongPredicate. Il n'affecte pas d'autres parties du code ou d'autres fonctionnalités de manière étendue.


    Solution ?

        Il est suggéré de déplacer la classe CountingLongPredicate en dehors de l'interface afin que la classe soit package private. Cela garantirait que la méthode forEachRemaining n'est pas accessible publiquement. De plus, des améliorations d'optimisation et de documentation sont suggérées pour clarifier le comportement de la méthode forEachRemaining.


    ont-il ajouter des nouveaux test ?
    
        Il n'ont pas ajouter des nouveaux test mais un comentaire pour spécifier sont fonctionement.


