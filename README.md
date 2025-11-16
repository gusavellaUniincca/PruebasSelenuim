# Pruebas Selenuim
Pruebas en selenuim para aplicacion Core de rentas test Noviembre 2025
# 📘 Guía Completa de Diagramas Mermaid

Este repositorio contiene una colección completa de ejemplos de diagramas utilizando **Mermaid**, el lenguaje de diagramación basado en texto soportado de forma nativa por GitHub.

Mermaid permite documentar procesos, arquitecturas, flujos, estados, clases, bases de datos y más, sin usar herramientas visuales externas.

---

# 📚 ¿Qué es Mermaid?

Mermaid es un lenguaje de marcado que convierte texto en diagramas dinámicos.  
Se usa ampliamente en:

- GitHub (readme, issues, PRs)
- GitLab
- Confluence
- Notion
- Obsidian
- Documentación de proyectos

Es ideal porque:

- Es fácil de mantener
- Funciona perfecto con control de versiones
- El diagrama se actualiza solo con cambios en el texto
- No necesitas herramientas externas

---

# 🧩 Diagramas incluidos en este README

1. Flowchart  
2. Sequence Diagram  
3. Class Diagram  
4. State Diagram  
5. Gantt Chart  
6. ER Diagram  
7. User Journey  
8. Pie Chart  

Puedes usar este README como referencia o plantilla en tus propios proyectos.

classDiagram
    class User {
        +string name
        +string email
        +login()
    }

    class AuthService {
        +generateJWT()
        +validateToken()
    }

    User --> AuthService
mermaid    
stateDiagram-v2
    [*] --> Desconectado
    Desconectado --> Autenticando
    Autenticando --> Autenticado
    Autenticando --> Error
    Error --> Desconectado
# Diagrama del flujo de Login



A continuación se muestra el flujo de autenticación con JWT:

```mermaid
sequenceDiagram
    participant User
    participant FE as Frontend
    participant API

    User->>FE: Ingresa credenciales
    FE->>API: Envía login
    API-->>FE: Retorna JWT
    FE->>API: Petición con Bearer Token
    API-->>FE: Respuesta OK

Nombre del Proyecto

Breve descripciÃ³n del proyecto, propÃ³sito y alcance.

------------------------------------------------------------------------

## ðŸ“š Tabla de Contenido

1.  DescripciÃ³n General
2.  Arquitectura
3.  Flujos Principales
4.  Modelado de Datos
5.  Estados del Sistema
6.  Cronograma del Proyecto
7.  ContribuciÃ³n
8.  Licencia

------------------------------------------------------------------------

## ðŸ§© DescripciÃ³n General

ExplicaciÃ³n breve del proyecto y lo que resuelve.

------------------------------------------------------------------------

## ðŸ—ï¸ Arquitectura

``` mermaid
flowchart TD
    A[Cliente] --> B[API Gateway]
    B --> C[Servicio Auth]
    B --> D[Servicio Principal]
    C --> E[Base de Datos]
    D --> E
```

------------------------------------------------------------------------

## ðŸ”„ Flujos Principales

### ðŸ” **Flujo de AutenticaciÃ³n (JWT)**

``` mermaid
sequenceDiagram
    participant U as Usuario
    participant A as API
    participant DB as Base de Datos

    U->>A: Enviar credenciales
    A->>DB: Buscar usuario
    DB-->>A: Datos del usuario
    A-->>U: Retorna JWT
```

------------------------------------------------------------------------

### ðŸ§¾ **Flujo del Proceso Principal**

``` mermaid
flowchart LR
    A[Inicio] --> B[ValidaciÃ³n]
    B -->|OK| C[Procesar]
    B -->|Error| D[Mostrar error]
    C --> E[Finalizar]
```

------------------------------------------------------------------------

## ðŸ—„ï¸ Modelado de Datos

### **Diagrama ER**

``` mermaid
erDiagram
    USER ||--o{ ORDER : hace
    ORDER ||--|{ PRODUCTO : contiene
    USER {
        int id
        string nombre
        string email
    }
    PRODUCTO {
        int id
        string nombre
        float precio
    }
```

------------------------------------------------------------------------

## ðŸ§  Estados del Sistema

``` mermaid
stateDiagram-v2
    [*] --> Inactivo
    Inactivo --> Ejecutando
    Ejecutando --> Error
    Error --> Inactivo
```

------------------------------------------------------------------------

## ðŸ“… Cronograma del Proyecto

``` mermaid
gantt
    title Cronograma
    dateFormat  YYYY-MM-DD

    section Fase 1
    PlanificaciÃ³n :a1, 2025-01-01, 7d
    DiseÃ±o :after a1, 5d

    section Fase 2
    Backend :2025-01-10, 14d
    Frontend :2025-01-15, 10d
```

------------------------------------------------------------------------

## ðŸ¤ ContribuciÃ³n

Explica cÃ³mo contribuir (PRs, issues, etc.)

------------------------------------------------------------------------

## ðŸ“„ Licencia

Indica el tipo de licencia (MIT, Apache, etc.)
