# Nexus Dashboard

> Centro de control industrial para el equipo de desarrollo — Visualiza herramientas, sinergias y actividad en tiempo real.

---

## 📋 Descripción

**Nexus Dashboard** es un panel de control tipo "War Room" que centraliza el desarrollo técnico del equipo, mostrando qué hacen los compañeros y cómo colaboran entre sí.

### Pilares

| Pilar | Descripción |
|-------|-------------|
| **Tool Grid** | Tarjetas dinámicas de repositorios GitHub con descripción, lenguajes, progreso y README |
| **Synergy Map** | Gráfico de nodos interactivo que muestra cómo las herramientas de un compañero se conectan con las de otros |
| **Dev-Pulse** | Feed de micro-actualizaciones (commits, comentarios, audios) asociados a los últimos cambios |

---

## 🏗️ Arquitectura

- **Frontend:** Next.js 14+
- **Estilado:** Tailwind CSS
- **Visualización:** react-force-graph
- **Data:** GitHub REST API (sin DB externa)
- **Config:** JSON centralizado (`config/dashboard.json`)

---

## ⚙️ Configuración

El archivo `config/dashboard.json` es el "cerebro" del dashboard:

```json
{
  "team": { ... },      // Miembros del equipo
  "repos": { ... },     // Repositorios a monitorizar
  "synergy": { ... },   // Conexiones entre miembros
  "ui": { ... },        // Theme y estilos
  "github": { ... }     // Config de API
}
```

### Agregar un nuevo miembro

```json
{
  "id": "nuevo_id",
  "name": "Nombre Apellido",
  "role": "Developer",
  "github": "username",
  "avatar": ""
}
```

### Agregar un nuevo repositorio

```json
{
  "id": "repo_id",
  "name": "nombre-repo",
  "owner": "organizacion",
  "description": "Descripción",
  "status": "alpha|stable|planning",
  "tags": ["tag1", "tag2"],
  "assignedTo": ["dev1", "dev2"]
}
```

### Definir sinergias

```json
{
  "from": "dev1",
  "to": "artist1",
  "type": "creative|technical|pipeline",
  "description": "Descripción de la conexión"
}
```

---

## 🎨 UI Theme

| Variable | Valor |
|----------|-------|
| Theme | Dark Mode |
| Estilo | Industrial / War Room |
| Color acento | `#00ff88` |
| Background | `#0a0a0a` |
| Card BG | `#1a1a1a` |

---

## 🚀 Uso

1. Clonar el repo
2. `npm install`
3. Configurar `config/dashboard.json` con los datos del equipo
4. `npm run dev`
5. Abrir `http://localhost:3000`

---

## 👥 Equipo

| Rol | Integrante | GitHub |
|-----|-----------|--------|
| PM | Igor Gopkalo Streiff | heavy_machine |
| Developer | Max Sarlija | maxsarlija |
| Developer | Manuel Mejia | pulpt37 |
| Tech Artist | Mariano Zulueta | mariano9700 |
| Tech Artist | Kalil Fiat | kalil94 |
| Tech Artist | Manuel Castellani | manucastellani |
| Tech Artist | Mauricio van der Wildt | elkronaiken |
| Tech Artist | Facundo Villarreal | facu041294 |
| Artist | Franco Ferrarello | fartvader |
| Artist | Alejandro Arteaga | arteaga.rey |

---

## 📌 Estado del Proyecto

- [x] Definición de arquitectura
- [x] Configuración centralizada (JSON)
- [ ] Implementación de Tool Grid
- [ ] Implementación de Synergy Map
- [ ] Implementación de Dev-Pulse
- [ ] Integración con GitHub API
- [ ] Despliegue

---

*Generado: 2026-04-24*
*Proyecto: Max Sarlija Academy — Desafío Viernes*