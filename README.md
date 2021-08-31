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

où `3.X.X` correspond à la version de python installée. Ensuite, vérifions aussi que `pip` a aussi été installé correctement (`pip` sera expliqué plus bas).  Pour ce faire, ouvrez un autre terminal ou *sortez* de l'interpréteur python (entrez la commande `>>> exit()` ou pesez `ctrl + d`). Entrez maintenant la commande

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

Windows est équipé de 2 options pour le terminal; `cmd` et `powershell`. Pour ouvrir un nouveau terminal, ouvrez le start menu et tappez 'cmd' ou 'powershell' dans la barre de recherche. Lorsque le terminal est lancé de cette manière, vous serez toujours situé dans votre *home* directory.

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
| `ls` | affiche le contenu du directory ou vous êtes | `ls` | Linux, Mac


# Utilisation de `pip`

