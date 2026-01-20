# 🧪Lab 02: Implementación de SSPR (Self-Service Password Reset)

Repo: **Azure-Lab-02-SSPR**

## 🎯 Objetivo
Reducir tickets de soporte habilitando **SSPR (Self-Service Password Reset)** de forma segura para un **grupo piloto**, requiriendo **doble verificación** y validando el flujo real de restablecimiento.

---

## 🛠️ Alcance y configuración
- **SSPR habilitado para:** *Seleccionado* → grupo **GRP_SSPR_Users**
- **Métodos permitidos para SSPR:** **Email (OTP)** + **Teléfono móvil (SMS)**
- **Número de métodos requeridos:** **2**
- **Usuario de prueba:** `usuario_1` (miembro del grupo)

> Nota: En este tenant, los métodos se habilitan desde **Métodos de autenticación (Directivas)** (política convergente de Microsoft Entra).

---

## ✅ Tareas realizadas
1. Creación del grupo **GRP_SSPR_Users**.
2. Creación de usuario de prueba `usuario_1` y asignación al grupo.
3. Activación de **SSPR** en modo **Seleccionado** para el grupo piloto.
4. Habilitación de métodos para SSPR: **Email (OTP)** y **SMS**.
5. **Validación**: ejecución del flujo “He olvidado mi contraseña” para comprobar que se ofrecen los métodos configurados.
6. (Extra) **Creación masiva** de usuarios mediante importación **CSV**.

---

## 📸 Evidencias

### 1) SSPR habilitado para grupo piloto (Selected)
![SSPR habilitado - grupo](images/01-sspr-grupo.png)

### 2) Métodos permitidos (Directivas de Métodos de autenticación)
Email (OTP) + Teléfono móvil (SMS)
![Métodos SSPR](images/02-sspr-metodos.png)


![Métodos SSPR](images/03-sspr-metodos.png)


### 3) Validación real del flujo SSPR
Pantalla donde el usuario selecciona método (Email/SMS) durante el restablecimiento.
![Validación SSPR](images/04-validacion-sspr-seleccion-metodo.png)


### 4) Extra: onboarding masivo por CSV

> Generación del CSV (Excel):**  

![CSV Excel](images/CSV_usuarios.png)



> Resultado en Entra (importación):**  

![Resultado importación](images/11-users-created.png)
---

## ✅ Checklist de verificación
- [x] SSPR habilitado solo para grupo piloto
- [x] Se requieren **2 métodos** para restablecer
- [x] Métodos disponibles: **Email (OTP)** + **SMS**
- [x] Validación realizada (flujo real muestra selección de método)
- [x] Usuario de prueba incluido en el grupo
- [x] (Extra) Importación masiva por CSV documentada

---

## 🗣️ Qué le diría al cliente / entrevista
“Implementé SSPR para un **grupo piloto** con **doble verificación** (Email + SMS) para reducir tickets de soporte sin perder seguridad.
Además, añadí un ejemplo de **onboarding masivo por CSV**, típico en entornos reales, y validé el flujo completo de restablecimiento.”
