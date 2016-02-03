# studentmediene-training
Tulleprosjekt brukt til å lære litt om webutvikling samtidig som man bruker GitHub

- Installer [python 2.7] - vi og mange andre bruker fortsatt python 2.7
- Installer [virtualenv] - lar deg installere pakker som kun påvirker ett prosjekt
- Installer [pip] - veldig fin pakkebehandler i python
- Installer [git] - versjonskontrollsystemet alle i SM bruker
- Installer er editor som f eks [PyCharm] - er gratis når du har @ntnu.no e-post
- Importer dette prosjektet til en mappe du vil ha det i med følgende kommandoer
```sh
> cd my-project-folder  
> virtualenv env  
> source env/bin/activate  
> git clone git@github.com:viktorfa/studentmediene-training.git  
> cd studentmediene-training  
```
Nå er et tomt prosjekt lastet inn og du er i samme mappe som manage.py. Dette er filen man kan utføre viktige operasjoner i django med. F eks starte serveren lokalt og "migrere" databasen - noe som er veldig viktig og en kilde til mye hodepine.  
Installer django og start serveren med  
```sh
> pip install django
> python manage.py runserver  
```
Nå kom det sikkert en feilmelding fordi vi ikke har "migrert" databasen. Kjør derfor skriptet  
```sh
> python manage.py migrate  
```
Det som skjer er at den lager tabeller i databasen som senere skal fylles med data. Hvilke tabeller den lager kan man lage selv, men nå var det kun de som følger med default på ethvert django-prosjekt.  Start nå serveren med  
```sh
> python manage.py runserver  
```
Besøk [http://127.0.0.1:8000/] og se at det er en side der.


Du er nå i "master" branchen på git. Det er denne man får som default når man henter et prosjekt fra github eller starter et nytt prosjekt. Det er også denne som vanligvis har en helt fungerende versjon på mange prosjekter. Det er derfor dumt å jobbe direkte i denne!
```sh
> git status
> git branch
```
Lag din egen branch med følgende kommando  
```sh
> git checkout -b ditt-navn # -b er flagget som sier at branchen er ny
```
Push denne branchen opp til github med  
```sh
> git push origin ditt-navn
```
Nå ligger den ute for alle å se og du har en backup i skyen.

Nå er det bare å følge resten av en tutorial som f eks [djangogirls] sin. Prøv å bruk git til det det er godt for og lag "pull-request" til masterbranchen på GitHub.


[PyCharm]: <https://www.jetbrains.com/pycharm/>
[python 2.7]: <https://www.python.org/downloads/>
[virtualenv]: <https://virtualenv.readthedocs.org/en/latest/installation.html>
[pip]: <https://pip.pypa.io/en/stable/installing/>
[PyCharm]: <https://www.jetbrains.com/pycharm/>
[git]: <https://git-scm.com/book/en/v2/Getting-Started-Installing-Git>
[http://127.0.0.1:8000/]: <http://127.0.0.1:8000/>
[djangogirls]: <http://tutorial.djangogirls.org/en/>
