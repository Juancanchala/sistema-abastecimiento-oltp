# 📦 Modelo de Datos OLTP – Sistema de Abastecimiento

Este repositorio contiene un proyecto completo de diseño y desarrollo de una base de datos transaccional (OLTP) para un sistema de abastecimiento del sector retail. Incluye el modelado estructurado, creación física en **MySQL Workbench**, carga de datos simulados y visualización analítica en Power BI.

## 🛠️ Tecnologías utilizadas

- **draw.io**: Documentación estructural y análisis de requerimientos.
- **MySQL Workbench**: Creación de base de datos real, normalización y ejecución de scripts SQL.
- **Power BI**: Visualización de indicadores operativos y estratégicos del sistema.


---

## 📁 Archivos incluidos
OLTP Modelado de datos Supply – DEP.drawio: archivo maestro del análisis estructural. Incluye el contexto del negocio, el modelo lógico, físico y los objetivos del sistema de abastecimiento. Es el insumo base del proyecto, desarrollado según la guía del profesor. La base de datos fue diseñada y construida directamente en MySQL Workbench.

dashboard_compras_abastecimiento_2024.pbix: dashboard interactivo en Power BI, conectado a la base OLTP. Contiene KPIs clave, análisis por proveedor y producto, y una visualización de la evolución anual de las compras.

Proyecto OLTP – Sistema de Abastecimiento.pdf: documento exportado con el contenido completo del análisis en formato PDF para lectura rápida o entrega académica.

---

## 🧩 Estructura del Modelo de Datos
El sistema se basa en un modelo relacional normalizado desarrollado en MySQL Workbench. La estructura fue diseñada siguiendo principios OLTP para garantizar consistencia, escalabilidad y trazabilidad en las operaciones de abastecimiento.

🔹 Tablas del Modelo
categoria
Contiene las categorías a las que pertenece cada producto.
Campos clave: categoriaID, nombreCategoria.

producto
Registro maestro de productos con descripciones, precios y relación con su categoría.
Campos clave: productoID, nombreProducto, descripcion, precio, categoriaID.

proveedor
Información de los proveedores registrados en el sistema.
Campos clave: proveedorID, nombreProveedor, contacto.

producto_proveedor
Tabla puente para representar relaciones muchos a muchos entre productos y proveedores.
Campos clave: productoID, proveedorID.

orden_compra
Cabecera de cada orden emitida con fecha y proveedor asociado.
Campos clave: ordenID, fecha, proveedorID.

detalle_orden
Detalle de cada compra: productos, cantidades y precios unitarios.
Campos clave: ordenID, productoID, cantidad, precioUnitario.

🔐 Integridad y relaciones
Se definieron claves primarias y foráneas en todas las tablas para mantener integridad referencial.

Las relaciones permiten reconstruir de forma eficiente el historial completo de compras.

🗓️ Datos de prueba
El modelo fue poblado con datos simulados para el año 2024, basados en escenarios realistas del sector retail.

Estos datos permiten probar consultas, relaciones y análisis en herramientas como Power BI sin depender de información confidencial.

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


