# 🎯 Guía Moderna de Commits

> Una convención elegante, visual e intuitiva para mensajes de commit que mejora la legibilidad del historial y acelera el desarrollo.

---

## 🚀 Filosofía

**Commits claros = Código mantenible**

Cada commit cuenta una historia. Esta guía te ayuda a contarla de forma visual, consistente y profesional usando emojis semánticos y una estructura predictible.

---

## ⚡ Formato Rápido

```bash
<emoji> <tipo>(<scope>): <descripción>

[cuerpo opcional]

[footer opcional]
```

### 📋 Anatomía de un Commit

```bash
✨ feat(auth): implementar autenticación con OAuth2

- Integrar Google OAuth2
- Añadir middleware de autenticación
- Crear guards para rutas protegidas

Closes #123
```

---

## 🎨 Tipos de Commit

### 🔥 **Desarrollo Principal**
| Emoji | Tipo | Descripción | Cuándo usar |
|-------|------|-------------|-------------|
| ✨ | `feat` | Nueva funcionalidad | Features, endpoints, componentes |
| 🐛 | `fix` | Corrección de errores | Bugs, hotfixes |
| 💥 | `feat!` | Breaking change | Cambios incompatibles |

### 🛠️ **Mejoras de Código**
| Emoji | Tipo | Descripción | Cuándo usar |
|-------|------|-------------|-------------|
| ♻️ | `refactor` | Reestructurar código | Optimizaciones sin cambio funcional |
| 🚀 | `perf` | Mejora de rendimiento | Optimizaciones de velocidad |
| 🎨 | `style` | Formato y estilo | Prettier, indentación, espacios |

### 🧪 **Testing & Quality**
| Emoji | Tipo | Descripción | Cuándo usar |
|-------|------|-------------|-------------|
| ✅ | `test` | Pruebas | Unit tests, integration tests |
| 🚨 | `fix` | Corrección crítica | Errores de seguridad |
| 🔒 | `fix` | Seguridad | Vulnerabilidades |

### 📝 **Documentación**
| Emoji | Tipo | Descripción | Cuándo usar |
|-------|------|-------------|-------------|
| 📚 | `docs` | Documentación | README, comentarios, wikis |
| 💡 | `docs` | Comentarios en código | JSDoc, inline comments |

### 🔧 **Configuración & Mantenimiento**
| Emoji | Tipo | Descripción | Cuándo usar |
|-------|------|-------------|-------------|
| 🔧 | `chore` | Configuración | Webpack, ESLint, package.json |
| 📦 | `build` | Sistema de build | Dependencies, CI/CD |
| 🔥 | `chore` | Eliminar código | Dead code, deprecated features |
| 🏗️ | `ci` | CI/CD | GitHub Actions, Docker |

### 🎯 **UI/UX**
| Emoji | Tipo | Descripción | Cuándo usar |
|-------|------|-------------|-------------|
| 💄 | `ui` | Interfaz de usuario | Layouts, componentes visuales |
| 📱 | `feat` | Responsive | Mobile-first, breakpoints |
| ♿ | `feat` | Accesibilidad | A11y, ARIA labels |

---

## 🎪 Scopes Modernos

### 🏗️ **Arquitectura**
- `core` - Lógica central
- `shared` - Utilidades compartidas
- `types` - TypeScript definitions
- `hooks` - React hooks personalizados
- `store` - State management (Redux, Zustand)

### 🎨 **Frontend**
- `ui` - Componentes de interfaz
- `layout` - Estructuras de página
- `theme` - Sistemas de design
- `animation` - Micro-interacciones
- `responsive` - Adaptabilidad móvil

### ⚙️ **Backend**
- `api` - Endpoints y controladores
- `auth` - Autenticación y autorización
- `db` - Base de datos y migrations
- `middleware` - Middleware personalizado
- `validation` - Schemas y validaciones

### 🛠️ **DevOps & Tools**
- `ci` - Continuous Integration
- `docker` - Containerización
- `deploy` - Deployment scripts
- `monitoring` - Logs y métricas
- `security` - Configuración de seguridad

### 📱 **Mobile & Cross-Platform**
- `navigation` - Navegación entre pantallas
- `storage` - AsyncStorage, MMKV, SecureStore
- `notifications` - Push notifications, local notifications
- `camera` - Funcionalidades de cámara
- `location` - Geolocalización y mapas
- `biometric` - TouchID, FaceID, fingerprint
- `permissions` - Permisos del dispositivo
- `offline` - Sincronización offline-first
- `native` - Módulos nativos customizados
- `expo` - Configuración y servicios de Expo

---

## ✨ Ejemplos del Mundo Real

