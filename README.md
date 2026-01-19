# Lab 02: Implementación de SSPR (Self-Service Password Reset)

Repo: **Azure-Lab-02-SSPR**

## 🎯 Objetivo
Reducir tickets de soporte habilitando **restablecimiento de contraseña de autoservicio (SSPR)** de forma segura, usando **doble verificación** (Email + Teléfono) y aplicándolo a un entorno de laboratorio con usuarios creados en bloque.

---

## 🛠️ Tareas realizadas
1. Creación del grupo piloto **GRP_SSPR_Users**.
2. Creación del usuario **usuario_1** y asignación al grupo.
3. Configuración de SSPR (restablecimiento de contraseña) para usuarios del tenant.
4. Habilitación de métodos de verificación: **Email (OTP)** + **Teléfono (SMS)**.
5. **Validación**: prueba real del flujo de restablecimiento mostrando selección de método.
6. (Extra “pro”) **Onboarding masivo** de usuarios mediante **CSV (Bulk create)**.

> Nota: En este tenant, la habilitación de métodos para SSPR se gestiona desde **Métodos de autenticación (directivas)** (política convergente de Entra).

---

## 📸 Evidencias

### ✅ Evidencias principales (SSPR)
- **SSPR habilitado (Propiedades):** ![SSPR Propiedades](images/01-sspr-propiedades.png)
- **Métodos habilitados (Directivas): OTP Email + SMS:** `images/02-authmethods-otp-email-sms.png`  
- **Validación real (SSPR): selección de método Email/SMS en el reset:** `images/03-validacion-sspr-seleccion-metodo.png`

### ⭐ Evidencias extra (Onboarding masivo con CSV)
> Recomendación: **no hace falta captura de Excel**. Con una captura del **resultado de la importación** y/o de la **lista de usuarios creados** es suficiente y queda más limpio.

- **Resultado de importación masiva (Bulk create):** `images/10-bulk-results.png`
- **Usuarios creados en Entra:** `images/11-users-created.png`

---

## ✅ Checklist de verificación
- [x] SSPR habilitado
- [x] Se requieren **2 métodos** para el restablecimiento
- [x] Métodos permitidos: **OTP de correo electrónico** + **SMS**
- [x] Validación realizada: se muestra selección de método en el flujo real
- [x] Usuario `usuario_1` creado y asignado al grupo (si aplica)
- [ ] Métodos débiles deshabilitados (si aplica en el tenant)

---

## 🗣️ Qué le diría al cliente / entrevista
“SSPR mejora la productividad y reduce costes operativos al disminuir tickets de soporte, manteniendo seguridad con verificación fuerte.  
Además, simulé un escenario real con **onboarding masivo por CSV**, habitual cuando se reciben altas en bloque, y validé el flujo de restablecimiento mostrando la selección de métodos configurados.”
