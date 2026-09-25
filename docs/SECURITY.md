# Seguridad y privacidad

Este repositorio es publico. Todo lo que se suba aqui puede quedar visible para terceros.

## Reglas

- No subir archivos del Google Sheet corporativo.
- No subir exportaciones CSV, XLSX, capturas o copias de pestañas con datos reales.
- No incluir nombres, IDs, correos, cedulas, telefonos o cualquier dato personal de agentes.
- No guardar tokens, credenciales, claves de Apps Script, URLs privadas ni secretos.
- No exponer endpoints que devuelvan la base completa de horarios.

## Conexion recomendada

La app publica debe conectarse a una capa intermedia. Esa capa debe:

- Validar permisos.
- Recibir una consulta puntual.
- Devolver solo los campos necesarios.
- Omitir datos personales cuando no sean indispensables.
- Registrar errores sin guardar datos sensibles.

## Opciones para la siguiente fase

| Opcion | Uso recomendado | Riesgo principal |
| --- | --- | --- |
| Apps Script Web App privado | Prototipo rapido con control de acceso | Configuracion incorrecta de permisos |
| Backend propio | Mayor control de autenticacion y logs | Mas mantenimiento |
| Datos anonimizados publicados | Consultas generales sin personas | Puede quedar desactualizado |

## Antes de publicar cambios

Revisar que el commit no contenga:

- Archivos `.xlsx`, `.csv`, `.json` o `.txt` con datos reales.
- Capturas de pantalla del horario.
- Variables con nombres como `TOKEN`, `SECRET`, `API_KEY` o `SHEET_ID`.
