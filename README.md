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



/* eslint-disable */

const sql = require('mssql');

const config = {
  user: 'sa',
  password: '12',
  server: 'DESKTOP-5H15VG0',
  database: 'test',
  options: {
    encrypt: true, // Si es necesario, dependiendo de tu configuración
    trustServerCertificate: true,
  },
};

const pool = new sql.ConnectionPool(config);

pool.connect((err) => {
  if (err) {
    console.error('Error al conectar a la base de datos:', err.message);
  } else {
    console.log('Conexión exitosa a la base de datos SQL Server');
  }
});

module.exports = pool;




mainWindow.removeMenu(); // Quita el menú de Electron
  mainWindow.maximize(); // Maximiza la ventana
  mainWindow.show(); // Muestra la ventana
