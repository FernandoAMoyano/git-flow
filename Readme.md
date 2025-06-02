# ``¿Qué es Git Flow?``
---


Git Flow es un modelo de ramificación para Git que define un conjunto estricto de reglas sobre cómo y cuándo crear y fusionar ramas. Fue creado por Vincent Driessen y se ha convertido en un estándar de la industria para equipos de desarrollo que necesitan un flujo de trabajo estructurado.


# ``Estructura de Ramas en Git Flow``
---


### ➡️Ramas Principales (Permanentes)

#### 1. **main (o master)**
- **Propósito**: Contiene el código en producción
- **Características**: Siempre estable y desplegable
- **Fusiones**: Solo recibe código desde `release` y `hotfix`

#### 2. **develop**
- **Propósito**: Rama de integración para desarrollo
- **Características**: Contiene las últimas funcionalidades completadas
- **Fusiones**: Recibe código desde `feature` y se fusiona hacia `release`

### ➡️Ramas Temporales (Se eliminan después del uso)

#### 3. **feature/**
- **Propósito**: Desarrollo de nuevas funcionalidades
- **Nomenclatura**: `feature/nombre-funcionalidad`
- **Origen**: Se crea desde `develop`
- **Destino**: Se fusiona de vuelta a `develop`
- **Ejemplo**: `feature/login-usuarios`, `feature/carrito-compras`

#### 4. **release/**
- **Propósito**: Preparación para una nueva versión
- **Nomenclatura**: `release/v1.2.0`
- **Origen**: Se crea desde `develop`
- **Destino**: Se fusiona a `main` y `develop`
- **Uso**: Últimos ajustes, corrección de bugs menores, actualización de versiones

#### 5. **hotfix/**
- **Propósito**: Corrección urgente en producción
- **Nomenclatura**: `hotfix/descripcion-bug`
- **Origen**: Se crea desde `main`
- **Destino**: Se fusiona a `main` y `develop`
- **Ejemplo**: `hotfix/error-pago`, `hotfix/vulnerabilidad-seguridad`