# Mapa de Poder Político Argentino 🇦🇷

Este repositorio es un **mapa de poder político argentino** de acceso libre, que agrupa a los principales actores de la política nacional —funcionarios, legisladores, aliados, opositores y gobernadores— junto a sus cuentas oficiales en **X (Twitter)**.

La información se presenta como una página web generada con **GitHub Pages**, accesible en:

👉 [https://cirotron.github.io/gabinete-argentina-x](https://cirotron.github.io/gabinete-argentina-x)

---

## 📂 Estructura del repositorio

- `gabinete.json` → Base de datos con todos los grupos y miembros (cargo, nombre, cuenta de X).
- `index.html` → Página principal que renderiza los grupos dinámicamente desde el JSON.
- `style.css` → Estilos de la página.

---

## 🗂️ Grupos incluidos

| Grupo | Descripción |
|---|---|
| 🔵 **Gabinete Formal** | Ministros y funcionarios con cargo oficial en el Poder Ejecutivo |
| 🔴 **Triángulo de Hierro** | Núcleo informal y estratégico de poder: Milei, Karina y Santiago Caputo |
| 🟢 **Equipo Económico** | Funcionarios y asesores que definen la política económica y monetaria |
| 🟣 **Bloque Legislativo LLA** | Referentes de La Libertad Avanza en el Senado y Cámara de Diputados |
| 🟠 **Aliados Clave** | Fuerzas externas y socios políticos que sostienen la gobernabilidad del oficialismo |
| ⚫ **Opositores Principales** | Líderes de la oposición kirchnerista y peronista con proyección nacional |
| 🩵 **Gobernadores Dialoguistas** | Mandatarios provinciales con diálogo y apoyo legislativo al Gobierno nacional |
| 🟫 **Secretarías de la Presidencia** | Secretarios con rango ministerial que asisten directamente al Presidente |
| ⚖️ **Poder Judicial** | Miembros de la Corte Suprema de Justicia de la Nación |
| 🟡 **Oposición Legislativa Dialoguista** | Referentes del centro en el Congreso que definen la aprobación de leyes (PRO, UCR, Encuentro Federal) |
| 🚩 **Gobernadores Opositores** | Mandatarios provinciales no dialoguistas (kirchnerismo y aliados duros) |
| 👥 **Poder Sindical** | Cúpula y secretarios generales de la Confederación General del Trabajo (CGT) |
| 💼 **Poder Económico (Círculo Rojo)** | Líderes empresariales de cámaras y grandes corporaciones privadas de Argentina |

---

## 🗃️ Estructura del JSON

El archivo `gabinete.json` tiene la siguiente estructura:

```json
{
  "grupos": [
    {
      "id": "id-del-grupo",
      "nombre": "Nombre visible",
      "descripcion": "Descripción del grupo",
      "color": "#HEX",
      "miembros": [
        {
          "cargo": "Cargo del funcionario",
          "nombre": "Nombre completo",
          "x": "@handle",
          "link": "https://x.com/handle",
          "es_cuenta_institucional": true
        }
      ]
    }
  ]
}
```

> Los campos `x` y `link` pueden ser `null` si la persona no tiene cuenta oficial. Si no posee cuenta personal pero el organismo o corporación que representa sí la tiene, se incluye dicho handle con la bandera `"es_cuenta_institucional": true`.

---

## 🔄 Cómo actualizar

Para reflejar cambios en el mapa de poder:

1. Editar el archivo [`gabinete.json`](./gabinete.json): modificar miembros existentes, agregar nuevos o crear un grupo nuevo.
2. Hacer **commit** en la rama `main` (o abrir un Pull Request desde una rama).
3. GitHub Pages actualizará automáticamente la web.

### Agregar un nuevo grupo

Agregar un objeto al array `grupos` en `gabinete.json` con los campos `id`, `nombre`, `descripcion`, `color` y `miembros`. La página lo renderizará automáticamente sin tocar el HTML.

---

## 📌 Notas

- Las cuentas de X incluidas son las **oficiales o verificadas públicamente** de cada actor.
- Un mismo actor puede aparecer en más de un grupo (ej: Milei en Gabinete Formal y Triángulo de Hierro).
- Este proyecto es de acceso libre, **no oficial** y con fines informativos.
