# Firechat

Chat con firebase y login con redes sociales (google y twitter)

Para iniciar esta aplicación tiene que ir primero a (https://firebase.google.com) y obtener una cuenta de firebase. Crear un proyecto nuevo llamado firechat

En database de firestore elija Cloud Firestore

Ponga en las reglas de la database esta regla:

```
service cloud.firestore {
  match /databases/{database}/documents {
    match /{document=**} {
      allow read, write: if true;
    }
  }
}
```


Vaya a proyect overview y elija agregar firebase a tu web app copie y pegue el contenido de sus credenciales en la carpeta: environments/enviroments.ts

De la linea 9 a la 14

```
apiKey: "",
authDomain: "",
databaseURL: "",
projectId: "",
storageBucket: "",
messagingSenderId: ""

```


Navegue en su consola a la carpeta de este proyecto e instale las dependencias

```
npm install

```

Cuando termine de instalar las dependencias escriba el comando

```
ng serve

```

Abra cuantas ventanas quiera del navegador y comience a chatear

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 1.5.5.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.
