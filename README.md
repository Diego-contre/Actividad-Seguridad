# 🔐 Actividad: Seguridad en Sistemas y Redes

---

## 🧩 I. Conceptos Base

| Concepto | Definición Simple | Nivel Técnico Breve | Ejemplo Real |
|----------|------------------|--------------------|--------------|
| **Permissions** | Quién puede entrar y qué puede hacer. | Control de acceso (RBAC/ACL) que define privilegios. | Usuario puede ver su perfil, admin puede borrarlo. |
| **Password Segura** | Llave difícil de adivinar. | Cadena con alta entropía + hashing + salt. | Kj8#pL2$mN1!Q vs password123. |
| **Vulnerabilidad** | Falla explotable. | Debilidad en diseño o código. | SQL Injection en formulario. |
| **Intrusión** | Acceso sin permiso. | Uso de exploits para entrar. | Acceso al panel admin robando sesión. |
| **Seguridad de Red** | Protección del tráfico. | Firewalls, VPNs, segmentación. | Firewall permite solo 443. |

---

## 🔑 II. Permissions

### Conceptos

- **Autenticación (AuthN):** Verifica identidad  
- **Autorización (AuthZ):** Define permisos  

### Diferencia

- AuthN = quién eres  
- AuthZ = qué puedes hacer  

---

### 💻 Ejemplo Developer

**Login → Autenticación**
- Usuario ingresa credenciales
- Backend genera token/sesión

**Roles → Autorización**
```js
if (user.role === "admin") {
  allowDelete();
}
