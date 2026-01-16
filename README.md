# 🕷️ Scraping – Backend de Datos

## 📌 Descripción General

El proyecto **Scraping** corresponde al **backend del sistema Cliente Scraping**, encargado de **extraer, procesar y exponer información** mediante técnicas de **web scraping** y una **API en Python**.

Este módulo obtiene datos (ranking FIFA), los almacena localmente y los expone para ser consumidos por un cliente frontend (React).

---

## 🎯 Objetivo del Proyecto

* Extraer información desde una fuente web.
* Procesar y estructurar los datos.
* Almacenar la información en archivos y base de datos.
* Exponer los datos mediante una API.

---

## 🛠️ Tecnologías Utilizadas

* **Python 3**
* **Web Scraping**
* **API REST (Flask / FastAPI)**
* **SQLite**
* **JSON**

---

## 📁 Estructura del Proyecto

```
Scraping/
├── 📁 __pycache__/
│
├── 📄 .gitignore
├── 📄 api.py
├── 📄 fifa_ranking.json
├── 📄 ranking.db
├── 📄 requerimientos.txt
└── 📄 scraper.py
```

---

## 🧠 Arquitectura del Sistema

### 🕷️ `scraper.py`

* Realiza el proceso de **scraping web**.
* Obtiene información del ranking FIFA.
* Procesa y normaliza los datos.
* Guarda los resultados en:

  * Archivo JSON (`fifa_ranking.json`)
  * Base de datos SQLite (`ranking.db`)

---

### 🌐 `api.py`

* Implementa una **API REST**.
* Expone los datos almacenados para su consumo.
* Permite que el frontend (React) consulte la información.

Ejemplo de endpoints esperados:

```
GET /ranking
GET /ranking/{pais}
```

---

### 🗄️ Base de Datos (`ranking.db`)

* Base de datos SQLite.
* Almacena el ranking FIFA estructurado.

---

### 📄 `fifa_ranking.json`

* Archivo de persistencia alternativa.
* Facilita el consumo rápido de datos.

---

## ▶️ Ejecución del Proyecto

### 📦 Instalación de dependencias

```bash
pip install -r requerimeintos.txt
```

### ▶️ Ejecutar scraping

```bash
python scraper.py
```

### ▶️ Ejecutar API

```bash
python api.py
```

---

## 🔁 Flujo Completo del Sistema

1. `scraper.py` obtiene los datos desde la web.
2. Los datos se procesan y almacenan.
3. `api.py` expone los datos vía API.
4. El frontend React consume la información.

---

## 📈 Ejemplo de Uso

```json
{
  "pais": "Argentina",
  "ranking": 1,
  "puntos": 1850
}
```

---

## 🚀 Mejoras Futuras

* Manejo de errores HTTP.
* Automatización del scraping.
* Autenticación de la API.
* Despliegue en la nube.
* Cache de resultados.

---

## 💼 Enfoque para Entrevista

Este proyecto demuestra:

* Web scraping real.
* Backend en Python.
* Creación de API REST.
* Integración backend–frontend.
* Persistencia de datos.

---

## 👨‍💻 Autor

**Juan Escobar**
Estudiante de Desarrollo de Software

---

## 📄 Licencia

Proyecto de uso académico y demostrativo.
