# Las Cuentas de Flor 🌸

App web instalable (PWA) para que Flor registre sus cuentas fijas y gastos del mes, reemplazando su cuaderno.

Creada para Flor por **melitalove** · Versión 1.0

## Qué hace

- Registro de pagos de Arriendo, Gas, VTR, Agua, Luz, Gasto común, Tricot, Entel y Salcobrand Pay, con foto o PDF de la boleta.
- Otros gastos por categoría (Oliver, maquillaje, farmacia, supermercado, varios y categorías nuevas).
- Avisos de vencimiento dentro de la app (3 días antes y el día del pago) y, si se activan, en el celular.
- Botón "Ir a pagar" que abre la página de pago y copia el número de cliente o RUT.
- Alerta de Oli cuando una cuenta llega más de 25% sobre su promedio.
- Cuotas de Tricot y Salcobrand Pay, que avanzan solas al registrar el pago de la tienda.
- Resumen mensual desde septiembre de 2026, con gráfico, promedio por cuenta y la cuenta que más subió.
- Resumen anual en PDF con las boletas adjuntas.
- Calculadora, notas tipo cuaderno, clima de Santiago y opción para ocultar las cifras.
- Funciona sin internet una vez instalada.

## Archivos

```
index.html              La app completa
manifest.webmanifest    Nombre, colores e íconos para instalarla
sw.js                   Permite usarla sin internet
icons/                  Ícono de la app en todos los tamaños
```

## Publicar en GitHub Pages

1. Crea un repositorio nuevo en GitHub, por ejemplo `cuentas-de-flor`.
2. Sube todos los archivos de esta carpeta a la raíz del repositorio (manteniendo la carpeta `icons`).
3. En el repositorio, entra a **Settings → Pages**.
4. En **Source** elige **Deploy from a branch**, rama `main`, carpeta `/ (root)`, y guarda.
5. En uno o dos minutos la app queda en `https://TU-USUARIO.github.io/cuentas-de-flor/`.

Desde la terminal sería:

```bash
git init
git add .
git commit -m "Las Cuentas de Flor v1.0"
git branch -M main
git remote add origin https://github.com/TU-USUARIO/cuentas-de-flor.git
git push -u origin main
```

## Instalarla en el celular de Flor

- **Android (Chrome):** abrir la dirección, tocar el menú ⋮ y elegir **Instalar app** o **Agregar a la pantalla principal**.
- **iPhone (Safari):** abrir la dirección, tocar **Compartir** y elegir **Agregar a inicio**. En iPhone los avisos al celular solo funcionan con la app instalada así (iOS 16.4 o superior).

## Primeros pasos para Flor

1. Entrar a **Ajustes → Tu RUT** y escribirlo una vez. Se guarda solo en su teléfono.
2. En **Ajustes**, tocar **Activar avisos** y aceptar.
3. Revisar en **Ajustes → Mis cuentas** que los números de cliente, días de pago y enlaces estén bien.

## Importante sobre los datos

Todo lo que Flor registra (pagos, boletas, notas, cuotas y su RUT) queda guardado **solo en su celular**, no en GitHub ni en internet. Por eso:

- Si cambia de teléfono, borra los datos del navegador o desinstala la app, la información se pierde.
- El RUT no está escrito en el código a propósito, porque este repositorio es público.

## Publicar una versión nueva

1. Haz los cambios en `index.html`.
2. Sube el número de versión en `index.html` (`const VERSION='1.0'`).
3. Cambia el nombre de la caché en `sw.js` (`const CACHE = 'cuentas-flor-v1.0'`), por ejemplo a `v1.1`.
4. Haz commit y push. El celular tomará la versión nueva la próxima vez que abra la app con internet.
