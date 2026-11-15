# Estimaciones Agrónomos · C&L Fruit

App web para celular: cada agrónomo ingresa la estimación del día siguiente y el bisemanal (kilos por día); Producción ve el consolidado y quién falta.

- **Entrada:** cuenta Microsoft de C&L (mismo registro de Entra «Entregas CyL» que usa Requisitos SAG).
- **Datos:** listas del sitio SharePoint «Producción Agrícola» (cylfruit.sharepoint.com/sites/ProduccinAgrcola):
  - `AG_Asignaciones`: productor → agrónomo (la del Mantenedor de Agrónomos). Columna `CSG` opcional: vacía = todo el productor.
  - `AG_Catalogo`: productores, CSG, predios y variedades de SDT (lo publica el Mantenedor).
  - `AG_Registros`: lo que envía cada agrónomo. Título `D|fecha|agrónomo` (diaria) o `B|año-Wsemana|agrónomo` (bisemanal).
  - `AG_Config`: qué cuenta es qué agrónomo o Producción.
- **Demo sin cuentas ni datos reales:** agregar `?demo` a la dirección (`?demo&rol=prod` para la vista de Producción).

## Puesta en marcha (una sola vez)
1. Crear un repositorio público en GitHub (por ejemplo `Estimaciones-agronomos`) y subir estos archivos.
2. Settings → Pages → Deploy from a branch → rama `main`, carpeta `/ (root)`.
3. Entra ID → Registros de aplicaciones → Entregas CyL → Autenticación → Aplicación de página única → agregar el URI de redirección de la nueva dirección (termina en `/`).
4. Abrir la dirección en el celular e instalarla desde el menú del navegador («Agregar a pantalla de inicio»).
