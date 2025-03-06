erDiagram
    EVENTO {
        int id_evento PK
        varchar tipo
        varchar ubicacion
        date fecha
    }

    CLIENTE {
        int id_cliente PK
        varchar nombre
        varchar datos_contacto
        text requerimientos
    }

    PERSONAL {
        int id_personal PK
        varchar nombre
        varchar disponibilidad
        varchar tarea
    }

    PRESUPUESTO {
        int id_presupuesto PK
        int costos_proveedores
        int pagos_realizados
        int ganancias_esperadas
    }

    ASISTENCIA {
        int id_asistencia PK
        int invitados_confirmados
        int asistentes_reales
    }

    EVENTO ||--o{ CLIENTE : "Contrata"
    EVENTO ||--o{ PERSONAL : "Asigna"
    EVENTO ||--o{ PRESUPUESTO : "Tiene"
    EVENTO ||--o{ ASISTENCIA : "Registra"
