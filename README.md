# Proyecto OpenSearch: Despliegue Local, Búsqueda Facetada e Interacción REST API

Este repositorio contiene la solución completa para la implementación técnica de OpenSearch y OpenSearch Dashboards mediante entornos contenedorizados con Docker Compose, ingesta de datasets de prueba, inserción manual de registros y exploración avanzada mediante la API REST y Dev Tools.

## 📁 Estructura del Repositorio

```text
.
├── README.md                           # Documentación principal del repositorio
├── docker/
│   └── docker-compose.yml              # Configuración multi-nodo de OpenSearch y OpenSearch Dashboards
├── docs/
│   ├── opensearch_installation_guide.md # Guía paso a paso de instalación y configuración
│   └── rest_api_exploration.md         # Manual de interacción vía API REST y Dev Tools
├── payloads/
│   ├── custom_log_sample.json          # Documento JSON insertado manualmente
│   └── dsl_facet_queries.json          # Consultas Query DSL para Dev Tools y cURL
└── dashboards/
    └── sample_web_logs_dashboard.json  # Exportación de Saved Objects del Dashboard interactivo
```

## 🚀 Prerrequisitos e Instalación

### Ajuste de Memoria del Sistema Anfitrión (Linux)
Antes de iniciar los contenedores, configure la memoria virtual máxima del kernel:

```bash
sudo sysctl -w vm.max_map_count=262144
sudo swapoff -a
```

### Iniciar Servicios con Docker Compose
Navegue al directorio `docker/` y ejecute:

```bash
docker compose up -d
docker compose ps
```

Acceda a la interfaz web de OpenSearch Dashboards desde su navegador en: `http://localhost:5601`.
