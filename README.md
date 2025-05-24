Proyecto Koelsa - Sistema de Gestión de Inventario
Sistema integral de gestión de inventario desarrollado en Python con interfaz gráfica Tkinter y base de datos MySQL, que integra capacidades de computación interactiva mediante IPython.

Descripción General
Koelsa es una aplicación empresarial que combina funcionalidades completas de gestión de inventario con el entorno de computación interactiva de IPython, empaquetada como un ejecutable independiente para Windows. El sistema permite realizar operaciones de inventario, gestión de cadena de suministro y análisis de datos a través de una interfaz de shell Python interactiva. Koelsa.sql:53-70

Arquitectura del Sistema
El proyecto sigue una arquitectura MVC (Modelo-Vista-Controlador) con las siguientes capas:

Capa de Datos
Base de datos MySQL: Esquema koelsa con entidades principales para productos, proveedores, almacenes y usuarios
Gestión de transacciones: Tablas de entrada y salida para movimientos de inventario
Sistema de requerimientos: Flujo de solicitudes de compra y aprobaciones
Capa de Modelo
Gestión de productos: VistaProducto.py:1-30
Gestión de proveedores: Proveedor.py:1-25
Conexión a base de datos: Sistema centralizado de conexiones
Capa de Controlador
Controlador de login: LoginControlador.py:6-20
Controlador de menú: MenuControlador.py:77-90
Capa de Vista
Interfaz gráfica Tkinter: Formularios para registro y gestión de datos
Sistema de autenticación: Login de usuarios con validación de credenciales
Características Principales
Gestión de Inventario
Registro y administración de productos con códigos internos, ubicaciones y categorías
Control de stock con entradas y salidas detalladas
Gestión de almacenes y subalmacenes
Seguimiento de maquinaria y equipos
Gestión de Proveedores
Registro completo de proveedores con datos de contacto y RUC
Asociación de productos con proveedores específicos
Gestión de precios y condiciones comerciales
Sistema de Requerimientos
Creación y seguimiento de solicitudes de compra
Flujo de aprobación con solicitadores y supervisores
Control de criterios de urgencia y presupuestos
Reportes y Análisis
Historial completo de movimientos por producto
Consultas SQL integradas para análisis de datos
Reportes de inventario y transacciones
Estructura de la Base de Datos
Entidades Principales
producto: Productos e ítems de inventario
proveedor: Proveedores y vendedores
almacen: Almacenes y ubicaciones de almacenamiento
usuario: Usuarios del sistema
Transacciones
entrada/entradaDetalle: Transacciones de ingreso de stock
salida/salidaDetalle: Transacciones de salida de stock
Requerimiento/requerimientoDetalle: Solicitudes de compra Koelsa.sql:288-305
Tecnologías Utilizadas
Python 3.12: Lenguaje principal de desarrollo
Tkinter: Framework para interfaz gráfica de usuario
MySQL: Sistema de gestión de base de datos
IPython: Entorno de computación interactiva
cx_Freeze: Empaquetado como ejecutable independiente
Instalación y Configuración
Requisitos del sistema:
Windows AMD64
MySQL Server instalado y configurado
Base de datos:
Ejecutar el script Koelsa.sql para crear el esquema y datos iniciales
Configurar las credenciales de conexión en el módulo de conexión
Ejecución:
El proyecto se distribuye como ejecutable independiente
No requiere instalación de Python en el sistema destino
Estructura del Proyecto
Proyecto/  
├── controlador/          # Controladores MVC  
│   ├── LoginControlador.py  
│   └── MenuControlador.py  
├── modelo/              # Modelos de datos  
│   └── Proveedor.py  
├── vista/               # Interfaces de usuario  
│   └── VistaProducto.py  
├── Koelsa.sql          # Esquema de base de datos  
└── build/              # Archivos de distribución  
Funcionalidades del Sistema
Autenticación
Sistema de login con validación de credenciales
Gestión de sesiones de usuario
Gestión de Productos
Registro con campos completos: part name, marca, familia, descripción
Control de unidades de medida y precios
Asignación a almacenes específicos
Control de Inventario
Entradas de stock con documentación
Salidas asociadas a proyectos y maquinaria
Trazabilidad completa de movimientos
Administración
Gestión de familias de productos
Configuración de almacenes y ubicaciones
Mantenimiento de catálogos maestros
Notes
El proyecto Koelsa representa un sistema completo de gestión empresarial que combina la robustez de una base de datos estructurada con la flexibilidad de un entorno de computación interactiva. La arquitectura MVC facilita el mantenimiento y la escalabilidad del sistema, mientras que la integración con IPython proporciona capacidades avanzadas de análisis de datos.

Wiki pages you might want to explore:
