# Actividad_1
## Actividad 1 de la clase Ing. Devops

### El encargo debe incluir los siguientes apartados:
1. Crean un repositorio Git en GitHub con las siguientes ramas: main, develop, feature/<nombre> y hotfix/<nombre>. (IE5)
2. Implementan GitFlow o trunk-based development, justificando su elección en el README del repositorio. (IE1)
3. Simulan un desarrollo colaborativo integrando al menos 2 cambios tipo feature y 1 tipo hotfix mediante pull requests. (IE2)
4. Documentan en un archivo README.md o wiki las convenciones de commits, flujos de merge, naming de ramas y estrategias de
revisión. (IE5)
5. Configuran al menos una acción básica de GitHub Actions que se ejecute con cada push a develop y pull request a main. (IE3/IE4)

📌 Ramas Principales
main
Contiene código en producción.
Siempre estable.
Solo recibe cambios desde release o hotfix.
develop
Rama base para desarrollo.
Integra nuevas funcionalidades antes de pasar a producción.
🚀 Ramas de Soporte
1. ✨ Feature

Propósito: Desarrollo de nuevas funcionalidades.

Base: develop
Merge hacia: develop

Formato:

feature/<nombre-corto-descriptivo>

Ejemplos:

feature/login-usuario
feature/api-productos
feature/integracion-pago

Reglas:

Usar minúsculas.
Separar palabras con guiones (-).
Ser claro y conciso.
2. 🛠️ Bugfix

Propósito: Corrección de errores en desarrollo.

Base: develop
Merge hacia: develop

Formato:

bugfix/<descripcion-del-error>

Ejemplos:

bugfix/error-login
bugfix/fix-null-pointer
3. 🚢 Release

Propósito: Preparar una nueva versión para producción.

Base: develop
Merge hacia: main y develop

Formato:

release/<version>

Ejemplos:

release/1.0.0
release/2.1.0

Reglas:

Seguir versionado semántico: MAJOR.MINOR.PATCH.
4. 🚨 Hotfix

Propósito: Corrección urgente en producción.

Base: main
Merge hacia: main y develop

Formato:

hotfix/<descripcion-o-version>

Ejemplos:

hotfix/fix-login-critico
hotfix/1.0.1
🔤 Reglas Generales
Usar siempre minúsculas.
No usar espacios (usar - en su lugar).
Evitar caracteres especiales (@, #, etc.).
Mantener nombres cortos pero descriptivos.
Usar inglés o español, pero no mezclar (definir estándar del equipo).
🧩 Buenas Prácticas

✔ Incluir contexto suficiente en el nombre
✔ Relacionar con ticket/issue si aplica
✔ Eliminar ramas después de hacer merge
✔ Mantener ramas actualizadas con develop

🔗 Ejemplo de Flujo
# Crear feature
git checkout develop
git checkout -b feature/login-usuario

# Finalizar feature
git checkout develop
git merge feature/login-usuario

# Crear release
git checkout -b release/1.0.0

# Crear hotfix
git checkout main
git checkout -b hotfix/fix-login
📎 Recomendación

Puedes complementar esta convención con:

Convención de commits (ej: Conventional Commits)
Uso de issues/tickets (Jira, GitHub Issues)
Pull Requests obligatorios con revisión
