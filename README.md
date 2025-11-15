# Pruebas Selenuim
Pruebas en selenuim para aplicacion Core de rentas test Noviembre 2025
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
