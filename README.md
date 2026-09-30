# Jarvis

[![Versión](https://img.shields.io/github/v/release/nilerdar/jarvis-releases?label=versi%C3%B3n)](https://github.com/nilerdar/jarvis-releases/releases/latest)

Instaladores de Jarvis, el asistente de escritorio. Este repositorio solo contiene
las versiones publicadas: la app instalada comprueba aquí si hay una nueva y se
actualiza sola.

**Versión actual: 1.2.0** (tag `v1.2.0`, publicada el 30/09/2026)

## Instalación en Windows

1. Descarga [jarvis-1.2.0-setup.exe](https://github.com/nilerdar/jarvis-releases/releases/download/v1.2.0/jarvis-1.2.0-setup.exe).
2. Ábrelo. Windows puede avisar con SmartScreen (la app no está firmada):
   *Más información → Ejecutar de todas formas*.
3. Las siguientes versiones se instalan solas: Jarvis avisa cuando hay una lista.

## Instalación en Mac (Apple Silicon: M1, M2, M3…)

1. Descarga [jarvis-1.2.0.dmg](https://github.com/nilerdar/jarvis-releases/releases/download/v1.2.0/jarvis-1.2.0.dmg) y arrastra Jarvis a *Aplicaciones*.
2. La primera vez, **clic derecho sobre Jarvis → Abrir → Abrir** (la app no está firmada
   por Apple). Si macOS dice que "está dañada", abre la Terminal y ejecuta:
   `xattr -cr /Applications/Jarvis.app`
3. En Mac las actualizaciones no se instalan solas: Jarvis avisa y abre esta página
   para que descargues la nueva versión.

Requisito: tener [Claude Code](https://docs.claude.com/en/docs/claude-code) instalado y con la sesión iniciada.

## Novedades

### 1.2.0

- Jarvis entiende mejor los **listados en Excel/CSV** (órdenes de trabajo, inventarios…): cuenta, filtra, agrupa y suma con cálculo exacto en vez de "a ojo", y puede consultar el histórico de un mismo listado.
- **Comparar listados** de dos días: qué filas son nuevas, cuáles han desaparecido y cuáles han cambiado, con recuentos, ratios y proyecciones calculados por código. Puede exportar el resultado a un Excel nuevo. Las reglas se pueden ajustar con archivos en `reglas/`.
- Nuevas herramientas para **listar y ver cualquier documento** de la carpeta de conocimiento, no solo presupuestos o correos.
- **Escribir en el Panel de Avisos** (opcional, hay que configurarlo): crear y modificar avisos, eventos y tareas desde el chat. Siempre simula primero y pide confirmación, no pisa cambios hechos por otra persona, deja un historial y permite deshacer las ediciones y las tareas nuevas. No se modifica el script del Panel.
- Ligero aumento del coste por mensaje por las herramientas nuevas (~3 %).

### 1.1.0

- Panel de Avisos: Jarvis se sincroniza solo con el Google Sheet del panel (cada 10 min) y lo usa como conocimiento, incluidos los PDF/Word/Excel adjuntos enlazados.
- Nueva pestaña **Avisos** en Conocimiento: tabla con filtros y búsqueda, y el detalle de cada aviso con sus PDF.
- Versión para Mac (Apple Silicon): primera vez, clic derecho → Abrir. En Mac las actualizaciones no se instalan solas: Jarvis avisa y abre la página de descargas.

### 1.0.0

- Primera versión con instalador y actualizaciones automáticas.
- Chat con Jarvis sobre tu carpeta de conocimiento: facturas, presupuestos, Excels, contratos y correos.
- Búsqueda en los documentos, consultas e informes de gastos en PDF.
- Presupuestos: ver, editar (siempre como versión nueva) y generar el PDF para el cliente.
- Correos: leerlos, guardar adjuntos y preparar borradores de respuesta (nunca se envían solos).
- Todo funciona sin instalar Python: solo hace falta Claude Code.
