# Teszt

Név: Ézsiás Gergő

## Kérdések:

1. Mit értünk egy `commit` alatt, mit tartalmaz?

A commit a fájlok módosításáról készült snapshotot tartalmazza, illetve annak szerkeszthető leírását/kommentjét.

1. Mit értünk branch alatt, mire jó?

A branch egyazon állapotból lineárisan leágaztatott verzió, melyen külön-külön lehet dolgozni, commitolni és feltölteni.

1. Hogyan jutunk egy másolathoz egy repóról?

Klónozással, vagy mint jelen esetben forkolással.

1. Mire való a `push` és `pull` parancs?

A push parancs a commitok másik (lehet távoli, de lokális is) repóba történő exportálását teszi lehetővé, míg a pull parancs egy másik repó commitjainak importálását.

1. Mire való a `.gitignore` file?

A .gitignore fálj tartalmazza azoknak a fájloknak, könyvtáraknak a nevét, amelyek a lokális repó könyvtárában találhatóak, de nem szükséges követni a módosításaikat. (untracked)

1. Hogy lehet megnézni, hogy miben változott egy file, mire tudjuk még ezt a kimenetet használni?

A git diff paranccsal lehet összehasonlítást végezni, ezzel a paranccsal lehet fájlokat, brancheket is egymáshoz viszonyítani.

1. Mi az a conflict és mi a teendőnk conlfict esetén?

Conflict különböző branchek merge-elésekor léphet fel, akkor integrálja a felhasználó a brancheket, melyek során a különböző verziójú fájlok tartalma közti eltérések okozzák a conflict-ot. A conflictok egy részét a github fel tudja oldani, amely esetben nem, ott a felhasználó manuálisan választja ki melyik verziót tartja meg a fálj tartalmi eltérései között.

1. Mi a három állapota file-oknak git szempontjából, milyen parancsokkal mozgatjuk ezek között?

untracked, modified, staged

untracked: a fálj változásait nem szükséges a git-nek követnie.
modified: a fáljt követi a git és módosítást észlel a tartalmában.
staged: a fálj változásairól snapshot készült, a fálj commitolható.

1. Milyen lépésekkel tudunk egy új file-t hozzáadni egy repóhoz?

A fáljt a lokális repó könyvtárában létrehozzuk, majd

git add új_fálj.bmi			A fálj állapotát követni kezdi a git és staged lesz.
git commit új_fálj.bmi
git push				A változtatás commitja felkerül a távoli repóba.


1. Melyik git parancsot használnád, hogy megtudd milyen állapotban van épp a repo?

git status


4. feladat

commit db6d33bc2fb48a8a313effec9d73f5bccd29abc6
Author: Mark Zuckerberg <zuck@facebook.com>
Date:   Fri Nov 8 13:08:59 2019 +0100

    Change the status endpoint to /health
    
    To follow industry standards, the endpoint responsible for the status of
    the service should live under the /health endpoint and return a bool
    value denoted by the `health` key.

commit 1d1cf3480c68b564613809bec72ed33d9a98e2d0
Author: András Maróy <andras@maroy.hu>
Date:   Fri Nov 8 14:10:54 2019 +0100


