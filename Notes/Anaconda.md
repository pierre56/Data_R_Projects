# Installation Anaconda

## Tuto / Doc
https://www.datacamp.com/community/tutorials/installing-anaconda-windows

## Install

Installation compliquée

Créé un environnement "Full_install" qui comprend tous les composants
Tentative de le faire marcher pour l'installer a Audelor

## Installation presque réussie
Il suffit de prendre le dossier de l'environnement dans le répertoire
> C:\ProgramData\Anaconda3\envs

Et l'intégrer sur un autre poste

## VSCode est marqué comme nom présent
correspond aux librarys c# de microsoft

### Error
('Connectivity Error', 'Please check your internet connection is working.')

## Installation de VSCode

[Page téléchargement visualstudio code](https://code.visualstudio.com/)

[Tentative Tuto](https://stackoverflow.com/questions/43351596/activating-anaconda-environment-in-vscode/45092632)

https://marketplace.visualstudio.com/items?itemName=ms-python.anaconda-extension-pack



### Select Interpreter


1. shift + cmd + P
2. Search Select Interpreter
3. Select env  in anaconda3 env

# Toujours des soucis, plus rien ne se lance

### Error
    anaconda qt platform plugin "windows" in ""

https://stackoverflow.com/questions/47299757/app-failed-to-start-because-it-could-not-find-qt-platform-plugin-windows-in

https://anaconda.org/conda-forge/qtconsole

## Config
(base) C:\ProgramData\Anaconda3>conda info

     active environment : base
    active env location : C:\ProgramData\Anaconda3
            shell level : 1
       user config file : C:\Users\p.ledorze\.condarc
 populated config files : C:\Users\p.ledorze\.condarc
          conda version : 4.5.11
    conda-build version : 3.15.1
         python version : 3.7.0.final.0
       base environment : C:\ProgramData\Anaconda3  (writable)
           channel URLs : https://repo.anaconda.com/pkgs/main/win-64
                          https://repo.anaconda.com/pkgs/main/noarch
                          https://repo.anaconda.com/pkgs/free/win-64
                          https://repo.anaconda.com/pkgs/free/noarch
                          https://repo.anaconda.com/pkgs/r/win-64
                          https://repo.anaconda.com/pkgs/r/noarch
                          https://repo.anaconda.com/pkgs/pro/win-64
                          https://repo.anaconda.com/pkgs/pro/noarch
                          https://repo.anaconda.com/pkgs/msys2/win-64
                          https://repo.anaconda.com/pkgs/msys2/noarch
          package cache : C:\ProgramData\Anaconda3\pkgs
                          C:\Users\p.ledorze\AppData\Local\conda\conda\pkgs
       envs directories : C:\ProgramData\Anaconda3\envs
                          C:\Users\p.ledorze\AppData\Local\conda\conda\envs
                          C:\Users\p.ledorze\.conda\envs
               platform : win-64
             user-agent : conda/4.5.11 requests/2.19.1 CPython/3.7.0 Windows/10 Windows/10.0.16299
          administrator : True
             netrc file : None
           offline mode : False

## Modifcation du fichier de config
> C:\Users\p.ledorze\.condarc

    proxy_servers:
        http: http://10.128.152.1:3128
        https: https://10.128.152.1:3128

> conda update --all

> conda config --set auto_update_conda True --system

> conda config --show

## Paths

>echo %PATH%

(base) C:\ProgramData\Anaconda3>where python
C:\ProgramData\Anaconda3\python.exe
C:\ProgramData\Anaconda3\envs\Full_install_clean\python.exe

(base) C:\ProgramData\Anaconda3>where conda
C:\ProgramData\Anaconda3\Library\bin\conda.bat
C:\ProgramData\Anaconda3\Scripts\conda.ex


## Création nouvel env


### Info environment
conda info --envs
conda info

### Create environment
conda create --name Satan
conda activate Satan

### List des packages dans l'environment
conda list --explicit
conda list --explicit > spec-file.txt


## The easiest way to save the packages from an environment to be installed in another computer is:
> conda list -e > req.txt

then you can install the environment using
>conda create -n new environment --file req.txt



### Install pip

Il n'est pas recommandé d'utiliser PIP et Conda en mm temps.
https://stackoverflow.com/questions/20994716/what-is-the-difference-between-pip-and-conda
mais dans certains cas c'est quand mm bien pratique...

conda install -n Satan pip
source activate Satan
pip <pip_subcommand>

### Installation de packages
https://conda.io/docs/user-guide/getting-started.html#managing-packages


conda install anaconda
(beaucoup de packages + dépendances)

## RecursionError('maximum recursion depth exceeded',)
Soucis récurrent, doute si lié au proxy ou si lié a un big de conda

Impossible de finir une Installation de package via conda

https://github.com/conda/conda/issues/6960
