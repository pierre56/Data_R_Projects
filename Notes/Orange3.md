# Installation de Orange3


## Python Hint
* Use exit() or Ctrl-Z plus Return to exit

## Probleme

Installation via anaconda-navigator compliquée
Apparait comme installé mais ne se lance pas au démarrage



### Log
Traceback (most recent call last):
File "D:\Program_Files\Anaconda\envs\Full_install\Scripts\orange-canvas-script.py", line 6, in
from Orange.canvas.__main__ import main
File "D:\Program_Files\Anaconda\envs\Full_install\lib\site-packages\Orange\canvas\__main__.py", line 30, in
from Orange.canvas.application.canvasmain import CanvasMainWindow
File "D:\Program_Files\Anaconda\envs\Full_install\lib\site-packages\Orange\canvas\application\canvasmain.py", line 61, in
from ..document.usagestatistics import UsageStatistics
File "D:\Program_Files\Anaconda\envs\Full_install\lib\site-packages\Orange\canvas\document\__init__.py", line 17, in
from .schemeedit import SchemeEditWidget
File "D:\Program_Files\Anaconda\envs\Full_install\lib\site-packages\Orange\canvas\document\schemeedit.py", line 37, in
from .suggestions import Suggestions
File "D:\Program_Files\Anaconda\envs\Full_install\lib\site-packages\Orange\canvas\document\suggestions.py", line 7, in
from .interactions import NewLinkAction
File "D:\Program_Files\Anaconda\envs\Full_install\lib\site-packages\Orange\canvas\document\interactions.py", line 29, in
from ..canvas import items
File "D:\Program_Files\Anaconda\envs\Full_install\lib\site-packages\Orange\canvas\canvas\items\__init__.py", line 9, in
from .annotationitem import TextAnnotation, ArrowAnnotation
File "D:\Program_Files\Anaconda\envs\Full_install\lib\site-packages\Orange\canvas\canvas\items\annotationitem.py", line 6, in
import docutils.core
ModuleNotFoundError: No module named 'docutils'

## Solution

Fail install in
> D:\Program_Files\Anaconda\envs\Full_install\lib\site-packages\Orange

Win in
> D:\Program_Files\Anaconda\envs\Full_install

λ python -version
λ python -m pip install docutils
λ python -m pip install --upgrade pip

-----
## Installer un plugin
[faq](https://orange.biolab.si/faq/)


pip install orange3-text
conda install orange3-timeseries

## Steps
[doc Steps](https://orange.biolab.si/toolbox/)

----
For psycopg to be recognized in Orange, it needs to be installed in the same virtual environment, which is normally located in C:\Users\<usr>\Anaconda3\envs\orange3 (on Windows). For the installation to work, you’d have to run it with the proper pip, namely:

> C:\Users\<usr>\Anaconda3\envs\orange3\Scripts\pip.exe install psycopg2

## EN vrai

D:\Program_Files\Anaconda\envs\Full_install
λ python -m pip install psycopg2

D:\Program_Files\Anaconda\envs\Full_install
λ python -m pip install quantile

Redémarrage et OK


## Connection Base Postgresql

> SELECT usename FROM pg_user;

### DB Info
Postgresql
localhost:5432
Formation_postgresql/dimensions
postgres
no mdp
