# 🍃 MongoDB Atlas — Base de Datos NoSQL en la Nube

> Configuración de cluster MongoDB Atlas gratuito, gestión de usuarios con roles y administración de colecciones con MongoDB Compass.

---

## 📋 Descripción

Configuración de una base de datos **NoSQL en la nube** usando **MongoDB Atlas** (free tier).  
Incluye creación del cluster, gestión de usuarios con diferentes niveles de privilegios, creación de bases de datos y colecciones, e inserción de documentos.  
La conexión se gestionó desde **MongoDB Compass** instalado en Fedora 43 vía Flatpak.

---

## 🛠️ Stack y Herramientas

| Tecnología | Uso |
|-----------|-----|
| MongoDB Atlas | Cluster NoSQL gratuito en la nube |
| MongoDB Compass | GUI de administración |
| Fedora 43 | Sistema anfitrión |
| Flatpak | Instalador de Compass en Linux |

---

## ☁️ Configuración del Cluster

```
Plataforma:   MongoDB Atlas (cloud.mongodb.com)
Plan:         Free Tier (M0 Sandbox)
Región:       Configurada según disponibilidad
```

---

## 👥 Usuarios y Roles Creados

### Usuario 1 — Acceso completo
```
Autenticación:  Password
Privilegio:     readWriteAnyDatabase (lectura/escritura en cualquier BD)
```

### Usuario 2 — Acceso restringido
```
Autenticación:  Password
Privilegio:     readAnyDatabase (solo lectura)
```

---

## 🗄️ Bases de Datos y Colecciones

### Base de Datos: `Unitecnar`

#### Colección: `estudiantes`
```json
{
  "nombre": "...",
  "codigo": "...",
  "carrera": "...",
  "semestre": ...,
  "email": "..."
}
```

### Base de Datos: `segunda_bd`

Tres colecciones adicionales con sus respectivos campos y documentos insertados.

---

## 🔧 Instalación de MongoDB Compass en Fedora

```bash
# Instalar via Flatpak (método recomendado para Linux)
flatpak install mongodb-compass

# Abrir Compass
flatpak run mongodb-compass
```

---

## 🔌 Conexión con MongoDB Compass

```
# Obtener URL de conexión:
# Atlas → Connect → Compass → Copiar Connection String

# Formato:
mongodb+srv://usuario:<password>@cluster0.xxxxx.mongodb.net/

# Pegar la URL en Compass → Connect
```

### Resultado
- ✅ Usuario 1 conectado exitosamente con acceso completo
- ✅ Usuario 2 conectado exitosamente con acceso de solo lectura

---

## 📊 Diferencias NoSQL vs SQL

| Característica | MongoDB (NoSQL) | MySQL (SQL) |
|---------------|----------------|-------------|
| Estructura | Documentos JSON flexibles | Tablas con esquema fijo |
| Escalabilidad | Horizontal (sharding) | Vertical |
| Relaciones | Embebido / referencias | Foreign Keys |
| Consultas | MQL | SQL estándar |
| Ideal para | Datos no estructurados | Datos relacionales |

---

## 🧠 Aprendizajes

- Configuración de cluster MongoDB Atlas gratuito
- Gestión de usuarios con roles y permisos en MongoDB
- Diferencia entre bases de datos relacionales y documentales
- Instalación de herramientas en Fedora Linux via Flatpak
- Conexión remota a base de datos en la nube con MongoDB Compass
