npx create-react-app reimpresion
npm install electron
npm install electron-is-dev
npm install concurrently
npm install wait-on

crear main

npm run electron-react

npx electron-builder

npm run electron-pack

https://medium.com/@duytq94/bundling-your-react-web-to-a-desktop-app-with-electron-1b19ebcf8933





import path from 'path';
import { app, BrowserWindow, shell, ipcMain } from 'electron';
import { autoUpdater } from 'electron-updater';
import log from 'electron-log';
import MenuBuilder from './menu';
import { resolveHtmlPath } from './util';
const express = require('express');
const cors = require('cors');

const expressApp = express(); // Cambiamos el nombre de la variable para evitar conflictos

const port = 5000;

// Habilita CORS para todas las rutas
expressApp.use(cors());

// Ruta que devuelve "Hola Mundo"
expressApp.get('/api/hola', (req, res) => {
  res.send('Hola Mundo');
});

// Iniciar el servidor
expressApp.listen(port, () => {
  console.log(`Servidor Express escuchando en el puerto ${port}`);
});



"start": "concurrently \"npm run start:renderer\" \"npm run start-server\"",
