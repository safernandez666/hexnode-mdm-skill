# Instalación de la skill Hexnode MDM

La skill consta de `SKILL.md` y los archivos de `references/`. Copiá la carpeta completa para que el agente pueda cargar las referencias según la tarea.

## Desde Git

Desde el directorio en el que quieras descargar el repositorio:

```bash
git clone https://github.com/safernandez666/hexnode-mdm-skill.git
mkdir -p "$HOME/.agents/skills"
cp -R ./hexnode-mdm-skill "$HOME/.agents/skills/hexnode-mdm"
```

El último comando supone que `~/.agents/skills/hexnode-mdm` **no existe**. Si ya tenés una instalación, hacé una copia de seguridad o revisala antes de reemplazarla; no mezcles versiones sin revisarlas. Para Claude u otro agente, consultá su documentación para elegir el directorio de skills que corresponda.

## Verificación

1. Comprobá que exista `~/.agents/skills/hexnode-mdm/SKILL.md` y que la carpeta `references/` acompañe al archivo.
2. Reiniciá el agente si es necesario para que descubra la skill.
3. Probá una consulta específica, por ejemplo: “¿Cómo listo todos los dispositivos de Hexnode con paginación?”

La activación y las rutas de instalación dependen del agente. Para integración con la API se necesita acceso habilitado en el tenant y una API key; no incluyas esa clave en scripts distribuidos a los dispositivos.

## Referencias históricas

Los archivos antiguos de API, el reporte de revisión y `references/legacy-skill.md` se conservan por contexto. Pueden tener errores o información obsoleta; usá las referencias actuales y contrastá los detalles con la documentación oficial de Hexnode.
