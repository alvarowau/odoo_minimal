# Odoo Minimal

Repositorio con la configuración mínima necesaria para iniciar un proyecto con **Odoo 17** de forma rápida y ordenada.

## 📦 Contenido

Este repositorio incluye:

- Archivo `docker-compose.yml` para levantar Odoo 17, PostgreSQL y pgadmin4.
- Estructura de carpetas recomendada para desarrollo de módulos personalizados.
- Ejemplo base de un módulo vacío generado con `scaffold`.
- Configuración básica de volúmenes para persistencia de datos y desarrollo.

## 🚀 Requisitos previos

- Docker
- Docker Compose
- Git
- Navegador web actualizado

## 🛠️ Instalación

1. Clonar el repositorio:

```bash
git clone https://github.com/alvarowau/odoo_minimal.git
cd odoo_minimal
```

## 🚀 Levantar los contenedores

```bash
docker-compose up -d
```

## 🌐 Acceder a Odoo

- Navegar a [http://localhost:8069](http://localhost:8069)
- Configurar la base de datos y empezar a trabajar.

## 📁 Estructura recomendada

```
odoo_minimal/
│
├── addons/              # Aquí van los módulos personalizados
├── data/                # Persistencia de la base de datos PostgreSQL
├── docker-compose.yml   # Configuración de servicios
└── README.md            # Información del proyecto
```

## ✅ Verificar que todo funciona

- Al acceder a [http://localhost:8069](http://localhost:8069), deberías poder crear una base de datos y ver la interfaz de Odoo 17.
- El directorio `addons/` ya está montado y listo para tus desarrollos.

## ✏️ Cómo crear un módulo

Dentro del contenedor de Odoo, ejecuta:

```bash
docker exec -it odoo_minimal_odoo_1 odoo scaffold nombre_modulo /mnt/extra-addons
```

## 📚 Referencias

- [Documentación oficial de Odoo 17](https://www.odoo.com/documentation/17.0/)

## 🤝 Autor

- **AlvaroWau**
- [GitHub](https://github.com/alvarowau)
