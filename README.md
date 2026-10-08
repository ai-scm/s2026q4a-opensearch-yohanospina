# Proyecto OpenSearch

Este repositorio contiene la solución completa para la implementación técnica de OpenSearch y OpenSearch Dashboards mediante entornos contenedorizados con Docker Compose, ingesta de datasets de prueba, inserción manual de registros y exploración avanzada mediante la API REST y Dev Tools.

```

## Prerrequisitos e Instalación

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
