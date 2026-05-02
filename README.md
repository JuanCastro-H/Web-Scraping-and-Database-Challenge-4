# 📚 Deadly Query: Crime in the SQL Bookstore (Web Scraping)

## 🕵️‍♂️ TL;DR (1 min)

An end-to-end data pipeline that:

- Scrapes books from a website  
- Enriches author data using an external API  
- Models data in a normalized relational database  
- Runs SQL queries for real analysis  
- Optimizes performance using indexes  

**Result:** incomplete data → actionable insights  

---

## 🎯 Objective

Build a system capable of:

- Scraping **all categories and books** from the website  
- Enriching author data via an external API (no manual input)  
- Designing a normalized relational database  
- Executing meaningful SQL queries  
- Optimizing performance with indexing  

---

## ⚙️ Technologies Used

- Python  
- requests  
- BeautifulSoup  
- pandas  
- sqlite3  
- concurrent.futures (multithreading)  
- matplotlib  

---

## 🎯 Problem

The original dataset (*Books to Scrape*):

- Does not include authors  
- Does not support complex analysis  
- Is not structured for real-world querying  

---

## 💡 Solution

A system was built that:

1. Extracts data from the web  
2. Enriches information using an external API  
3. Designs a relational database  
4. Enables analysis through SQL  
5. Optimizes queries using indexing  

---

## 🏗️ System Architecture

Full pipeline:

1. **Scraping**
   - Category navigation  
   - Automatic pagination  
   - Structured data extraction  

2. **Transformation**
   - Data cleaning  
   - Conversion into DataFrame  

3. **Enrichment**
   - API requests based on book titles  
   - Author retrieval  
   - Parallel processing with threads  

4. **Persistence**
   - SQLite database  
   - Normalized relational model  

5. **Analysis**
   - SQL queries (joins, aggregations)  

6. **Optimization**
   - Indexing  
   - Performance benchmarking  

---

## 🧠 System Logic

### Scraping

- Full navigation across categories and pages  
- Extraction of:
  - title  
  - price  
  - rating  
  - stock  
  - category  

---

## 🗃️ Database Model

Tables:

- `books`  
- `authors`  
- `categories`  
- `book_author`  

Designed to:

- Avoid duplication  
- Maintain data integrity  
- Scale for complex queries  

---

## 🔍 Queries Performed

Key examples:

- 📈 High-rated, low-price books  
- 🏆 Top 5 highest-rated authors  
- 💰 Average price by category  
- ⚠️ Authors with 1-star books  
- 📊 Distribution of books by category  

These queries enable analysis of:

- quality  
- reputation  
- publishing trends  

---

## ⚡ Performance Optimization

A controlled test was performed:

1. Query without index  
2. Time measurement  
3. Index creation on `category_id`  
4. New measurement  

**Result:**

- Significant improvement in query speed  

---

## 📊 Visualization

Generated charts:

- Book distribution by category (bar chart)  
- Category proportions (pie chart)  

---

## 🚀 How to Run the Project

```bash
pip install requests beautifulsoup4 pandas matplotlib
```

---

### ▶️ Execution

1. Open the main notebook  
2. Run cells sequentially  

---

### ⏱️ Expected Runtime

- Scraping: 1–3 min  
- API enrichment: 3–6 min  
- Database + queries: immediate  

---

### 📂 Output

- `books.db` (structured database)  
- Enriched DataFrame  
- SQL queries ready for analysis  
- Visualizations  

---

## ✨ Possible Improvements

- Implement API caching  
- Use SQLAlchemy (ORM)  
- Add more data sources  
- Build an interactive dashboard  
- Automate the entire pipeline  

---

# 📌 Resumen en Español

Este proyecto desarrolla un pipeline de datos completo que permite extraer, enriquecer, almacenar y analizar información de libros obtenida desde la web.

El sistema parte de un dataset incompleto y lo transforma en una base de datos estructurada, lista para consultas reales y análisis más profundos.

---

## 🎯 Objetivo

- Extraer datos mediante web scraping  
- Enriquecer información con una API externa  
- Diseñar una base de datos relacional normalizada  
- Ejecutar consultas SQL para análisis  
- Optimizar el rendimiento mediante índices  

---

## ⚙️ Funcionamiento

- Scraping completo del sitio (categorías y paginación)  
- Limpieza y estructuración de datos  
- Enriquecimiento con información de autores  
- Almacenamiento en SQLite  
- Consultas SQL para análisis  
- Optimización mediante indexación  

---

## 📊 Capacidades del sistema

- Integración de múltiples fuentes de datos  
- Procesamiento paralelo (multithreading)  
- Modelo relacional escalable  
- Análisis mediante SQL  
- Visualización de datos  

---

## 🚨 Características destacadas

- Pipeline end-to-end  
- Enriquecimiento automático con API  
- Uso de concurrencia para eficiencia  
- Optimización con índices  
- Visualización clara de resultados  

---

## 🧠 Conclusión

El proyecto demuestra cómo transformar datos incompletos en información útil mediante un flujo estructurado.

Permite:

- Mejorar la calidad de los datos  
- Facilitar la toma de decisiones  
- Optimizar consultas  
- Escalar análisis complejos  

En esencia, convierte un dataset limitado en una fuente rica de conocimiento.