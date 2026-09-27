# Restaurante App - Semana 15

**Estudiante:** Janneth Talía Males Conejo


## Conceptos fundamentales de manejo de eventos

Aplicación de escritorio desarrollada en Python con Tkinter como continuación del proyecto restaurante_app.

En esta semana se incorpora el manejo de eventos mediante botones y funciones callback para realizar el registro y consulta de ventas, manteniendo la arquitectura modular y la persistencia mediante archivos JSON.

## Estructura del proyecto

restaurante_app/
├── datos/
│   ├── productos.json
│   ├── usuarios.json
│   └── ventas.json
├── modelos/
│   ├── producto.py
│   ├── usuario.py
│   └── venta.py
├── servicios/
│   ├── archivo_servicio.py
│   └── restaurante_servicio.py
├── ui/
│   ├── login_view.py
│   └── main_view.py
├── assets/
│   ├── icons/
│   └── logo/
├── main.py
└── README.md

## Funcionalidades

Se mantienen las funcionalidades de las semanas anteriores:

- Inicio de sesión.
- Consulta de usuarios.
- Gestión de productos.
- Persistencia de usuarios y productos.

Además, se incorporó:

- Registro de ventas.
- Selección de usuario y producto.
- Visualización de ventas en una tabla.
- Persistencia de las ventas en ventas.json.
- Actualización de la tabla después de registrar una venta.

## Manejo de eventos

Los botones de la interfaz utilizan command= para ejecutar funciones callback.

El flujo principal es:

Usuario
↓
Botón o componente
↓
command=
↓
Callback
↓
RestauranteServicio
↓
Persistencia
↓
Respuesta en la interfaz

La interfaz recibe las acciones del usuario, mientras que RestauranteServicio contiene la lógica de las operaciones y ArchivoServicio se encarga de la lectura y escritura de los archivos JSON.

## Ventas

Las ventas se almacenan en:

datos/ventas.json

Cada venta registra:

- Identificación del usuario.
- Código del producto.
- Fecha y hora.

La información permanece guardada aunque la aplicación se cierre y vuelva a ejecutarse.

## Recursos gráficos

Los recursos utilizados por la interfaz se encuentran en:

assets/icons/
assets/logo/

Se utilizan imágenes para complementar los botones y el logotipo de la aplicación.

## Ejecución

Desde la carpeta del proyecto ejecutar:

python restaurante_App/main.py

## Conclusión

La Semana 15 amplía el proyecto restaurante_app se incorpora el manejo de eventos mediante command= y funciones callback, además del registro y persistencia de ventas, manteniendo la arquitectura y funcionalidades desarrolladas anteriormente.