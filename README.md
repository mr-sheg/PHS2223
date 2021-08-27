# PHS2223

## Intro

Bonjours et bienvenu!
Vous trouverez ici des exemples et démos de l'utilisation de **python** dans la résolution de problèmes liés au cours *PHS2223 - Introduction à l'optique moderne*. Si vous avez des questions n'hésitez pas à me contacter !


### Conventions : le minimalisme!
Comme à mon habitude, je privilégie toujours une approche *simple* plutôt que *facile* (simple is better!). Je m'explique, par *simple*, j'entends une approche nécessitant le moins de *composantes* ou *libraries*. Par *facile*, j'entends généralement une approche nécessitant moins de *connaissance* ou *habiletés*. Par exemple, je préfère utiliser le terminal plutôt qu'une interface graphique pour plusieurs tâches. Je préfère manuellement installer les librairies ou modules que j'utilise (et uniquement ceux-là) plutôt que d'installer un environnement comprenant *tout ce qui peut être nécessaire*... ce qui m'amène à **pip** et **anaconda**...


### Pip ou anaconda?

Si vous êtes débutant python ou n'avez aucune idée de ce dont je parle je vous suggère d'aller lire ce [résumé de la situation](https://www.askpython.com/python/conda-vs-pip). Pour faire simple, je n'utilise pas et ne recommande pas l'utilisation d'anaconda (sauf exception, voir plus bas). Du point de vue pédagogique, l'utilisation d'anaconda fait en sorte que vous n'avez pas à développer plusieurs connaissances, habiletés et pratiques importantes (selon moi) en lien avec l'installation et la gestion de votre système et environnement python. C’est-à-dire que selon moi (sauf exception), l'utilisation d'anaconda s'avère détrimentale à votre apprentissage et à la progression de vos habiletés en programmation. Ceci est, bien sur, uniquement mon opinion et vous êtes libre de vous servir des outils que vous voulez :wink:.

**exception**

- Vous n'êtes pas sur un système sur lequel vous avez les droits administrateur $\rightarrow$ pip a besoin des droits administrateur dans certains cas $\rightarrow$ utilisez anaconda
- Vous travaillez avec d'autres sur un projet utilisant un environnement anaconda $\rightarrow$ gardez anaconda

---

## Installation de python

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
#### Exemple de **téléchargement** python 3.8.10 pour Windows 64bit

<center>
  <video width="500" controls preload> 
      <source src="doc/python_download.mkv"></source>
  </video>
</center>

---

#### Exemple d'**installation** python 3.8.10 pour Windows 64bit

<center>
  <video width="500" controls preload> 
      <source src="doc/installation_python_edited.mkv"></source>
  </video>
</center>

---


