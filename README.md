# Sistema de Automatización "Halcón"

Este repositorio contiene la planeación y el desarrollo de la aplicación web para la distribuidora de materiales **"Halcón"**. El objetivo principal es automatizar el seguimiento de pedidos y la gestión logística interna.

## Metodología de Trabajo
Para este proyecto se ha seleccionado la metodología **Scrum**. El desarrollo se dividirá en Sprints para asegurar entregas funcionales de los módulos de Ventas, Almacén y Ruta, permitiendo ajustes rápidos según las necesidades del cliente.

## Requerimientos Clave
- **Seguimiento de Pedidos:** Consulta pública mediante Número de Cliente y Factura.
- **Gestión de Roles:** Roles diferenciados para Ventas, Compras, Almacén y Ruta.
- **Evidencia Fotográfica:** Registro obligatorio de fotos de carga y entrega (exclusivo para el rol de Ruta).
- **Borrado Lógico:** Sistema de seguridad que permite ocultar y restaurar pedidos sin eliminarlos de la base de datos.

## Tecnologías Propuestas
- **Base de Datos:** MySQL / PostgreSQL.
- **Frontend:** HTML5, CSS3, JavaScript.
- **Control de Versiones:** Git & GitHub.

## Estructura del Proyecto
- `/docs`: Contiene los diagramas de Casos de Uso, Clases, BPMN y ERD.
- `/src`: Carpeta destinada al código fuente.
- `/assets`: Recursos visuales y evidencias.

##  Autor
[Luis Alonso Garcia Barron]

## Actualización Evidencia 2 - Programación de la Lógica

En esta fase, transformé los diagramas de la Evidencia 1 en un sistema funcional utilizando Laravel y MySQL.

### Implementaciones clave:
* **Modelos y Migraciones:** Creé las entidades de Pedidos (Orders), Usuarios, Roles y Evidencias, respetando las llaves foráneas para mantener la integridad de los datos.
* **Borrado Lógico:** Implementé SoftDeletes para que los registros no se eliminen permanentemente, permitiendo auditorías y recuperación de datos.
* **Flujo de Logística:** Programé la lógica para que el estatus del pedido cambie según el avance (Ordered -> In Process -> In Route -> Delivered), obligando a la carga de fotos en las etapas finales.
* **Seguridad:** El sistema diferencia entre consultas públicas (por número de factura) y el panel administrativo protegido.