### 🚀 **Features Modernas**
```bash
✨ feat(auth): implementar autenticación con NextAuth.js
🎯 feat(ai): integrar OpenAI API para sugerencias inteligentes
📱 feat(pwa): convertir aplicación en PWA
♿ feat(a11y): añadir navegación por teclado
```

### 🐛 **Fixes Inteligentes**
```bash
🐛 fix(api): manejar timeout en requests de terceros
🚨 fix(security): prevenir XSS en comentarios de usuario
🔒 fix(auth): cerrar sesión automática tras inactividad
💥 fix!: cambiar estructura de respuesta API v2
```

### ♻️ **Refactoring Pro**
```bash
♻️ refactor(hooks): migrar a custom hooks pattern
🚀 perf(images): implementar lazy loading con IntersectionObserver
🎨 style: migrar a CSS modules + PostCSS
🔥 chore: eliminar jQuery y migrar a vanilla JS
```

### 🧪 **Testing Avanzado**
```bash
✅ test(api): añadir tests de integración con MSW
🧪 test(e2e): implementar Playwright para UI testing
🚨 test(security): añadir tests de penetración automatizados
```

---

## ⚡ Comandos Rápidos

### 🎯 **Aliases Git Recomendados**

Añade a tu `.gitconfig`:

```ini
[alias]
    # Commits rápidos
    cf = "!f() { git add -A && git commit -m \"✨ feat: $1\"; }; f"
    cb = "!f() { git add -A && git commit -m \"🐛 fix: $1\"; }; f"
    cr = "!f() { git add -A && git commit -m \"♻️ refactor: $1\"; }; f"
    cs = "!f() { git add -A && git commit -m \"🎨 style: $1\"; }; f"
    cd = "!f() { git add -A && git commit -m \"📚 docs: $1\"; }; f"
    ct = "!f() { git add -A && git commit -m \"✅ test: $1\"; }; f"
    cc = "!f() { git add -A && git commit -m \"🔧 chore: $1\"; }; f"
    
    # Log bonito
    lg = log --oneline --decorate --graph --all
    lgs = log --oneline --decorate --graph --all --stat
```

### 🚀 **Uso de Aliases**
```bash
# En lugar de: git commit -m "✨ feat(auth): añadir login OAuth"
git cf "añadir login OAuth"

# En lugar de: git commit -m "🐛 fix(api): corregir timeout"
git cb "corregir timeout en API"
```

### 🚀 **Comandos Específicos para RN + Expo**

```ini
[alias]
    # Mobile específicos
    cm = "!f() { git add -A && git commit -m \"📱 feat(mobile): $1\"; }; f"
    cn = "!f() { git add -A && git commit -m \"🚀 feat(native): $1\"; }; f"
    ce = "!f() { git add -A && git commit -m \"⚡ feat(expo): $1\"; }; f"
    ca = "!f() { git add -A && git commit -m \"🍎 build(ios): $1\"; }; f"
    cdr = "!f() { git add -A && git commit -m \"🤖 build(android): $1\"; }; f"
    
    # NativeWind específicos
    cnw = "!f() { git add -A && git commit -m \"🎨 style(nativewind): $1\"; }; f"
    cth = "!f() { git add -A && git commit -m \"🌙 feat(theme): $1\"; }; f"
```

**Uso rápido:**
```bash
git cm "implementar drawer navigation"
git cnw "migrar componentes a NativeWind"
git ce "configurar OTA updates"
git ca "preparar build para TestFlight"
git cdr "optimizar bundle size para Play Store"
```

---

## 🎯 Checklist Pre-Commit

### ✅ **Antes de Commitear**

- [ ] **Atómico**: ¿Un solo cambio lógico?
- [ ] **Descriptivo**: ¿Explica QUÉ y POR QUÉ?
- [ ] **Emoji correcto**: ¿Representa visualmente el cambio?
- [ ] **Scope apropiado**: ¿Indica claramente el área afectada?
- [ ] **Sin typos**: ¿Gramática y ortografía correctas?
- [ ] **Builds**: ¿El código compila sin errores?

### 🚨 **Evita Estos Errores**
```bash
# ❌ Muy genérico
🔧 chore: cambios

# ❌ Sin contexto
🐛 fix: corregir bug

# ❌ Multiple responsabilidades
✨ feat: añadir login y refactorizar API y actualizar docs

# ✅ Perfecto
✨ feat(auth): implementar login con Google OAuth2
```

---

## 🎨 Herramientas Recomendadas

