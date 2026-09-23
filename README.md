<h1 align="center">Nido Coworking</h1>

<p align="center">
  App móvil de reserva de espacios de coworking<br>
  <strong>Bootcamp React Native Zero to Hero</strong> — semanas 01 a 04
</p>

---

## <img src="assets/icons/target.svg" width="20" height="20" alt=""> 1. Qué es

**Nido Coworking** es la app de un edificio de coworking de 5 pisos en Bogotá.
El usuario explora los espacios disponibles, los consulta en detalle y guarda
sus favoritos para reservarlos después.

| | |
| --- | --- |
| **Dominio asignado** | Coworking Space |
| **Elemento del dominio** | `Space` — un espacio reservable del edificio |
| **Pantalla principal** | Catálogo de espacios con búsqueda |
| **Pantallas secundarias** | Detalle del espacio · Guardados |
| **Alcance de este repositorio** | Semanas 01 a 04 del bootcamp |

### El catálogo

El edificio ofrece **6 tipos de espacio** y el catálogo tiene **12 espacios**
(2 por tipo), con precios de referencia en pesos colombianos por hora:

| Tipo | Espacios | Capacidad | Desde |
| --- | --- | --- | --- |
| Escritorio flexible | Ventanal Norte (p3) · Zona Lounge (p2) | 1 persona | $ 10.000 / hora |
| Escritorio dedicado | Ala Silenciosa (p3) · Estudio 4B (p4) | 1 a 2 personas | $ 18.000 / hora |
| Sala de juntas | Aurora (p5) · Mirador (p5) | 8 a 12 personas | $ 45.000 / hora |
| Oficina privada | Nido 2A (p2) · Nido 4C (p4) | 3 a 6 personas | $ 60.000 / hora |
| Cabina fónica | Individual Norte (p3) · Dúo Ventana (p3) | 1 a 2 personas | $ 6.000 / hora |
| Sala de eventos | Auditorio Nido (p1) · Taller Creativo (p1) | 16 a 40 personas | $ 85.000 / hora |

Los seis tipos de espacio, sus pisos y precios son la base del modelo de datos
(`src/types/index.ts`) y del catálogo (`src/data/mockData.ts`).

---

## <img src="assets/icons/calendar-week.svg" width="20" height="20" alt=""> 2. Roadmap semana a semana

Cada semana del bootcamp es **un commit** y agrega exactamente lo que pide su
proyecto:

| Semana | Qué pide el bootcamp | Qué agrega este proyecto |
| :---: | --- | --- |
| **01** | App de pantalla única con tarjetas: imagen, 2 textos con estilos distintos, acción `Pressable`, header del dominio, `StyleSheet`, TypeScript | Proyecto Expo + dominio definido + `HomeScreen` con 4 tarjetas y header |
| **02** | `FlatList` (10+ items) + búsqueda en tiempo real + estado vacío + `KeyboardAvoidingView` + constantes de tema + `useMemo`/`useCallback` | Catálogo de 12 espacios, buscador, estado vacío y `src/theme` |
| **03** | Tab Navigator + Stack anidado, params tipados, Ionicons, detalle y favoritos | `RootNavigator` (Tab + Stack), `DetailScreen` y `SavedScreen` |
| **04** | Store Zustand compartido, badge en el tab bar en tiempo real, botón Guardar/Quitar | `savedStore` de Zustand, badge dinámico y pantalla de guardados |

---

## <img src="assets/icons/badge-check.svg" width="20" height="20" alt=""> 3. Entregables del bootcamp

Lo que pide cada semana y dónde está en este repositorio:

