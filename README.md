# Warehouse Management System (WMS) - LogiCorp

---



This repository contains the design and implementation from scratch of a relational database for **LogiCorp**, a system focused on logistics management, warehousing, and multi-center distribution (Distribution Centers / CEDIS). 

The project was developed as a comprehensive academic deliverable to demonstrate the ability to model and implement data solutions to address real-world operational challenges.

### 🚀 Project Features

* **Complete Relational Model:** Normalized design that manages customers, employees, suppliers, inventories (racks/positions), and stock movement orders.
* **Data Integrity:** Strict use of constraints (`PRIMARY KEY`, `FOREIGN KEY`, `NOT NULL`) to ensure data consistency.
* **Automation with PL/SQL:** Server-side business logic implementation using security triggers and stored procedures with dynamic cursors.
* **Built-in Test Data:** The script includes the insertion of 20 sample records per entity to allow immediate query testing.

### 🛠️ Technologies Used

* **Database Engine:** Oracle Database
* **Language:** SQL / PL-SQL

### 📂 Repository Structure

* `Proyecto_BD.SQL`: Single script containing the entire execution sequence: environment cleanup (`DROP TABLES`), schema definition (`CREATE TABLES`), test data insertion, and the creation of analytical views, stored procedures, and triggers.

### ⚙️ Core Technical Implementation Highlights

#### 1. Business Rules Enforcement (Triggers)
* **`VALIDAR_OPERATIVO`**: Restricts inventory order manipulation exclusively to personnel with the 'OPERATIVO' (Operations) role, preventing administrative errors within the warehouse workflow.
* **`VALIDAR_AUDITOR_ADMIN`**: Secures audit integrity by allowing only 'ADMINISTRATIVO' (Administrative) profiles to log or modify the historical control records.

#### 2. Efficient Storage Logic (Procedures)
* **`Productos_Reubicacion`**: A **cursor-based** stored procedure that dynamically scans the inventory to identify heavy products that need to be relocated to lower positions for safety and space optimization.

---
*Note: This project represents a comprehensive simulation of a real operational environment, developed to demonstrate relational database architecture and data manipulation skills.*

---


Este repositorio contiene el diseño e implementación desde cero de una base de datos relacional para **LogiCorp**, un sistema enfocado en la gestión logística, almacenamiento y distribución multi-CEDIS (Centros de Distribución). 

El proyecto fue desarrollado como un entregable académico integral para demostrar la capacidad de modelar e implementar soluciones de datos robustas frente a problemáticas operativas reales.

### 🚀 Características del Proyecto

* **Modelo Relacional Completo:** Diseño normalizado que gestiona clientes, empleados, proveedores, inventarios (estantes/posiciones) y órdenes de movimiento de mercancía.
* **Integridad de Datos:** Uso estricto de restricciones (`PRIMARY KEY`, `FOREIGN KEY`, `NOT NULL`) para asegurar la consistencia de la información.
* **Automatización con PL/SQL:** Implementación de lógica de negocio directamente en el servidor mediante triggers de seguridad y procedimientos almacenados con cursores dinámicos.
* **Datos de Prueba Incorporados:** El script incluye la inserción de 20 registros por entidad para permitir pruebas de consultas inmediatas.

### 🛠️ Tecnologías Utilizadas

* **Motor de Base de Datos:** Oracle Database
* **Lenguaje:** SQL / PL-SQL

### 📂 Estructura del Repositorio

* `Proyecto_BD.SQL`: Script único que contiene toda la secuencia de ejecución: limpieza de entorno (`DROP TABLES`), creación de la estructura del esquema (`CREATE TABLES`), inserción de datos de prueba, creación de vistas analíticas, procedimientos y disparadores.

### ⚙️ Destacados Técnicos de la Implementación

#### 1. Blindaje de Reglas de Negocio (Triggers)
* **`VALIDAR_OPERATIVO`**: Restringe la manipulación de órdenes de inventario únicamente al personal con rol 'OPERATIVO', evitando errores administrativos en el flujo de almacén.
* **`VALIDAR_AUDITOR_ADMIN`**: Garantiza la seguridad de la auditoría permitiendo que solo los perfiles 'ADMINISTRATIVO' registren o modifiquen el histórico de control.

#### 2. Lógica de Almacenamiento Eficiente (Procedimientos)
* **`Productos_Reubicacion`**: Un procedimiento basado en **cursores** que recorre dinámicamente el inventario para identificar productos pesados que requieren reubicarse a posiciones inferiores por seguridad y optimización de espacios.

---
*Nota: Este proyecto representa una simulación completa de un entorno operativo real, desarrollado con fines de demostración de habilidades de arquitectura y manipulación de bases de datos relacionales.*
