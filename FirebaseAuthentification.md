# Firebase Authentication

Es gibt zwei Versionen für Firebase. Einmal das Admin SDK, welches nur zum Nutzer erstellen/updaten/löschen genutzt werden muss und Client Versionen, welche Einloggen und diverse Abfragen erlauben. Unter dem Client Referenz Link gibt es verschiedene Implementationen für verschiedene Sprachen. Das folgende Beispiel bezieht sich auf eine JavaScript Webnutzung.

## Links

- [Admin SDK Referenz](https://firebase.google.com/docs/reference/admin?authuser=0)

- [Client Referenz](https://firebase.google.com/docs/reference?authuser=0)

## Authentifizierungsdiagramm

Wird hier noch eingefügt...



## Initialisierung

### Firebase Javascript im HTML einbinden

```html
<script src="https://www.gstatic.com/firebasejs/7.14.2/firebase-app.js"></script>
<script src="https://www.gstatic.com/firebasejs/7.14.2/firebase-auth.js"></script>
<script src="https://www.gstatic.com/firebasejs/7.14.2/firebase-firestore.js"></script>
```



### Initialisierung im Javascript File

```javascript
//Firebase Initialisierung
var config = {
	apiKey: "AIzaSyBvTg0_QrhEvQ9UeZPH8--E2JZ55KA_u_c",
	authDomain: "smart-city-ss2020.firebaseapp.com",
	databaseURL: "https://smart-city-ss2020.firebaseio.com",
	projectId: "smart-city-ss2020",
    storageBucket: "smart-city-ss2020.appspot.com",
    messagingSenderId: "957240233717"
};

firebase.initializeApp(config);
```



## Beispiel

Ich habe ein gezipptes Beispiel von einem einfachen Login Formular hochgeladen und bereits das Firebaseprojekt mit einem Beispielnutzer angelegt zum anschauen. Dieser Nutzer hat derzeit nur eine Emailadresse und ein Passwort. Später hat der Nutzer auch einen Anzeigenamen, wo man überlegen könnte, ob man dort schon Vor und Nachnamen reinspeichert.

### Userdaten

**E-Mail:** exampleuser@test.de

**Passwort:** sgse-ss2020

