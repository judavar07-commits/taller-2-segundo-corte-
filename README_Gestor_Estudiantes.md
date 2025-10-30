# 📘 README – Gestor de Estudiantes (SQLite + MVC en Consola)

## 🧩 Descripción
Este proyecto implementa un **Gestor de Estudiantes** en **Python**, aplicando el patrón de arquitectura **MVC (Modelo–Vista–Controlador)** y el uso de **SQLite** para la persistencia de datos.  
El programa permite crear, consultar, actualizar, eliminar y buscar estudiantes almacenados en una base de datos local.

## 🎯 Objetivos
- Aplicar el patrón MVC para separar responsabilidades del código.  
- Utilizar **SQLite** como motor de base de datos embebido.  
- Manipular datos usando comandos **SQL**: `CREATE`, `INSERT`, `SELECT`, `UPDATE`, `DELETE`, `ORDER BY`, y `LIKE`.  
- Implementar una interfaz **por consola** fácil de usar.  

---

## 📁 Estructura del Proyecto

### Si usas el proyecto modular (`gestor_estudiantes_mvc/`):
```
gestor_estudiantes_mvc/
│
├── modelo/
│   └── estudiante.py        # Funciones de persistencia (SQLite)
│
├── controlador/
│   └── gestor.py            # Lógica de negocio y coordinación MVC
│
└── vista/
    └── main.py              # Interfaz por consola (menú principal)
```

### Si usas la versión unificada (`gestor_estudiantes.py`):
Todo el código está en un solo archivo.

---

## ⚙️ Requisitos
- Python 3.8 o superior  
- No requiere librerías externas (usa módulos estándar: `sqlite3`, `csv`, `pathlib`)

---

## ▶️ Ejecución

### Opción 1: Proyecto completo (carpetas MVC)
1. Abre la carpeta `gestor_estudiantes_mvc` en Visual Studio Code.  
2. Abre una terminal dentro del proyecto.  
3. Ejecuta:
   ```bash
   python vista/main.py
   ```

### Opción 2: Versión en un solo archivo
1. Abre `gestor_estudiantes.py` en Visual Studio Code.  
2. Ejecuta:
   ```bash
   python gestor_estudiantes.py
   ```

---

## 🧮 Funcionalidades del menú

| Opción | Acción | Descripción SQL |
|:------:|:--------|:----------------|
| 1 | Agregar estudiante | `INSERT INTO` |
| 2 | Listar estudiantes | `SELECT *` |
| 3 | Actualizar nota | `UPDATE estudiantes SET nota=? WHERE nombre=?` |
| 4 | Eliminar por umbral | `DELETE FROM estudiantes WHERE nota<?` |
| 5 | Buscar por nombre | `SELECT * WHERE nombre LIKE '%texto%'` |
| 6 | Listar por nota descendente | `ORDER BY nota DESC` |
| 7 | Salir del programa | Finaliza la ejecución |

---

## 🧠 Conceptos Clave
- **Modelo:** gestiona la base de datos (`sqlite3`), operaciones CRUD y persistencia.  
- **Controlador:** coordina las operaciones entre el modelo y la vista.  
- **Vista:** presenta un menú textual interactivo en la consola.  

---

## 💾 Archivos generados automáticamente
Al ejecutar el programa por primera vez, se crearán:
- `estudiantes.csv` → archivo con datos iniciales de ejemplo.  
- `estudiantes.db` → base de datos SQLite donde se almacenan los registros.  

---

## 📜 Ejemplo de uso

```
Gestor de Estudiantes — Menú
----------------------------
1. Agregar estudiante
2. Listar estudiantes
3. Actualizar nota (por nombre)
4. Eliminar registros por umbral de nota
5. Buscar por nombre (coincidencia parcial)
6. Listar ordenado por nota (descendente)
7. Salir
Seleccione opción (1-7):
```

---

## 🧾 Autor
**Juan David Aguirre Urrego**  
Curso de **Programación Avanzada**  
Universidad Distrital Francisco José de Caldas – 2025  
