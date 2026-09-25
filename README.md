# Cainiao Horarios

Aplicacion web publica para consultar horarios operativos de forma segura.

Este repositorio esta preparado para GitHub Pages y no debe contener:

- Google Sheets corporativos.
- Exportaciones completas del horario.
- IDs, nombres, cedulas, correos o datos personales de agentes.
- Credenciales, tokens, URLs privadas o llaves de API.

## Objetivo

Publicar una interfaz web estatica donde el usuario pueda consultar informacion de horarios mediante una conexion segura pendiente de implementar.

La fuente real de horarios debe vivir fuera del repositorio publico. La app solo debe consumir datos ya filtrados, anonimizados o entregados por un servicio intermedio con permisos controlados.

## Estado actual

- Estructura base para GitHub Pages.
- Pantalla inicial sin datos reales.
- Glosario publico de codigos operativos.
- Workflow de despliegue para GitHub Pages mediante GitHub Actions.

## Glosario operativo

| Codigo | Significado |
| --- | --- |
| H | Hotline |
| E | Email |
| C | Falsa Entrega |
| L | Pudo / Locker |
| P | P1 |
| Q | Otras Quejas |
| A | Adicional Falsa Entrega |
| J | Justificantes |
| U | Consultoria |
| T | Call Out |
| S | Consultoria Pudo-Locker |
| R | Consultas Frecuentes Off Line |
| Z | Ausencia con culpabilidad de agente |
| OFF | Desconexion por peticion de TL |
| N | No programada |
| Vacio | Break |

## Desarrollo local

No requiere dependencias para la primera version.

Abre `index.html` en el navegador o sirve la carpeta con cualquier servidor estatico.

```bash
python3 -m http.server 8080
```

## GitHub Pages

El repositorio incluye `.github/workflows/pages.yml`.

Cuando el repositorio exista en GitHub:

1. Subir los archivos a la rama `main`.
2. Ir a `Settings > Pages`.
3. Seleccionar `GitHub Actions` como fuente de despliegue.
4. Ejecutar el workflow `Deploy static site to GitHub Pages`.

## Seguridad

Antes de conectar horarios reales, revisar [docs/SECURITY.md](docs/SECURITY.md).
