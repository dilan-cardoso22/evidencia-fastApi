## API de Gestión de Facturación ##  

API REST desarrollada con FastAPI para administrar clientes, facturas y transacciones. El proyecto utiliza SQLModel como ORM y SQLite como base de datos, permitiendo realizar operaciones CRUD y calcular el valor total de las facturas.

## Características ## 
 
* Gestión de clientes.
* Gestión de facturas.
* Gestión de transacciones.
* Cálculo automático del valor total de una factura.
* Base de datos SQLite.
* Documentación automática con Swagger UI.
* Arquitectura modular utilizando FastAPI.

## Tecnologías Utilizadas ##

* Python 3
* FastAPI
* SQLModel
* SQLite
* Uvicorn

##  Estructura del Proyecto ##

```text
p.y.t.h.o.n/
│
├── app/
│   ├── models/
│   │   ├── clientes.py
│   │   └── facturas.py
│   │
│   ├── routers/
│   │   ├── clientes.py
│   │   ├── facturas.py
│   │   └── transacciones.py
│   │
│   ├── conexion_bd.py
│   └── main.py
│
├── requirements.txt
├── .gitignore
└── README.md
```

##  Instalación ##

### 1. Clonar el repositorio

```bash
git clone https://github.com/tu-usuario/tu-repositorio.git
cd p.y.t.h.o.n
```

### 2. Crear entorno virtual

```bash
python -m venv venv
```

### 3. Activar entorno virtual

#### Windows

```bash
venv\Scripts\activate
```

#### Linux / macOS

```bash
source venv/bin/activate
```

### 4. Instalar dependencias

```bash
pip install -r requirements.txt
```

## Ejecutar la Aplicación ##

Desde la carpeta raíz del proyecto:

```bash
uvicorn app.main:app --reload
```

El servidor quedará disponible en:

```text
http://127.0.0.1:8000
```

##  Documentación de la API ##

Swagger UI:

```text
http://127.0.0.1:8000/docs
```

ReDoc:

```text
http://127.0.0.1:8000/redoc
```

##  Base de Datos ##

La aplicación utiliza SQLite como sistema de almacenamiento.

Archivo generado automáticamente:

```text
base_datos.db
```

Las tablas se crean automáticamente al iniciar la aplicación mediante el evento startup.

##  Endpoints Disponibles ##

### Clientes

| Método | Endpoint       | Descripción            |
| ------ | -------------- | ---------------------- |
| GET    | /clientes      | Listar clientes        |
| GET    | /clientes/{id} | Obtener cliente por ID |
| POST   | /clientes      | Crear cliente          |
| PUT    | /clientes/{id} | Actualizar cliente     |
| DELETE | /clientes/{id} | Eliminar cliente       |

### Facturas

| Método | Endpoint                   | Descripción                     |
| ------ | -------------------------- | ------------------------------- |
| GET    | /facturas                  | Listar facturas                 |
| GET    | /facturas/{id}             | Obtener factura por ID          |
| GET    | /facturas/{id}/valor_total | Calcular valor total de factura |
| POST   | /facturas                  | Crear factura                   |
| PUT    | /facturas/{id}             | Actualizar factura              |
| DELETE | /facturas/{id}             | Eliminar factura                |

### Transacciones

| Método | Endpoint            | Descripción                |
| ------ | ------------------- | -------------------------- |
| GET    | /transacciones      | Listar transacciones       |
| GET    | /transacciones/{id} | Obtener transacción por ID |
| POST   | /transacciones      | Crear transacción          |
| PUT    | /transacciones/{id} | Actualizar transacción     |
| DELETE | /transacciones/{id} | Eliminar transacción       |

##  Endpoint de Prueba ##

```http
GET /
```

Respuesta:

```json
{
  "mensaje": "API funcionando"
}
```

##  Autor ##

Proyecto desarrollado como práctica de desarrollo backend utilizando FastAPI, SQLModel y SQLite. por Dilan Santiago Carreño.

##  Licencia ##

Este proyecto se distribuye con fines académicos y educativos.
