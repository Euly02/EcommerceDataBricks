<div align="center">

# <img width="24" height="24" alt="shopping-cart" src="https://github.com/user-attachments/assets/1da27076-6bda-418c-a54c-52d1f14578a2"/> Ecommerce con DataBricks
### Proyecto de ETL con Databricks - Medallion Architecture <img width="24" height="24" alt="medallion" src="https://github.com/user-attachments/assets/9a4ec107-285b-42d4-a095-9a16d7b2c783" />

[![Databricks](https://img.shields.io/badge/Databricks-FF3621?style=for-the-badge&logo=databricks&logoColor=white)](https://databricks.com/)
[![Azure](https://img.shields.io/badge/Azure-0078D4?style=for-the-badge&logo=microsoft-azure&logoColor=white)](https://azure.microsoft.com/)
[![PySpark](https://img.shields.io/badge/PySpark-E25A1C?style=for-the-badge&logo=apache-spark&logoColor=white)](https://spark.apache.org/)
[![Delta Lake](https://img.shields.io/badge/Delta_Lake-00ADD8?style=for-the-badge&logo=delta&logoColor=white)](https://delta.io/)
[![CI/CD](https://img.shields.io/badge/CI%2FCD-GitHub_Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white)](https://github.com/features/actions)



</div>

## 📖 Descripción del Proyecto
Este proyecto implementa un pipeline ETL completo utilizando la Arquitectura Medallion (Bronze → Silver → Gold) en Databricks con Unity Catalog. El objetivo es procesar y analizar datos de e-commerce brasileño para generar insights de negocio mediante dashboards interactivos.

## 🎯 Objetivos

- ✅ Implementar arquitectura Medallion en Databricks
- ✅ Procesar datos de e-commerce con PySpark
- ✅ Crear métricas de negocio accionables
- ✅ Desarrollar dashboards interactivos
- ✅ Aplicar mejores prácticas de ingeniería de datos

## 🏆 Características Principales

- Ingesta automatizada desde Azure Storage usando Managed Identity
- Transformaciones complejas con PySpark (window functions, agregaciones, joins)
- Calidad de datos con validaciones y limpieza
- Seguridad mediante permisos granulares en Unity Catalog

## 🏗️ Arquitectura
### Arquitectura Medallion
<img width="914" height="566" alt="image" src="https://github.com/user-attachments/assets/9bf04084-6002-4a64-a23f-9ac1f51edfc4" />

## 📊 Datasets
Brazilian E-Commerce Public Dataset by Olist

- Fuente: Kaggle
- Período: 2016-2018
- Registros: ~100,000 órdenes
- Formato: 6 archivos CSV

## 🚀 Instalación y Configuración
### Prerrequisitos

✅ Cuenta de Azure con suscripción activa
✅ Databricks Workspace configurado
✅ Unity Catalog habilitado
✅ Azure Storage Account (Data Lake Gen2)
✅ Managed Identity configurada

## 📁 Estructura del Proyecto
```
proyecto-etl-ecommerce/
│
├── README.md                          # ✅ Este archivo - Documentación principal
├── .gitignore                         # Archivos ignorados por Git
│
├── .github/                           # GitHub Actions (CI/CD)
│   └── workflows/
│       └── deploy.yaml                # Pipeline de deployment
│
├── datasets/                          # 📂 Datasets descargados
│   ├── olist_orders_dataset.csv
│   ├── olist_order_items_dataset.csv
│   ├── olist_customers_dataset.csv
│   ├── olist_products_dataset.csv
│   ├── olist_order_payments_dataset.csv
│   ├── olist_geolocation_dataset.csv
│   └── product_category_name_translation.csv
│
├── dashboard/                         # ✅ Dashboards y Apps
│   ├── Delivery_metricas.pdf                
│   ├── Metrics Ventas Category.pdf    # Configuración de Databricks App
│   └── Metrics ventas mensual.pdf     # SQL queries para dashboards
│
├── reversion/                         # ✅ Scripts de revocación
│   └── revoke_permissions             # REVOKE statements para seguridad
│
├── proceso/                           # ✅ Scripts ETL en PySpark
│   ├── Ingest_customers.py            # Ingesta de customers
│   ├── Ingest_location.py             # ingesta de location
│   ├── ingest_order_items.py          # ingesta de order items
│   ├── Ingest_Orders.py               # Ingesta de ordenes
│   ├── ingest_payments.py             # ingesta de payments
│   └── ingest_product_categories.py   # ingesta de categoria de productos
│   ├── ingest_productos.py            # Ingesta de productos
│   ├── Transform_customers.py         # Transformaciones de customers
│   ├── Transform_order_items.py       # Transformaciones de order items
│   ├── Transform_orders.py            # Transformaciones de ordenes
│   ├── Transform_payments.py          # Transformaciones de payments
│   ├── Transform_products.py          # Transformaciones de productos
│   ├── Load_delivery_metrics.py       # Cargar metricas delivery
│   ├── Load_ventas_categoria.py       # Cargar metricas de ventas de categoria
│   └── Load_ventas_mensuales.py       # Cargar metricas de ventas mensuales
│
├── scripts/                           # ✅ Scripts de preparación de ambiente
│   ├── preparacion_de_ambiente        # Preparar ambiente
│
├── seguridad/                         # ✅ Scripts de seguridad
│   ├── Permissions                    # GRANT statements por rol
│
└── certificaciones/                   # ✅ Certificaciones databricks
    ├── certificacion1.png             
    ├── certificacion2.png             
```

## 🛠️ Tecnologías

<div align="center">

| Tecnología | Propósito |
|:----------:|:----------|
| ![Databricks](https://img.shields.io/badge/Azure_Databricks-FF3621?style=flat-square&logo=databricks&logoColor=white) | Motor de procesamiento distribuido Spark |
| ![Delta Lake](https://img.shields.io/badge/Delta_Lake-00ADD8?style=flat-square&logo=delta&logoColor=white) | Storage layer con ACID transactions |
| ![PySpark](https://img.shields.io/badge/PySpark-E25A1C?style=flat-square&logo=apache-spark&logoColor=white) | Framework de transformación de datos |
| ![ADLS](https://img.shields.io/badge/ADLS_Gen2-0078D4?style=flat-square&logo=microsoft-azure&logoColor=white) | Data Lake para almacenamiento persistente |
| ![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=github-actions&logoColor=white) | Automatización CI/CD |
| ![Databricks](https://img.shields.io/badge/Azure_Databricks-FF3621?style=flat-square&logo=databricks&logoColor=white) | DataBricks Dashboards |  Visualización |

</div>


---

## ⚙️ Requisitos Previos

- ☁️ Cuenta de Azure con acceso a Databricks
- 💻 Workspace de Databricks configurado
- 🖥️ Cluster activo (nombre: `cluster_SD`)
- 🐙 Cuenta de GitHub con permisos de administrador
- 📦 Azure Data Lake Storage Gen2 configurado

---

## 🚀 Instalación y Configuración

### 1️⃣ Clonar el Repositorio

```bash
git clone https://github.com/Euly02/EcommerceDataBricks.git
```

### 2️⃣ Configurar Databricks Token

1. Ir a Databricks Workspace
2. **User Settings** → **Developer** → **Access Tokens**
3. Click en **Generate New Token**
4. Configurar:
   - **Comment**: `GitHub CI/CD`
   - **Lifetime**: `90 days`
5. ⚠️ Copiar y guardar el token

### 3️⃣ Configurar GitHub Secrets

En tu repositorio: **Settings** → **Secrets and variables** → **Actions**

| Secret Name | Valor Ejemplo |
|------------|---------------|
| `DATABRICKS_HOST` | `https://adb-xxxxx.azuredatabricks.net` |
| `DATABRICKS_TOKEN` | `dapi_xxxxxxxxxxxxxxxx` |

### 4️⃣ Verificar Storage Configuration

```python
storage_path = "abfss://raw@adlsprojectsmartdata.dfs.core.windows.net"
```

<div align="center">

✅ **¡Configuración completa!**

</div>

---

## 💻 Uso

### 🔄 Despliegue Automático (Recomendado)

```bash
git add .
git commit -m " feat: mejoras"
git push origin master
```

**GitHub Actions ejecutará**:
- 📤 Deploy de notebooks a `/etl/scripts`
- 🔧 Creación del workflow `WF_ECOMMERCE`
- ▶️ Ejecución completa:  Bronze → Silver → Gold
- 📧 Notificaciones de resultados

### 🖱️ Despliegue Manual desde GitHub

1. Ir al tab **Actions** en GitHub
2. Seleccionar **Deploy ETL**
3. Click en **Run workflow**
4. Seleccionar rama `main`
5. Click en **Run workflow**

#
<div align="center">

**Proyecto**: Data Engineering - Arquitectura Medallion  
**Tecnología**: Azure Databricks + Delta Lake + CI/CD  
**Última actualización**: 2026


</div>
