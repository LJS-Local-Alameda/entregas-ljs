# Entregas LJS

Calendario compartido de fechas de entrega comprometidas del taller. Los vendedores lo abren para ver la carga antes de ofrecer una fecha al cliente.

- Calendario mensual y lista, con filtros por tipo, vendedor y cliente.
- Avance de la muestra en sublimados (solicitada, recibida, aprobada).
- Historial de cada cambio de fecha, con quién, cuándo y motivo.
- Avisos de pedidos atrasados, por vencer y con muestra pendiente.
- Exportar e importar respaldo de pedidos en `.json` (pie de la página).

Es una página estática (`index.html`). El ingreso es con Google (Firebase Authentication) y los pedidos se guardan en Firestore. Solo las cuentas listadas en `firestore.rules` pueden ver y editar.

## Puesta en marcha

1. En [console.firebase.google.com](https://console.firebase.google.com) crea un proyecto (sin Google Analytics).
2. **Authentication > Comenzar > Google > Habilitar.** Elige un correo de soporte. Luego, en **Configuración > Dominios autorizados**, agrega `TU-USUARIO.github.io`.
3. **Firestore Database > Crear base de datos.** Modo producción, ubicación `southamerica-east1` (São Paulo).
4. **Firestore > Reglas.** Pega el contenido de `firestore.rules` con los 5 correos de Google (en minúsculas) y publica.
5. **Configuración del proyecto > Tus apps > Web (`</>`).** Registra la app y copia los valores a `firebase-config.js`.
6. En GitHub: **Settings > Pages > Deploy from a branch > `main` / `(root)`**.
7. Abre `https://TU-USUARIO.github.io/NOMBRE-DEL-REPO/` e ingresa con Google.

## Datos de clientes

Los pedidos no van en este repositorio. Los respaldos `.json` se descargan desde la página y están excluidos por `.gitignore`.
