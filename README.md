# Capacitor Learning Content

Contenido educativo para la plataforma de aprendizaje de Ionic + Capacitor.

## Descripción

Este repositorio contiene todo el contenido educativo:
- Lecciones teóricas (Markdown/JSON)
- Preguntas de quizzes
- Datos para mini-juegos
- Ejemplos de código

## Estructura del Contenido

```
content/
├── modules/
│   ├── module-1-fundamentals/
│   │   ├── meta.json           # Metadata del módulo
│   │   ├── lessons/
│   │   │   ├── 01-what-is-capacitor.md
│   │   │   ├── 02-architecture.md
│   │   │   ├── 03-project-structure.md
│   │   │   ├── 04-commands.md
│   │   │   └── 05-live-reload.md
│   │   ├── quiz.json           # Preguntas del quiz
│   │   └── game-data.json      # Datos para Command Builder
│   │
│   ├── module-2-plugins/
│   │   ├── meta.json
│   │   ├── lessons/
│   │   │   ├── 01-app-plugin.md
│   │   │   ├── 02-push-notifications.md
│   │   │   ├── 03-splash-statusbar.md
│   │   │   ├── 04-keyboard-browser.md
│   │   │   ├── 05-preferences.md
│   │   │   └── 06-biometric.md
│   │   ├── quiz.json
│   │   └── game-data.json      # Datos para Plugin Matcher
│   │
│   ├── module-3-build/
│   │   ├── meta.json
│   │   ├── lessons/
│   │   │   ├── 01-web-integration.md
│   │   │   ├── 02-native-features.md
│   │   │   ├── 03-android-build.md
│   │   │   ├── 04-ios-build.md
│   │   │   └── 05-automation.md
│   │   ├── quiz.json
│   │   └── game-data.json      # Datos para Build Pipeline
│   │
│   └── module-4-stores/
│       ├── meta.json
│       ├── lessons/
│       │   ├── 01-testing-strategy.md
│       │   ├── 02-play-store.md
│       │   ├── 03-app-store.md
│       │   └── 04-fintech-compliance.md
│       ├── quiz.json
│       └── game-data.json      # Datos para Store Reviewer
│
├── code-examples/
│   ├── capacitor-config/
│   ├── plugins/
│   ├── android/
│   └── ios/
│
└── assets/
    ├── diagrams/
    └── screenshots/
```

## Formato de Archivos

### meta.json (Módulo)

```json
{
  "id": "module-1",
  "title": "Setup + Fundamentos Capacitor",
  "description": "Configurar el environment y entender la arquitectura",
  "icon": "rocket",
  "requiredXP": 0,
  "lessons": ["01-what-is-capacitor", "02-architecture", "..."],
  "estimatedTime": "2 horas"
}
```

### Lección (Markdown)

```markdown
---
id: "01-what-is-capacitor"
title: "¿Qué es Capacitor?"
description: "Introducción a Capacitor y su ecosistema"
xpReward: 10
estimatedTime: "15 min"
---

# ¿Qué es Capacitor?

Capacitor es un runtime nativo...

## Código de ejemplo

\`\`\`typescript
import { Capacitor } from '@capacitor/core';

const platform = Capacitor.getPlatform();
\`\`\`
```

### quiz.json

```json
{
  "moduleId": "module-1",
  "passingScore": 70,
  "xpReward": 50,
  "questions": [
    {
      "id": "q1",
      "text": "¿Cuál es la diferencia principal entre Capacitor y Cordova?",
      "options": [
        "Capacitor usa WebView moderno y tiene mejor integración nativa",
        "Cordova es más nuevo",
        "No hay diferencia",
        "Capacitor solo funciona en iOS"
      ],
      "correctIndex": 0,
      "explanation": "Capacitor usa WKWebView en iOS y tiene acceso directo al código nativo..."
    }
  ]
}
```

### game-data.json (Plugin Matcher)

```json
{
  "gameId": "plugin-matcher",
  "moduleId": "module-2",
  "xpReward": 100,
  "pairs": [
    {
      "useCase": "Mostrar Face ID para login",
      "plugin": "@capacitor-community/biometric",
      "hint": "Autenticación biométrica"
    },
    {
      "useCase": "Guardar token de forma segura",
      "plugin": "@capacitor/preferences",
      "hint": "Storage encriptado"
    }
  ]
}
```

## Guía de Contribución

### Escribir Lecciones

1. Usar Markdown con frontmatter YAML
2. Incluir ejemplos de código funcionales
3. Mencionar diferencias iOS vs Android cuando aplique
4. Agregar tips y warnings donde sea útil
5. Mantener un tono conversacional pero técnico

### Crear Preguntas de Quiz

1. Mínimo 10 preguntas por módulo
2. Cubrir todos los temas de las lecciones
3. Incluir explicación para cada respuesta
4. Variar dificultad (fácil → difícil)

### Datos de Mini-juegos

1. Verificar que los datos sean técnicamente correctos
2. Incluir hints útiles
3. Balancear dificultad

## Repositorios Relacionados

- [capacitor-learning-platform](https://github.com/ismaeldosil/capacitor-learning-platform) - App principal
- [capacitor-learning-docs](https://github.com/ismaeldosil/capacitor-learning-docs) - Sistema de agentes
