# Hexnode MDM Skill - Guía de Instalación

Expert knowledge skill para Hexnode MDM/UEM con configuración completa de políticas para Windows, macOS, iOS, Android y más.

## ✨ Características

- **50+ categorías de políticas para macOS**
- **40+ categorías de políticas para Windows**
- **Políticas para iOS/iPadOS y Android**
- **Arquitectura y diagramas de flujo**
- **13+ escenarios de troubleshooting reales**
- **Scripts de automatización (bash y PowerShell)**
- **Integración con Hexnode API**
- **Best practices de producción**
- **Guías de testing completas**

## 📋 Requisitos

- Claude Desktop App, CLI, o cualquier implementación de Claude con soporte para skills
- Directorio de skills configurado (`~/.agents/skills/` o `~/.claude/skills/`)

## 🚀 Instalación

### Opción 1: Desde ZIP

```bash
# 1. Descomprimir el archivo
unzip hexnode-mdm-skill.zip

# 2. Copiar a tu directorio de skills
# Si usas .agents
cp -r hexnode-mdm ~/.agents/skills/

# O si usas Claude desktop app
cp -r hexnode-mdm ~/.claude/skills/

# 3. Verificar instalación
ls -la ~/.agents/skills/hexnode-mdm/SKILL.md
```

### Opción 2: Instalación manual

```bash
# 1. Crear directorio
mkdir -p ~/.agents/skills/hexnode-mdm/

# 2. Copiar archivos
# Copia SKILL.md, README.md a esa carpeta

# 3. Verificar
ls -la ~/.agents/skills/hexnode-mdm/
```

### Opción 3: Desde repositorio Git (si aplica)

```bash
cd ~/.agents/skills/
git clone <url-del-repo> hexnode-mdm
```

## ✅ Verificación

Después de instalar, verifica que el skill esté disponible:

1. **Reinicia Claude/Agent** si está corriendo
2. **Prueba el skill** con un prompt como:
   ```
   "¿Qué categorías de políticas están disponibles para Windows en Hexnode?"
   ```
3. Claude debería usar automáticamente el skill hexnode-mdm

## 📖 Uso

El skill se activa automáticamente cuando:

- Mencionas Hexnode MDM/UEM
- Preguntas sobre políticas de dispositivos
- Necesitas crear/troubleshooting scripts
- Trabajas con la API de Hexnode
- Configuras enrollment
- Implementas automations
- Troubleshooting de problemas MDM

### Ejemplos de prompts:

```
"Crea un script de PowerShell para renombrar dispositivos Windows en Hexnode"

"¿Qué políticas de seguridad están disponibles para macOS?"

"Troubleshoot: mi script en Hexnode muestra 'Pending' forever"

"¿Cómo configuro LAPS en Windows con Hexnode?"

"Explícame las diferencias entre Policies y Automations"
```

## 📁 Estructura del Skill

```
hexnode-mdm/
├── SKILL.md                    # Archivo principal del skill
├── README.md                   # Descripción general
├── SKILL_REVIEW_REPORT.md      # Reporte de revisión
└── INSTALL.md                  # Este archivo
```

## 🔧 Configuración

No requiere configuración adicional. El skill está listo para usar después de la instalación.

## 🆘 Soporte

Si tienes problemas:

1. Verifica que el archivo SKILL.md esté en la ubicación correcta
2. Reinicia Claude/Agent
3. Verifica permisos del archivo: `chmod 644 ~/.agents/skills/hexnode-mdm/SKILL.md`
4. Revisa logs de Claude si están disponibles

## 📝 Actualización

Para actualizar el skill:

```bash
# Respalda tu versión actual
cp -r ~/.agents/skills/hexnode-mdm ~/.agents/skills/hexnode-mdm.backup

# Reemplaza con la nueva versión
cp -r hexnode-mdm ~/.agents/skills/

# O si usas Git
cd ~/.agents/skills/hexnode-mdm
git pull
```

## 🤝 Contribuciones

Este skill se basa en implementaciones reales de producción. Si encuentras mejoras o casos de uso adicionales, documéntalos y compártelos.

## 📄 Licencia

Uso interno. No distribuir fuera de la organización sin autorización.

## 🏷️ Versión

- **Versión actual:** 2.0
- **Última actualización:** 2026-11-09
- **Plataformas soportadas:** macOS, Windows, iOS/iPadOS, Android, Linux, ChromeOS, tvOS, visionOS, Zebra Printers

---

**Desarrollado por:** Santiago Fernandez (santiagoagustinfernandez@gmail.com)  
**Organización:** COMPANY Technology Solutions
