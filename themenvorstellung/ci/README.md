# Einrichten von CI

Dieses Dokument beschreibt die Schritte, die getätigt werden müssen, um das Frontend und das Backend im Kubernetes Cluster zu deployen.

---

Folgende Bedingungen muss das Microservice Repository erfüllen:

1. Der Microservice muss in Frontend und Backend aufgeteilt sein, wobei sich das Frontend im Ordner *frontend* und das Backend im Ordner *backend* befindet.
2. Der *frontend* und der *backend* Ordner müssen beide ein Dockerfile beinhalten, welches ein Frontend bzw Backend Image erstellt.
3. Das Frontend muss über den Port 80 erreichbar sein.
4. Das Backend muss über den Port 8080 erreichbar sein.
5. Es muss über Github Actions ein Workflow erstellt werden, welcher den Inhalt der *workflow.yml* enthält.
6. Die Dateien *deployment.yaml*, *service.yaml* und *kustomization.yaml* müssen in das Root-Verzeichnis des Repositories kopiert werden.
7. Der Microservice wird immer dann deployed, wenn Änderungen auf den Master gepusht werden.

**Achtung**: In den Dateien *workflow.yml*, *deployment.yaml*, *service.yaml* und *kustomization.yaml* muss *MSSERVICE* durch den Namen des jeweiligen Microservices ersetzt werden.<br>Beispiel für das Repository MS_Restaurants: restaurants

# Einrichten einer persistenten Datenbank

Hier werden die Einrichtung der PostgreSQL und MongoDB Datenbanken beschrieben. Andere Datenbanken könnten ähnlich eingefügt werden. Wir stehen aber auch bei Fragen zur Verfügung.

---

## Einrichten von PostgreSQL

1. Die beiden Dateien *deployment.yaml* und *workflow.yml* müssen erweitert werden. Die Inhalte der Dateien sind in *deployment_postgresql.yaml* und *workflow_postgresql.yml* zu finden. Bitte behaltet die alten Dateinamen in eurem Repository bei.
2. Es muss wie beim letzten Mal jedes *MSSERVICE* durch den eigenen Microservice Namen ersetzt werden.
3. Es müssen in eurem Repository drei Secrets erstellt werden. Geht dazu auf Settings und anschließend links auf Secrets. Folgende Secrets müssen erstellt werden:
   1. Name: POSTGRES_USER<br>Value: Euer Benutzername
   2. Name: POSTGRES_PASSWORD<br>Value: Euer Passwort
   3. Name: POSTGRES_DB<br>Value: Euer Datenbankname (Sollte eigentlich alles selbsterklärend sein)
4. Anschließend könnt ihr euren Microservice deployen und die Datenbank testen.

## Einrichten von MongoDB

1. Die Datei *deployment.yaml* muss erweitert werden. Die Inhalte der Datei sind in *deployment_mongodb.yaml* zu finden. Bitte behaltet den alten Dateinamen in eurem Repository bei.
2. Es muss wie beim letzten Mal jedes *MSSERVICE* durch den eigenen Microservice Namen ersetzt werden.
3. Bei MongoDB werden kein Benutzername und Passwort angegeben. Zum Verbinden mit eurer Datenbank müsst ihr somit keine Anmeldedaten angeben.

**ACHTUNG**: Euer Backend muss sich über *localhost* mit der Datenbank verbinden.