| Semana | Entregable | Estado |
| :---: | --- | --- |
| 01 | App funcional en simulador iOS y/o Android | [Capturas](#4-capturas-de-pantalla) |
| 01 | Mínimo 3 tarjetas con datos del dominio | `src/data/mockData.ts` — 4 espacios |
| 01 | Código subido al repositorio con el nombre del dominio en `app.json` | `app.json` — `"name": "coworking-space"` |
| 01 | Screenshot o grabación de la app | [Capturas](#4-capturas-de-pantalla) |
| 02 | Lista con mínimo 8 elementos del dominio | 12 espacios |
| 02 | Búsqueda en tiempo real funcionando | `src/screens/HomeScreen.tsx` |
| 02 | README con descripción del dominio | Secciones 1 y 5 de este README |
| 02 | README con captura de pantalla y decisiones de diseño | Secciones 4 y 5 |
| 03 | Tab + Stack con params tipados | `src/navigation/` |
| 03 | Capturas de las 3 pantallas (Home, Detail, Favorites) | [Capturas](#4-capturas-de-pantalla) |
| 03 | README actualizado con el dominio y la implementación | Este README |
| 04 | Store Zustand con badge en tiempo real | `src/stores/savedStore.ts` |
| 04 | Capturas de Home, Detail y Saved | [Capturas](#4-capturas-de-pantalla) |

**Estado técnico:** `pnpm exec tsc --noEmit` sin errores · Metro empaqueta los 926
módulos de la app · los 4 commits del historial son reproducibles.

---

## <img src="assets/icons/camera.svg" width="20" height="20" alt=""> 4. Capturas de pantalla

Las capturas se toman desde el dispositivo o el simulador con la app corriendo
(`pnpm start`). Guardar en la carpeta [`capturas/`](capturas/) con estos nombres:

| Archivo | Semana que lo pide | Pantalla |
| --- | :---: | --- |
| `01-home-tarjetas.png` | 01 | Catálogo con las tarjetas |
| `02-busqueda.png` | 02 | Buscador filtrando (ej. escribiendo `sala`) |
| `02-estado-vacio.png` | 02 | Estado vacío con un término sin resultados |
| `03-detalle.png` | 03 | Detalle de un espacio con su ficha |
| `03-guardados.png` | 03 | Pestaña de favoritos |
| `04-badge.png` | 04 | Tab bar con el badge de guardados |

**Cómo tomar cada captura:**

- **Teléfono Android:** botones *Volumen abajo + Encendido* a la vez.
- **iPhone:** *Botón lateral + Volumen arriba*. Las capturas quedan en Fotos.
- **Emulador Android (Android Studio):** el ícono de cámara de la barra lateral.
- **Simulador iOS (Xcode):** menú *File → Save Screen* (o `Cmd + S`).
- **Windows + teléfono por cable:** `adb exec-out screencap -p > captura.png`
  (requiere [platform-tools](https://developer.android.com/tools/releases/platform-tools)
  y la depuración USB activada).

---

## <img src="assets/icons/pen.svg" width="20" height="20" alt=""> 5. Decisiones de diseño

Las que conviene poder justificar en la revisión:

**El dominio es el catálogo, no las reservas.** Una reserva necesita backend
(calendario, disponibilidad, usuarios) y el bootcamp llega hasta el estado
global en memoria en la semana 04. Modelar el catálogo de espacios permite
trabajar con datos mock de forma honesta.

**"Guardados" en lugar de un carrito.** El coworking no vende productos: se
guardan espacios para reservarlos después. Es el equivalente funcional del
carrito que propone el bootcamp, con el vocabulario del dominio.

**Precios en COP por hora.** Es el modelo real del negocio (pago por uso) y da
un campo numérico que formatear (`formatCOP`) y reutilizar en varias pantallas.

**Imágenes locales en vez de URLs.** El enunciado acepta ambas. Locales
(`require`) para que la app se vea bien sin conexión y no dependa de que un
enlace externo siga vivo.

**Un solo `Pressable` por tarjeta.** Toda la tarjeta es la acción: así el
feedback visual (`pressed`) está garantizado sin anidar elementos interactivos.

**Sistema de tema desde la semana 02.** Los colores y medidas viven en
`src/theme`, no escritos a mano en cada `StyleSheet`. Cambiar el acento del
dominio es editar una línea.

**Iconografía: solo íconos de línea.** Todas las marcas gráficas de la app son
variantes `-outline` de Ionicons (`business-outline`, `bookmark-outline`,
`search-outline`, `close-outline`): trazo sin relleno y sin fondo. El estado
activo se comunica con color, no con un glifo relleno. En la documentación se
usan los SVG de `assets/icons/`, también de solo trazo.

---

## <img src="assets/icons/terminal.svg" width="20" height="20" alt=""> 6. Cómo ejecutar

### Requisitos

- **Node.js 22 o superior** (la LTS 24 es la recomendada)
- **pnpm 10.28.0**
- **Expo Go** en el teléfono ([Android](https://play.google.com/store/apps/details?id=host.exp.exponent) · [iOS](https://apps.apple.com/app/expo-go/id982107779))

```bash
npm install -g pnpm@10.28.0     # solo la primera vez
```

### Instalar y arrancar

```bash
pnpm install     # instala las dependencias exactas del package.json
pnpm start       # arranca Expo y muestra el código QR
```

En la terminal de Expo: `a` para Android, `i` para iOS, o escanear el QR con
Expo Go (el teléfono y el computador deben estar en la misma red WiFi).

---

## <img src="assets/icons/badge-check.svg" width="20" height="20" alt=""> 7. Verificación

```bash
pnpm exec tsc --noEmit                       # TypeScript estricto, sin salida = sin errores
pnpm exec expo export --platform android     # comprueba que Metro empaqueta la app
```

Ambos deben terminar sin errores en cada semana.

**Prueba funcional completa (semana 04):**

1. La pestaña *Guardados* arranca sin badge y con el estado vacío.
2. Abrir un espacio, tocar *Guardar*: el botón pasa a *Guardado*.
3. Volver atrás: el badge de la pestaña ya muestra **1**.
4. Guardar dos espacios más: el badge muestra **3**.
5. En *Guardados*, quitar uno con el ícono de cerrar: el badge baja a **2**.
6. *Limpiar todo*: la lista queda vacía y el badge desaparece.
7. El buscador filtra por nombre, tipo, descripción y piso.

---

## <img src="assets/icons/folder.svg" width="20" height="20" alt=""> 8. Estructura del proyecto

```
coworking-space/
├── App.tsx                 Punto de entrada (NavigationContainer + SafeAreaProvider)
├── index.js                Registro del componente raíz (registerRootComponent)
├── app.json                Configuración de Expo
├── expo-env.d.ts           Tipos del entorno Expo/Metro (require de imágenes)
├── assets/
│   ├── icons/              Íconos SVG de línea usados en esta documentación
│   └── spaces/             Fotos locales de los espacios
├── capturas/               Capturas de pantalla de cada semana
└── src/
    ├── components/         ItemCard
    ├── data/               mockData (12 espacios, sin backend)
    ├── navigation/         RootNavigator + tipos de params
    ├── screens/            HomeScreen · DetailScreen · SavedScreen
    ├── stores/             savedStore (Zustand)
    ├── theme/              COLORS · TYPOGRAPHY · SPACING · RADIUS
    ├── types/              Space · SpaceType · SPACE_TYPE_LABEL
    └── utils/              formatCOP · formatCapacity
```

---

## <img src="assets/icons/git-branch.svg" width="20" height="20" alt=""> 9. Historia de commits

Un commit por semana, con el nombre de cada semana del bootcamp:

```
Semana 04 — Estado Global con Zustand
Semana 03 — React Navigation 7
Semana 02 — Listas, Inputs y Estilos
Semana 01 — Core Components y Flexbox
```

Cada commit agrega exactamente lo que pide el proyecto de esa semana, en orden:
del componente único con tarjetas hasta el estado global con Zustand.

```bash
git log --oneline    # ver el historial
```

---

## <img src="assets/icons/pen.svg" width="20" height="20" alt=""> 10. Notas de configuración

Tres cosas que **no** vienen bien en los starters del bootcamp (rama `main`) y
que este proyecto trae resueltas:

**1. Entry point roto.** Los starters usan `"main": "expo/AppEntry"` (y la
semana 04, `expo-router/entry`), que ya no existen en Expo SDK 57: la app
compila pero arranca en **pantalla en blanco**. Aquí se usa el patrón de la
rama `fix/starter-entrypoints-and-config`: un `index.js` con
`registerRootComponent(App)` y `"main": "index.js"`.

**2. `app.json` obsoleto.** Los starters declaran `"sdkVersion": "53.0.0"` y
apuntan a `icon`/`splash`/`adaptiveIcon` que no existen. Aquí se omiten y la
versión del SDK la resuelve el paquete `expo`.

**3. `StatusBar` con `backgroundColor`.** El starter de la semana 02 usa una
prop que ya no existe en `expo-status-bar` de SDK 57, así que ese archivo no
compila. Aquí se omite.

---

<p align="center">
  <strong>Nido Coworking</strong> · Proyecto de dominio del bootcamp React Native Zero to Hero<br>
  <sub>Semanas 01 a 04 · Expo SDK 57 · React Native 0.86 · TypeScript 6.0</sub>
</p>
