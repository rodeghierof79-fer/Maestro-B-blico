# Maestro Bíblico — PWA

Asistente de enseñanza bíblica reformada. Progressive Web App instalable en celular y computadora.

---

## Estructura del proyecto

```
maestro-biblico/
├── index.html          # App principal
├── manifest.json       # Configuración PWA
├── sw.js               # Service Worker
├── vercel.json         # Configuración de deploy
├── icons/
│   ├── icon-192.png    # Ícono Android / Chrome
│   ├── icon-512.png    # Ícono splash screen
│   └── icon-180.png    # Apple Touch Icon
├── api/
│   └── chat.js         # Proxy serverless (Vercel Function)
├── CLAUDE.md           # Contexto estable del proyecto
└── MEMORIA.md          # Memoria acumulativa del proyecto
```

---

## Deploy en Vercel

### 1. Subir a GitHub

```bash
# En la carpeta del proyecto:
git init
git add .
git commit -m "feat: Maestro Bíblico PWA inicial"

# Crear repo en github.com, luego:
git remote add origin https://github.com/TU_USUARIO/maestro-biblico.git
git branch -M main
git push -u origin main
```

### 2. Deploy en Vercel

1. Ir a [vercel.com](https://vercel.com) → New Project
2. Importar el repositorio de GitHub
3. **IMPORTANTE**: Configurar variable de entorno:
   - Nombre: `ANTHROPIC_API_KEY`
   - Valor: `sk-ant-...` (tu clave de Anthropic)
4. Click en **Deploy**

Vercel detecta automáticamente `vercel.json` y configura las Vercel Functions.

### 3. Variables de entorno en Vercel

```
Settings → Environment Variables → Add New:
ANTHROPIC_API_KEY = sk-ant-api03-...
```

---

## Instalar como app

### Android (Chrome/Edge)
1. Abrí la URL de la app en Chrome o Edge
2. Menú (⋮) → "Agregar a pantalla de inicio" o "Instalar app"
3. O esperá el banner automático de instalación

### iPhone/iPad (Safari)
1. Abrí la URL en Safari
2. Botón Compartir → "Agregar a pantalla de inicio"
3. Confirmá el nombre y tocá "Agregar"

### Computadora (Chrome/Edge)
1. Abrí la URL en Chrome o Edge
2. Ícono de instalación (⊕) en la barra de direcciones
3. O Menú → "Instalar Maestro Bíblico..."

---

## Desarrollo local

Para probar localmente sin Vercel, podés usar cualquier servidor estático con soporte para variables de entorno, o simplemente configurar la clave API directamente en la app (engranaje ⚙):

```bash
# Con Python:
python3 -m http.server 8080

# Con Node.js (npx):
npx serve .
```

**Nota**: En desarrollo local, el endpoint `/api/chat` no funcionará (requiere Vercel Functions). La app automáticamente intenta usar la clave API guardada localmente como fallback.

---

## Clave API

- Obtenela en: [console.anthropic.com](https://console.anthropic.com) → API Keys
- **Producción**: configurar como variable de entorno en Vercel (más seguro)
- **Local/prueba**: configurar en la app con el botón ⚙

---

## Doctrina y teología

Ver `CLAUDE.md` para el marco teológico completo.
Ver `MEMORIA.md` para el historial de decisiones y aprendizajes.
