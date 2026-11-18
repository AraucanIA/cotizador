# Cotizador Araucan IA

App de cotizaciones de Araucan IA para computador y celular. Cotiza en pesos (Chile) o en dólares (clientes internacionales, con PDF en inglés), separa los cobros únicos de los mensuales y genera el PDF con el logo, la paleta y las redes de la marca. Funciona sin internet una vez instalada.

## Qué hay en esta carpeta

| Archivo | Para qué sirve |
|---|---|
| index.html | La aplicación completa, con el logo y la tipografía Jost, **sin precios** |
| manifest.webmanifest | Nombre e íconos para instalarla como aplicación |
| sw.js | Guarda la app en el equipo para que funcione sin internet |
| icon-192.png, icon-512.png, icon-maskable-512.png, apple-touch-icon.png | Íconos de la app |

## Cómo publicarla en GitHub Pages (una sola vez, gratis)

1. En la organización **AraucanIA** de GitHub, crear un repositorio público, por ejemplo `cotizador`.
2. **Add file › Upload files**: subir todos los archivos de esta carpeta, sin cambiarles el nombre, y confirmar con **Commit changes**.
3. **Settings › Pages**: en *Branch* elegir `main` y la carpeta `/ (root)`, y guardar.
4. En uno o dos minutos queda en `https://araucania.github.io/cotizador/`.

Esta copia no trae precios: en cada equipo se cargan una vez desde Precios › Importar Excel, con el archivo de precios que se comparte por privado. Nunca subas ese Excel ni un respaldo .json al repositorio.

## Cómo instalarla en cada equipo

- **Computador (Chrome o Edge):** abrir la dirección y usar el ícono "Instalar" de la barra de direcciones, o el aviso "Instalar" dentro de la app.
- **Android (Chrome):** menú ⋮ › "Instalar aplicación" o "Agregar a pantalla principal".
- **iPhone (Safari):** botón Compartir › "Agregar a inicio".

## Uso diario

1. Elegir **Chile · CLP** o **Internacional · USD** y el ejecutivo (Humberto o Pedro).
2. Completar el cliente: nombre o empresa es obligatorio; contacto, teléfono, email, RUT y dirección son opcionales.
3. Tocar los precios de la lista. En los planes de contenido hay tres precios: mensual, 3 meses y 6 meses.
4. Ajustar cantidades, detalle o tipo de cobro en cada línea. **Agregar ítem libre** sirve para lo que no está en la lista.
5. Si corresponde, poner un descuento (en % o en $) y marcar **Sumar IVA**.
6. **Generar PDF**: el folio se asigna solo. Desde la ventana del PDF se descarga, se comparte (celular) o se abre WhatsApp con el mensaje para el cliente.

El PDF muestra el total, el abono para iniciar y el saldo, y, si hay servicios mensuales, cuánto se paga desde el segundo mes. El código QR abre el WhatsApp del ejecutivo con el mensaje "quiero aceptar la cotización N°…".

## Recomendaciones

- **Folios:** el primero es el 1032, que sigue a la planilla. Si Humberto y Pedro cotizan desde equipos distintos, usar un prefijo distinto en cada uno (Ajustes › Numeración).
- **IVA:** viene apagado porque el tarifario se publica sin IVA. Cuando la facturación esté lista, activar **Sumar IVA por defecto** en Ajustes.
- **Precios:** se editan en la pestaña Precios. Para cambiarlos en bloque: **Exportar Excel**, editar y **Importar Excel**. También se puede publicar esa planilla en Google Sheets como CSV y pegar el enlace en Ajustes.
- **Respaldo:** cada equipo guarda sus propias cotizaciones. Descargar un respaldo una vez al mes (Ajustes › Respaldo).
- **Historial:** marcar cada cotización como aceptada o rechazada para ver la conversión, y **Exportar a Excel** para llevarla a la planilla de leads.
- **Actualizaciones:** al reemplazar el index.html en GitHub, cada equipo recibe la versión nueva la próxima vez que abra la app con internet.

## Librerías y licencias

jsPDF 2.5.1 y SheetJS 0.18.5 se cargan desde cdnjs; qrcode-generator 1.4.4 (MIT, Kazuhiko Arase) desde jsDelivr. La tipografía Jost (Indestructible Type) tiene licencia SIL Open Font License 1.1.
