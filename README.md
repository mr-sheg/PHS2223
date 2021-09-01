# PHS2223

# Intro

Bonjours et bienvenu!
Vous trouverez ici des exemples et démos de l'utilisation de **python** dans la résolution de problèmes liés au cours *PHS2223 - Introduction à l'optique moderne*. Si vous avez des questions n'hésitez pas à me contacter !


## Conventions : le minimalisme!
Comme à mon habitude, je privilégie toujours une approche *simple* plutôt que *facile* (simple is better!). Je m'explique, par *simple*, j'entends une approche nécessitant le moins de *composantes* ou *libraries*. Par *facile*, j'entends généralement une approche nécessitant moins de *connaissance* ou *habiletés*. Par exemple, je préfère utiliser le terminal plutôt qu'une interface graphique pour plusieurs tâches. Je préfère manuellement installer les librairies ou modules que j'utilise (et uniquement ceux-là) plutôt que d'installer un environnement comprenant *tout ce qui peut être nécessaire*... ce qui m'amène à **pip** et **anaconda**...


## Pip ou anaconda?

Si vous êtes débutant python ou n'avez aucune idée de ce dont je parle je vous suggère d'aller lire ce [résumé de la situation](https://www.askpython.com/python/conda-vs-pip). Pour faire simple, je n'utilise pas et ne recommande pas l'utilisation d'anaconda (sauf exception, voir plus bas). Du point de vue pédagogique, l'utilisation d'anaconda fait en sorte que vous n'avez pas à développer plusieurs connaissances, habiletés et pratiques importantes (selon moi) en lien avec l'installation et la gestion de votre système et environnement python. C’est-à-dire que l'utilisation d'anaconda s'avère (toujours selon moi) détrimentale à votre apprentissage et à la progression de vos habiletés en programmation. Ceci est, bien sur, uniquement mon opinion et vous êtes libre de vous servir des outils que vous voulez :wink:.

**exception**

- Vous n'êtes pas sur un système sur lequel vous avez les droits administrateur -> pip a besoin des droits administrateur dans certains cas -> utilisez anaconda
- Vous travaillez avec d'autres sur un projet utilisant un environnement anaconda -> gardez anaconda

---

# Installation de python

La première étape pour se servir de python est bien sûr de l'installer sur son système. Je recommande l'installation de la version *python 3.8 64bit* (au moment de l'écriture de ce guide). Pour ce faire, téléchargez la version la plus récente de *python 3.8* pour votre système d'exploitation à [python.org](https://www.python.org/).

Procéder ensuite à l'installation sur votre système.

Lors d'une installation sur Windows. Assurez-vous de bien sélectionner les options suivantes ou leurs équivalents ;

1. `Add Python 3.8 to PATH`
1. `Customize installation`
1. Cochez toutes les `advanced options`
1. Assurez-vous que l'`install location` soit bien `C:\Program Files\Python38`
1. À la fin de l'installation si vous avez l'option `Disable Path length limit` **faîte le**!!!

Vous pouvez maintenant vérifier que l'installation s'est effectuée avec succès en ouvrant un terminal et en entrant la commande

    python


---
### Exemple de **téléchargement** python 3.8.10 pour Windows 64bit



https://user-images.githubusercontent.com/27356351/131276719-82fc4afa-abc0-4c1d-a5a6-6b9744aa03fd.mp4


---

### Exemple d'**installation** python 3.8.10 pour Windows 64bit

https://user-images.githubusercontent.com/27356351/131276739-21e81191-f44e-4d7c-a9a7-fcb40909637e.mp4


---

## Vérification de l'installation

Vérifions maintenant que l'installation s'est effectuée avec succès. Pour ce faire, ouvrez un terminal (voir la section `terminal et shell` pour quelques détails) et entrez la commande

    python

Si l'installation python a été un succès, vous devriez obtenir un message de retour similaire à

```
 Python 3.X.X (default, Jun 30 2021, 10:22:16) 
 [GCC 11.1.0] on linux
 Type "help", "copyright", "credits" or "license" for more information.
 >>> 
```

où `3.X.X` correspond à la version de python installée. Ensuite, vérifions aussi que `pip` a aussi été installé correctement (`pip` sera expliqué plus bas).  Pour ce faire, ouvrez un autre terminal ou *sortez* de l'interpréteur python déjà ouvert (entrez la commande `>>> exit()` ou pesez `ctrl + d`). Entrez maintenant la commande

    pip

Vous devriez maintenant obtenir un message similaire à

```
Usage:   
  pip <command> [options]
  
Commands:
  install                     Install packages.
  download                    Download packages.
  uninstall                   Uninstall packages.

  ...
  ...
  ...
```

https://user-images.githubusercontent.com/27356351/131553527-76f52bce-119a-46ad-aa23-74d53e48766d.mp4

Si ce n'est pas le cas, **ne progressez pas plus loi**, il y a eu un problème lors de l'installation. Il arrive souvent que des problèmes soient causés par plusieurs installations python en conflits sur votre système. Si vous ne savez pas comment gérer plusieurs installations différentes sur le même système (c'est normal à ce point, je l'explique plus loin :wink: ), le plus simple est de s'assurer de désinstaller toute trace de python de votre système (*ATTENTION*: à faire seulement sur windows. Mac et Linux ont toujours au moins une version de python installée et utilisée par votre OS.) Reprenez ensuite les étapes précédentes en faisant attentions aux bonnes options à cocher et sélectionné. Si rien n'y fait, n'hésitez pas à me contacter!


# Terminal et shell

À partir de maintenant, nous nous servirons souvent du terminal pour différentes tâches comme installer des librairies, gérez des environnements python et lancer jupyter. Je sais, je sais, le terminal est un petit monstre caché aux tréfonds des ordinateurs modernes qui terrifie tous ceux qui ne savent pas déjà s'en servir. N'ayez crainte! Je serai votre guide et ensemble nous saurons bien illuminez ces coins sombres qui hante vos cauchemars informatiques!

## Terminal, CLI, prompt ou shell?

C'est déjà compliqué! 'Terminal', 'CLI' (short for 'Command Line Interface'), 'prompt' (ou 'command prompt') ou bien 'shell'? Ok ok faisons simple! Pour la suite, je vais toujours utiliser le mot 'terminal'. Sachez par contre que les 4 termes sont souvent utilisés interchangeablement et dans différents contextes. Il existe plusieurs nuances et une sorte de hiérarchie entre chacun, mais toutes ces subtilités dépassent largement notre contexte. Donc pour faire simple, 'terminal'! Par contre, je dois ici présenter les nuances entre les 3 OS; Windows, Mac et Linux.

### **Windows**

Windows est équipé de 2 options pour le terminal; `cmd` et `powershell`. Pour ouvrir un nouveau terminal, ouvrez le start menu et tappez 'cmd' ou 'powershell' dans la barre de recherche. Lorsque le terminal est lancé de cette manière, vous serez toujours situé dans votre *home directory*.

https://user-images.githubusercontent.com/27356351/131553445-c63f2a11-8836-4921-9b71-b576376006d3.mp4

Une autre manière très utile pour ouvrir un terminal dans un directory spécifique est d'ouvrir celui-ci avec *explorer* et ensuite de `shift + right click` pour obtenir l'option `open powershell here`.

https://user-images.githubusercontent.com/27356351/131553466-c29daa3c-6abc-41e5-9fdf-23f18ff9678d.mp4

### **Mac**

Désolé, je n'ai pas de Mac et contrairement à Windows l'installation d'une machine virtuelle OSX est très difficile (thx Apple...). Voici le mieux que je puisse faire pour vous;

https://support.apple.com/en-ca/guide/terminal/apd5265185d-f365-44cb-8b09-71a064a42125/mac

### **Linux**

You got this.

### Commandes utiles

Voici une liste des commandes qui peuvent vous être utile. Bien sûr, toutes ne fonctionnent pas sur chaque OS. (**Note** ; Je ne peux pas non plus tester les commandes pour mac, j'ai fait confiance à la documentation en ligne.)

| Commande | Utilisation | exemple | OS |
|---|---|---|---|
| `cd` (for Change Directory) | navigation à un autre directory | `cd Desktop` `cd /home/gsheehy/Desktop/`  | Linux, Mac, Win
| `cd ..` | navigation au parent directory | `cd ..` | Linux, Mac, Win
| `dir` | affiche le contenu du directory ou vous êtes | `dir` | Linux, Mac, Win
| `ls` | affiche le contenu du directory ou vous êtes | `ls` | Linux, Mac |
| `mkdir` | crée un nouveau directory | `mkdir directory_name` | Linux, Mac, Win


# Utilisation de `pip`

Voyons maintenant comment installer des librairies et modules additionnels. Pour ce faire, le plus facile est d'utiliser un *package manager*. Les *package manager* ne sont pas exclusifs et précèdent largement python. Bien que peu communs sur Windows, leur utilisation est une méthode fiable et robuste de gérer automatiquement le téléchargement et l'installation de programmes, ressources, extension, libraires, etc... à partir de *repositories* (spécifiquement *Package Indexes*) en ligne. Dans le cas de python, `pip` est un *package manager* permettant l'installation de libraries disponibles sur https://pypi.org/ (PyPI = Python Package Index). `Pip` est un CLI tool (Command Line Interface Tool) ce qui implique que son utilisation se fait via un terminal. Commençons par un exemple simple; l'installation de *numpy*. Pour ce faire, ouvrez un terminal et entrez la commande

    pip install numpy

https://user-images.githubusercontent.com/27356351/131576982-b54441e9-8448-4441-93d8-9fa8d1b26e88.mp4

Les messages en jaune sont des *warning* et nous informe de potentiels problèmes, mais ne sont pas des *erreurs* et n'indiquent généralement pas l'échec de commandes. Pour vérifiez que l'installation de *numpy* s'est effectué avec succès, nous pouvons vérifier les libraries installées sur le système avec

---

### Warning important à régler

Dans l'exemple vidéo, 2 `warnings` sont présents. Le premier est causé par le *path* `C:\Users\...\Python\Python38\Scripts` qui n'est pas dans le *windows PATH* (ce genre de chose n'arrive que sur windows :facepalm: ). Il faut régler ça!

Le second warning est causé par une version de `pip` qui peut être mis à jour. Ce n'est pas *nécessaire*, mais très facile à régler:

    pip install --upgrade pip

---

vérifions les `packages` installés

    pip list

Installons *jupyter lab* (attention à ne pas mettre d'espace entre *jupyer* et *lab* dans la commande pip!!!),

**ATTENTION** - *certains* packages doivent être installer en mode administateur (c'est le cas pour jupyter). Pour ce faire, ouvrez un terminal par `rightclick` + `run as administrator` puis

    pip install jupyterlab

https://user-images.githubusercontent.com/27356351/131739126-50f540bc-f075-4ea5-a26a-8551c03c719b.mp4

Pas d'inquiétude, beaucoup de modules ont été installé en addition de *jupyter lab*. C'est normal et une très bonne chose. Simplement, `pip` a non seulement installé *jupyter lab* comme demandé, mais aussi toutes les dépendances nécessaires à *jupyter lab*!

pour vérifier l'installation de jupyter

    jupyter lab


Finalement, voyons aussi comment désinstaller un module. Pour désinstaller *numpy* par exemple

    pip uninstall numpy

Pour obtenir plus d'information sur `pip` et son utilisation,

    pip help

# Environnements virtuel Python

Maintenant que vous savez vous servir de `pip` pour installer des librairies additionnelles, la prochaine étape est d'apprendre à créer et gérer des environnements virtuels. Pourquoi? Tout simplement parce que ce que nous avons fait dans la section précédente peut (dans certain cas) menez à des problèmes plus tard. Lorsque nous avons installer *numpy* et *jupyter*, nous les avons installé *system wide*.

Ok, mais et alors?

Considérons la situation suivante;
Vous travaillez avec 2 équipes différentes sur 2 projets différents. Dans le projet 1, vous utilisez python 3.9 et *numpy* 1.21 alors que dans le projet 2, vous utilisez python 3.7 et *numpy* 1.14. Faîte-moi confiance, ce genre de situation est plus fréquente qu'il n'y paraît :wink:. Comment pouvons-nous alors avoir plusieurs versions différentes des modules installés *system wide*? Simplement, on ne peut pas! C'est pourquoi on doit utiliser des *environnements virtuels*!

Pour faire simple, un environnement virtuel est un *directory* contenant une *copie locale* de python incluant son propre *Python binary* et ses propres modules additionnels. La méthode que nous utiliserons pour créer nos environnements virtuels est l'utilisation du module `venv` (https://docs.python.org/3/library/venv.html) qui fait partit du *Python Standard Library* (-> déjà installé, pas besoin de `pip install ...`).

## Créer un nouvel environnement

Avant tout, il faut décider où mettre le nouvel environnement. Je suggère fortement de créer un *directory* appelez `python/` dans votre *home folder* (*path* exacte dépend de votre OS et configuration) et d'y installer tous vos futures environnements. Comme ça, vous aurez toujours un accès rapide à partir d'un nouveau terminal (qui ouvre directement dans votre *home folder*). ATTENTION, une fois créer, déplacer un environnement peut avoir des conséquences et briser certaines choses... à éviter!

Terminal:

    mkdir python
    cd python

Pour créer un nouvel environnement (*phs2223* sera ici le nom de ce nouvel environnement),

    python -m venv phs2223


https://user-images.githubusercontent.com/27356351/131577994-4c5ab321-b317-4db0-8dbe-5f8d7ea4170d.mp4

Maintenant pour installer des modules additionnels avec `pip`, nous devons *activer* cet environnement dans un terminal (*l'activation* doit être faite à chaque fois pour chaque nouveau terminal)

**Windows**

    C:\Users\...\>python\phs2223\Scripts\activate
    
https://user-images.githubusercontent.com/27356351/131578111-20868b2c-c106-4998-b08f-5d3582f0c9da.mp4

**Mac et Linux**

    [...]$ source python/phs2223/bin/activate

Lorsqu'un environnement est *activé*, vous aurez son nom entre parenthèse devant le prompt (ligne dans le terminal). Dans ce cas,

**Windows**

    (phs2223) C:\Users\...>

**Mac et Linux**

    (phs2223) [... ~]$

Nous pouvons maintenant utiliser `pip` avec notre nouvel environnement comme précédemment ou pour installer une liste de dépendances (`requirement.txt`)

# requirement.txt

Maintenant que nous savons comment créer des environnements virtuels ainsi que d'y installer les packages additionnels que l'on veut, nous allons maintenant apprendre à partager ces environnements. Supposons ici que j'ai créé un environnement (ex: `/.../python/phs2223`) dans lequel j'ai installé plusieurs packages (ex: numpy, jupyter lab, matplotlib, sympy, ...) tous avec une version spécifique. Comment faire pour partager cette information pour que tous aient le même environnement? Je vous partage la liste des packages et vous passez la prochaine heure à faire du ```pip instal``` ? Non, trop long... Je vous partage mon dossier `/.../python/phs2223`? Non, problème de compatibilité entre les OS et trop lourd, ... Alors comment? Je vous donne un `requirement.txt`!

Pour installer les packages d'un `requirement.txt`, 

    pip install -r requirement.txt

**NOTE** - assurez vous

1. D'avoir *activer* votre environnement (sinon vous allez installer la liste *system wide*)
2. D'être dans le dossier où se trouve `requirement.txt` (sinon vous pouvez spécifier le *absolute path* du `requirement.txt` dans la commande)

## requirement.txt de phs2223

Télécharger maintenant le *repository* phs2223. Pour ce faire, retourner au haut de la page, cliquez sur *code*, puis *download as zip*. Faîtes l'extraction où vous voulez pour la suite. Procédez ensuite à l'installation avec `pip`.


https://user-images.githubusercontent.com/27356351/131731006-01c67907-e85d-4519-b3d2-6eb918931243.mp4


https://user-images.githubusercontent.com/27356351/131731036-2448565b-8692-4d92-859b-1a05977c8d4d.mp4



# Lancement de `jupyter lab`

Nous voilà finalement à la dernière étape, ajouter notre environnement `phs2223` à jupyter.

**Note** - Vous devez **aussi** avoir installé jupyter *system wide* (et une de ses dépendances: `ipykernel`)

Si on lance `jupyter lab` présentement, nous n'aurons pas accès au *kernel* de notre nouvel environnement.

Pour vérifier les *kernels* disponibles,

    jupyter kernelspec list

Pour ajouter le *kernel* d'un environnement, **dans un terminal où l'environnement est activé**,

    python -m ipykernel install --user --name NOM_DE_LENVIRONNEMENT



Vous pouvez maintenant lancer *jupyter* et exécuter les *jupyter notebooks* (`.ipynb`) du cours PHS2223!
