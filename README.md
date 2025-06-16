# 📦 Modelo de Datos OLTP – Sistema de Abastecimiento

Este repositorio contiene un proyecto completo de diseño y desarrollo de una base de datos transaccional (OLTP) para un sistema de abastecimiento del sector retail. Incluye el modelado estructurado, creación física en **MySQL Workbench**, carga de datos simulados y visualización analítica en Power BI.

## 🛠️ Tecnologías utilizadas

- **MySQL Workbench**: Creación de base de datos real, normalización y ejecución de scripts SQL.
- **Power BI**: Visualización de indicadores operativos y estratégicos del sistema.
- **draw.io**: Documentación estructural y análisis de requerimientos.

---

## 📄 Archivos incluidos

- `Modelado de datos - DEP.drawio`: archivo maestro del análisis completo del sistema (contexto, modelo lógico, físico y objetivos).
- `modelo-abastecimiento.pdf`: versión exportada en PDF para lectura rápida.
- `Dashboard_Compras_2024.pbix`: tablero dinámico con KPIs y visuales conectados a la base OLTP.
- `scripts_mysql.sql` (opcional si lo tienes): script completo de creación y carga de datos en MySQL Workbench.

---

## 🧩 Estructura del modelo de datos

- 6 tablas normalizadas: `categoria`, `producto`, `proveedor`, `producto_proveedor`, `orden_compra`, `detalle_orden`.
- Claves primarias y foráneas bien definidas.
- Datos simulados del año 2024 para pruebas analíticas realistas.

---

## 📊 Indicadores en Power BI

- Total de órdenes y unidades compradas
- Valor total de compras
- Top productos más comprados
- Proveedores con mayor volumen
- Segmentadores por proveedor y producto

---

## 🎯 Objetivo del proyecto

> Desarrollar una base de datos OLTP funcional en MySQL Workbench con soporte para análisis posterior en Power BI, representando un flujo operativo real de compras y abastecimiento.

---

## 👨‍🏫 Contexto académico

Proyecto desarrollado como entrega práctica basada en el archivo del profesor: `Modelado de datos - DEP.drawio`, que contiene el análisis completo del negocio, el modelo conceptual y físico, y la lógica transaccional del sistema.

---
