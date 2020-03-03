# BlockArt Backend

## Hier befindet sich die Backendlogik für das Projekt BlockArt
Die Datenbank befindet sich auf einem MySql Server mit der URL [sql88.your-server.de] (sql88.your-server.de).
Deployt ist das Projekt auf einem Heroku Server und erreichbar unter der URL http://blockarthdm.herokuapp.com
(Note: Da es sich um einen free Account handelt, geht der Server nach 30 min Inaktivität in den Standby und benötigt bei einem neuen API Aufruf ca 5 Sekunden bis er wieder reagiert.)

Heroku cli und heroku login required.

Um die logs auf dem Heroku Server zu sehen wird der Befehl `heroku logs -t --app blockarthdm` verwendet.

Neustart der App über Heroku Console `heroku ps:restart --app blockarthdm`.

Weiteren git remote head hinzufügen: `heroku git:remote -a blockarthdm`.

Nur einen Subfolder auf den Heroku Server deployen: `git subtree push --prefix foldername heroku master`

Um das Projekt auszuführen, ist Node.js nötig. 

Um alle dependecies zu installieren muss nur in dem backend Ordner der Befehl 'npm install' ausgeführt werden. 
Installiert wird dann:
- Express (node.js framework)
- MySql (MySql driver für Node)
- Body-parser (handels the post body request)

Um das Projekt lokal zu starten wird der Befehl `node index` ausgeführt.

Wenn man einzelne APIs testen will geht das am besten mit Postman, welchen man seperat installieren muss. Danach muss das `BlockArt.postman_collection.json´ welches sich im backend/test Ordner befindet importiert werden. In diesem habe ich bereits alle API Aufrufe definiert.
