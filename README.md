# ProfileApp - Pantalla de Perfil con Jetpack Compose

Una pantalla de perfil moderna construida con **Kotlin + Jetpack Compose** y Material Design 3.

## ✨ Características

| Elemento | Implementación |
|---|---|
| Layout base | `Scaffold` con `TopAppBar` |
| Tarjeta principal | `ElevatedCard` centrada con `RoundedCornerShape(24.dp)` |
| Avatar | `Icon` (Person) dentro de `Box` con `CircleShape` |
| Nombre | `Text` con `headlineLarge` + `FontWeight.Bold` |
| Carrera | `Text` con `titleMedium` en color teal |
| Habilidades | 3 × `AssistChip` (Kotlin, Compose, Android) |
| Botón de contacto | `Button` que lanza un `Snackbar` con el correo |
| Alternar tema | `IconButton` en `TopAppBar` que alterna claro/oscuro |

## 🎨 Paleta de colores

```
Primary / Teal    →  #00ACC1
Avatar BG         →  #B2EBF2
Avatar Icon       →  #00838F
Dark Background   →  #121B27
Dark Surface      →  #1E2A38
Light Background  →  #EFF6FB
```

## 📁 Estructura del proyecto

```
ProfileApp/
├── app/
│   └── src/
│       └── main/
│           └── java/com/example/profileapp/
│               └── MainActivity.kt   ← Todo el código aquí
└── README.md
```

## 🚀 Cómo correr el proyecto

### Requisitos
- Android Studio Hedgehog o superior
- Kotlin 1.9+
- Compose BOM 2024.x
- Min SDK: 24 | Target SDK: 35

### Pasos
1. Clona el repositorio
2. Abre el proyecto en Android Studio
3. Sincroniza con Gradle
4. Corre en emulador o dispositivo físico (API 24+)

## 📦 Dependencias clave (`build.gradle.kts`)

```kotlin
dependencies {
    val composeBom = platform("androidx.compose:compose-bom:2024.06.00")
    implementation(composeBom)
    implementation("androidx.compose.ui:ui")
    implementation("androidx.compose.material3:material3")
    implementation("androidx.compose.material:material-icons-extended")
    implementation("androidx.activity:activity-compose:1.9.0")
}
```

## 🌙 Alternancia de tema

El `IconButton` en la `TopAppBar` alterna entre:
- ☀️ **Tema claro** — fondo `#EFF6FB`, superficies blancas
- 🌙 **Tema oscuro** — fondo `#121B27`, superficies `#1E2A38`

El estado se maneja con `remember { mutableStateOf(false) }` y se pasa hacia abajo como parámetro.

## 📧 Contacto

Al presionar **"Contactar"**, aparece un `Snackbar` con el correo:
```
marcats21@gmail.com
```
Con acción `"COPIAR"` (puedes implementar `ClipboardManager` para copiar al portapapeles).

---
Construido con ❤️ usando Kotlin & Jetpack Compose
