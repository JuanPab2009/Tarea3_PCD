# Tarea3_PCD

# Tarea3_PCD: API de Gestión de Usuarios

## Descripción del Proyecto

Tarea3_PCD es una API REST desarrollada como parte de un proyecto académico para la gestión de usuarios. Utiliza FastAPI para crear una interfaz robusta y eficiente, junto con SQLAlchemy para la interacción con la base de datos.

## Características Principales

- Creación de usuarios con validación de email único
- Obtención de información de usuario por ID
- Actualización de información de usuario
- Eliminación de usuarios
- Manejo de errores para IDs no existentes y emails duplicados
- Autenticación mediante API Key para todos los endpoints

## Tecnologías Utilizadas

- Python 3.12
- FastAPI
- SQLAlchemy
- Pydantic
- SQLite (como base de datos)

## Requisitos Previos

- Python 3.12 o superior
- pip (gestor de paquetes de Python)
- Conocimientos básicos de APIs REST y línea de comandos

## Instalación y Configuración

1. Clonar el repositorio:
   ```bash
   git clone https://github.com/tu-usuario/Tarea3_PCD.git
   cd Tarea3_PCD

2. Crear y activar un entorno virtual:
   ```bash
   python3 -m venv venv
   source venv/bin/activate  # En Windows use: venv\Scripts\activate
   ```

3. Instalar las dependencias:
   ```bash
   pip install -r requirements.txt
   ```

4. Configurar la variable de entorno para la API Key:
   Cree un archivo `.env` en la raíz del proyecto con el siguiente contenido:
   ```
   API_KEY=su_api_key_secreta
   ```

## Uso

1. Iniciar el servidor:
   ```bash
   uvicorn main:app --reload
   ```

2. Acceder a la API:
   - La API estará disponible en `http://localhost:8000`
   - Documentación interactiva (Swagger UI): `http://localhost:8000/docs`

3. Utilizar los endpoints:
   - POST `/users/`: Crear un nuevo usuario
   - GET `/users/{user_id}`: Obtener información de un usuario
   - PUT `/users/{user_id}`: Actualizar información de un usuario
   - DELETE `/users/{user_id}`: Eliminar un usuario

   Nota: Todos los endpoints requieren una API Key válida en el parámetro de consulta `access_token`.

## Estructura del Proyecto

```
Tarea3_PCD/
│
├── main.py           # Punto de entrada de la aplicación y definición de endpoints
├── models.py         # Definición de modelos de SQLAlchemy
├── database.py       # Configuración de la base de datos
├── README.md         # Este archivo
├── requirements.txt  # Dependencias del proyecto
└── .env              # Archivo de configuración (no incluido en el repositorio)
```