### 🔧 **Automatización**
- **[Commitizen](https://commitizen-tools.github.io/commitizen/)** - CLI interactivo
- **[Husky](https://typicode.github.io/husky/)** - Git hooks
- **[Conventional Changelog](https://github.com/conventional-changelog/conventional-changelog)** - Auto-generar changelogs
- **[Semantic Release](https://semantic-release.gitbook.io/)** - Versionado automático

### 📱 **React Native + Expo Tools**
- **[EAS CLI](https://docs.expo.dev/eas/)** - Build y deployment en la nube
- **[Expo Development Build](https://docs.expo.dev/development/introduction/)** - Custom dev clients
- **[Flipper](https://fbflipper.com/)** - Debugging avanzado RN
- **[Reactotron](https://infinite.red/reactotron)** - Inspector de state y API calls
- **[Metro Bundler](https://facebook.github.io/metro/)** - Optimización de bundles

### 📊 **Análisis**
- **[Git History](https://github.com/pomber/git-history)** - Visualizar cambios
- **[GitKraken](https://www.gitkraken.com/)** - Cliente Git visual
- **[Sourcetree](https://www.sourcetreeapp.com/)** - Alternativa gratuita

---

## 🎯 Ejemplos por Tecnología

### ⚛️ **React/Next.js**
```bash
✨ feat(components): crear sistema de design tokens
🎯 feat(hooks): implementar useLocalStorage con SSR support
📱 feat(responsive): añadir breakpoints con Tailwind
♻️ refactor(state): migrar Context API a Zustand
```

### 🟢 **Node.js/Express**
```bash
✨ feat(middleware): crear rate limiting inteligente
🚀 perf(db): optimizar queries con índices compuestos  
🔒 fix(security): implementar helmet y CORS estricto
🐛 fix(api): manejar gracefully conexiones WebSocket
```

### 🐍 **Python/Django**
```bash
✨ feat(models): implementar soft delete con managers
🧪 test(views): añadir tests con factory_boy
📦 build(deps): actualizar Django a LTS más reciente
♻️ refactor(serializers): simplificar con DRF viewsets
```

### 📱 **React Native + Expo + NativeWind**
```bash
✨ feat(navigation): implementar stack navigator con type safety
🎯 feat(storage): integrar AsyncStorage con MMKV para performance
📱 feat(gestures): añadir swipe gestures con react-native-gesture-handler
🎨 style(theme): migrar StyleSheet a NativeWind classes
🚀 perf(images): optimizar con expo-image y caching inteligente
🔧 chore(expo): configurar EAS Build para production
📦 build(android): generar AAB con firma automática
🍎 build(ios): configurar fastlane para App Store deployment
🔔 feat(notifications): implementar push notifications con Expo
🗺️ feat(maps): integrar MapView con markers customizados
📸 feat(camera): añadir captura de fotos con expo-camera
🎵 feat(audio): implementar reproductor con expo-av
🌐 feat(offline): cache de datos con react-query + AsyncStorage
⚡ feat(splash): crear animated splash screen con Lottie
🔒 feat(biometric): autenticación con TouchID/FaceID
📐 style(responsive): implementar sistema responsive con NativeWind
🎭 feat(animations): micro-interacciones con react-native-reanimated
🌙 feat(theme): modo oscuro dinámico con sistema preferences
🔄 feat(updates): OTA updates con expo-updates
🧪 test(components): testing con @testing-library/react-native
```

---

## 🏆 Convención Pro Tips

### 🎯 **Nivel Experto**

1. **Usa conventional commits** para automatizar releases
2. **Agrupa commits relacionados** con `fixup!` y `squash!`
3. **Referencias issues** con `Closes #123, Fixes #456`
4. **Co-authored commits** para pair programming
5. **Signed commits** para verificación de autor

### 🚀 **Flujo de Trabajo Recomendado**

```bash
# 1. Feature branch
git checkout -b feat/user-dashboard

# 2. Commits atómicos
git cf "crear componente UserCard"
git cf "implementar filtros de usuario"
git cf "añadir paginación lazy"

# 3. Squash antes del merge
git rebase -i main

# 4. Merge con mensaje descriptivo
git merge --no-ff feat/user-dashboard
```

---

## 📊 Métricas de Éxito

Un buen historial de commits te permite:

- ✅ **Revisar cambios** en segundos
- 🔍 **Debuggear** con `git bisect` eficientemente  
- 📖 **Generar changelogs** automáticamente
- 🔄 **Hacer rollbacks** seguros
- 👥 **Onboarding** rápido de nuevos devs

---

## 🎉 Conclusión

Esta convención no es solo sobre emojis bonitos - es sobre **comunicación efectiva** en tu código. 

Un commit bien escrito es una inversión en el futuro de tu proyecto y en la sanidad mental de tu equipo.

**¡Happy coding!** 🚀

---

*Última actualización: Septiembre 2025*
