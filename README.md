# 📚 Consulta Mortal: Crimen en la Librería SQL (Web Scraping)

## 🕵️‍♂️ TL;DR (1 min)

Pipeline de datos end-to-end que:

* Extrae libros desde la web (scraping)
* Enriquece autores con API externa
* Modela datos en base relacional normalizada
* Ejecuta consultas SQL para análisis real
* Optimiza performance con índices

Resultado: datos incompletos → información accionable

---


## 🎯 Objetivo

Construir un sistema capaz de:

* Scrapear **todas las categorías y libros** del sitio
* Enriquecer autores desde una API externa (sin carga manual)
* Diseñar una base de datos relacional normalizada
* Ejecutar consultas SQL útiles
* Optimizar performance mediante índices

---

## ⚙️ Tecnologías utilizadas

* Python
* requests
* BeautifulSoup
* pandas
* sqlite3
* concurrent.futures (multithreading)
* matplotlib

---

## 🎯 Problema

El dataset original (*Books to Scrape*):

* No incluye autores
* No permite análisis complejos
* No está preparado para consultas reales

---

## 💡 Solución

Se construyó un sistema que:

1. Extrae datos desde la web
2. Enriquece información con API externa
3. Diseña una base de datos relacional
4. Permite análisis mediante SQL
5. Optimiza consultas con índice

## 🏗️ Arquitectura del sistema

Pipeline completo:

1. **Scraping**

   * Navegación por categorías
   * Paginación automática
   * Extracción estructurada

2. **Transformación**

   * Limpieza de datos
   * Conversión a DataFrame

3. **Enriquecimiento**

   * Consulta a API por título
   * Obtención de autores
   * Paralelización con threads

4. **Persistencia**

   * Base de datos SQLite
   * Modelo relacional normalizado

5. **Análisis**

   * Consultas SQL (joins, agregaciones)

6. **Optimización**

   * Indexación
   * Benchmark de performance

---

## 🧠 Lógica del sistema

### Scraping

* Navegación completa por categorías y paginación
* Extracción de:

  * título
  * precio
  * rating
  * stock
  * categoría


## 🗃️ Modelo de base de datos

Tablas:

* `libros`
* `autores`
* `categorias`
* `libro_autor`

Diseñado para:

* evitar duplicados
* mantener integridad
* escalar consultas

---

## 🔍 Consultas realizadas

Ejemplos clave:

* 📈 Libros con rating alto y bajo precio
* 🏆 Top 5 autores mejor valorados
* 💰 Precio promedio por categoría
* ⚠️ Autores con libros de 1 estrella
* 📊 Distribución de libros por categoría

Estas consultas permiten análisis de:

* calidad
* reputación
* mercado editorial

---

## ⚡ Optimización de performance

Se realizó una prueba controlada:

1. Consulta sin índice
2. Medición de tiempo
3. Creación de índice en `id_categoria`
4. Nueva medición

Resultado:

* Mejora significativa en velocidad de consulta

Esto demuestra cómo los índices impactan en sistemas reales.

---

## 📊 Visualización

Se generaron gráficos como:

* Distribución de libros por categoría (bar chart)
* Proporción de categorías (pie chart)

Esto permite interpretar los datos de forma más intuitiva.

---

## 🚀 Cómo ejecutar el proyecto

```bash
pip install requests beautifulsoup4 pandas matplotlib
```

---

### Ejecución

1. Abrir el notebook principal
2. Ejecutar celdas en orden

---

### ⏱️ Qué esperar

* Scraping: 1–3 min
* Enriquecimiento API: 3–6 min
* DB + consultas: inmediato

---

### 📂 Output

* `books.db` (base estructurada)
* DataFrame enriquecido
* Queries listas para análisis
* Visualizaciones

---

## ✨ Mejoras interesantes para el proyecto

* Implementar cache para API
* Usar SQLAlchemy para ORM
* Agregar más fuentes de datos
* Crear dashboard interactivo
* Automatizar el pipeline completo

---


