## Auteur : Léo FRERE

# Projet:

Le but de ce projet est de représenter une liste chainnée ainsi que de pouvoir générer une "javadoc" pour pharo.

Les listes chainnées sont repésentées par la class ChainList qui est composée de head qui enregistre une valeur et de tail qui est une ChainList. Avec cette classe, on peut ajouter, supprimer, modifier un élement. Il y a aussi la possibilié d'itérer sur la liste ainsi que de vérifier si elle est vide, si elle contient un élement ainsi que de récupérer l'index d'un élement et récupérer un élément avec un index.

La "javadoc" est représentée par la classe PharoDoc qui va générer la documentation html d'une classe. Mais cette classe permet aussi de genérer la docementation de toutes les classes d'un package.

# Comment utiliser PharoDoc:

## Par défaut:
Par défaut vous pouvez générer la pharodoc de la manière suivante :

Pour une classe.
```Pharo
pharoDoc := PharoDoc new.
pharoDoc generateClassDoc: anClass.
```

Pour un package.
```Pharo
pharoDoc := PharoDoc new.
pharoDoc generatePackageDoc: anPackage.
```

La création des fichiers se fera dans le dossier Pharo Mooc.

## Windows choix du dossier:
Pour choisir le dossier dans lequel générer la pharodoc vous devez donnez un chemin vers le dossier de la manière suivante (/!\ si le dossier n'existe pas la pharodoc ne se générera pas):

Pour une classe.
```Pharo
pharoDoc := PharoDoc new.
pharoDoc generateClassDoc: anClass at: 'Users\utilisateur\...\doc' opt: 'windows'.
```

Pour un Package.
```Pharo
pharoDoc := PharoDoc new.
pharoDoc generatePackageDoc: anClass at: 'Users\utilisateur\...\doc' opt: 'windows'.
```

## Unix choix du dossier:
(Les informations suivante non pas été testé sur les systems MacOs)
Pour choisir le dossier dans lequel générer la pharodoc vous pouvez choisir entre rooot et home  comme point de départ puis vous devez donnez un chemin vers le dossier de la manière suivante (/!\ si le dossier n'existe pas la pharodoc ne se générera pas):

Pour une classe.
```Pharo
pharoDoc := PharoDoc new.
"/!\ root ne fonctionnera pas si pharo n'est pas lancer avec sudo"
pharoDoc generateClassDoc: anClass at: '...\doc' opt: 'root'.
pharoDoc generateClassDoc: anClass at: '...\doc' opt: 'home'.
```

Pour un Package.
```Pharo
pharoDoc := PharoDoc new.
"/!\ root ne fonctionnera pas si pharo n'est pas lancer avec sudo"
pharoDoc generatePackageDoc: anClass at: '...\doc' opt: 'root'.
pharoDoc generatePackageDoc: anClass at: '...\doc' opt: 'home'.
```


