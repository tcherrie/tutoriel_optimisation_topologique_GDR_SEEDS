# Tutoriel Optimisation Topologique - GDR SEEDS - 10/05/2023

[![GitHub license](https://img.shields.io/github/license/tcherrie/tutoriel_optimisation_topologique_GDR_SEEDS)](https://github.com/tcherrie/tutoriel_optimisation_topologique_GDR_SEEDS) [![GitHub release](https://img.shields.io/github/release/tcherrie/tutoriel_optimisation_topologique_GDR_SEEDS.svg)](https://github.com/tcherrie/tutoriel_optimisation_topologique_GDR_SEEDS/releases/) [![GitHub stars](https://img.shields.io/github/stars/tcherrie/tutoriel_optimisation_topologique_GDR_SEEDS)](https://github.com/tcherrie/tutoriel_optimisation_topologique_GDR_SEEDS/stargazers) 
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.7969354.svg)](https://doi.org/10.5281/zenodo.7969354)


[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/tcherrie/tutoriel_optimisation_topologique_GDR_SEEDS/main?urlpath=/tree/)

## 1) Contenu du répertoire
L'objectif de ce tutoriel est de réaliser l'optimisation topologique d'un transformateur, à l'aide de [NGSolve](https://ngsolve.org/), logiciel open-source fonctionnant sous [Python](https://www.python.org/). Ce répertoire contient plusieurs fichiers, dont certains [notebooks Jupyter](https://jupyter.org/) exécutables. Ces fichiers sont organisés pour être consultés dans l'ordre suivant :

- `README` (ce fichier)
- `1-Guide Jupyter.ipynb` : notebook sur les bases d'utilisation de Jupyter
- `2-BaseNgSolve.ipynb` : notebook d'illustration de la syntaxe de NGSolve
- `3-Optimisation topologique d'un transformateur.ipynb` : notebook associé à l'activité de ce tutoriel
- `4-Tutoriel (sujet).pdf` : énoncé comportant des questions associées à l'activité

Il contient également des éléments de correction et d'explication :

- `5-Tutoriel (corrigé).pdf` : énoncé comportant des éléments de réponse aux questions théoriques
- `Presentation_tutoriel_optimisation_topologique.pdf` : présentation générale de l'activité
- `Optimisation topologique d'un transformateur-corrige.ipynb` : notebook de l'activité complet et fonctionnel

Enfin, il contient des fichiers annexes :
- `LICENCE` : fichier de Licence GNU General Public License
- `Dockerfile` : fichier de configuration de la machine virtuelle [MyBinder](https://mybinder.org/)
- `CITATION.cff` : fichier comportant les informations de citation

## 2) Lancement sur machine distante *sans installation*

1. Cliquer sur [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/tcherrie/tutoriel_optimisation_topologique_GDR_SEEDS/main?urlpath=/tree/), et attendre le chargement de la machine virtuelle. *Attention*, cette dernière se déconnecte après 10 minutes d'inactivité, et votre travail ne sera pas sauvegardé!
2. Ouvrir les notebooks Jupyter présents sur l'arborescence directement via votre navigateur internet.
3. Vous pouvez maintenant interagir avec les notebooks et démarrer l'activité.

**Important** : le lancement de la machine distante utilise le service gratuit et collaboratif [MyBinder](https://mybinder.org/). Il repose donc sur des *ressources limitées*, dont le plus gros calculateur a récemment été [débranché](https://blog.jupyter.org/mybinder-org-reducing-capacity-c93ccfc6413f) fin avril (pas de chance), ce qui peut rendre la procédure précédente inutilisable.

## 3) Lancement sur machine distante (uniquement disponible le jour du tutoriel)
1. Se rendre sur le [serveur jupyter](http://connectme.geeps.centralesupelec.fr:555). (et accepter avec votre navigateur que le lien ne soit pas un https)
2. Se connecter avec les codes qui vous ont été donnés en début de séance.
3. Ouvrir les notebooks Jupyter présents sur l'arborescence directement via votre navigateur internet.
4. Vous pouvez maintenant interagir avec les notebooks et démarrer l'activité.

## 4) Lancement en local, *avec installation* (testée sur Windows 10)

1. Télécharger et décompresser le contenu de ce [répertoire github](https://github.com/tcherrie/tutoriel_optimisation_topologique_GDR_SEEDS) **sur votre bureau**. Pour cela cliquer sur "Code", puis "Download ZIP".
2. Télécharger et installer [Miniconda](https://docs.conda.io/en/latest/miniconda.html) avec les options par défaut correspondant à votre système
3. Ouvrir une console Anaconda Prompt (sur Windows, taper dans la barre de recherche en bas à gauche "Anaconda prompt" ; sur Linux et Mac on utilisera directement le terminal)

Désormais, on écrira la suite d'instructions suivante sur la console (vous pouvez copier les instructions et les coller dans la console par un clic droit ; appuyer sur Entrée après avoir écrit l'instruction pour l'exécuter ; appuyer sur "y" pour confirmer lorsque cela vous sera demandé) : 

4. Créer un nouvel environnement "tutoriel_optim_topo" réservé à l'activité : `conda create -n tutoriel_optim_topo python=3`
5. Activer l'environnement : `conda activate tutoriel_optim_topo`
6. Installer des packages nécessaires (500Mb) : `conda install jupyter numpy matplotlib` (appuyer sur y + entrée pour confirmer l'installation). Si un blocage apparait, fermer la console et recommencer les étapes 3, 5 et 6. Les packages déjà téléchargés ne seront pas retéléchargés, ce qui fluidifiera le processus.
7. Installer NGSolve (300Mb) : `pip install ngsolve`
8. Installer des extensions de visualisation sur les notebooks :
 - `pip install --upgrade webgui_jupyter_widgets`
 - `jupyter nbextension install --user --py webgui_jupyter_widgets`
 - `jupyter nbextension enable --user --py webgui_jupyter_widgets`

**Si une erreur apparaît à l'étape 8**, essayer `jupyter nbextension install webgui_jupyter_widgets` ; sinon passer directement à l'étape 9.

9. Lancer Jupyter : `jupyter notebook`
10. Dans l'explorateur de fichiers qui s'ouvre, sélectionner "Desktop", puis "tutoriel_optimisation_topologique_GDR_SEEDS-main"

Vous êtes arrivé dans le dossier du tutoriel, et vous pouvez démarrer le notebook de votre choix en cliquant dessus.

## 5) License

Copyright (C) 2023 Théodore CHERRIERE (theodore.cherriere@ens-paris-saclay.fr), Thomas GAUTHEY (thomas.gauthey@centralesupelec.fr)

This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with this program.  If not, see <https://www.gnu.org/licenses/>.
