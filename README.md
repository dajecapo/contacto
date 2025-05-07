# Sección: Contáctanos

Esta sección permite que cualquier persona envíe un mensaje directo al administrador del sitio "Adopta un Sabio" mediante un formulario web. El mensaje se almacena automáticamente en la hoja `CONTACTO` de Google Sheets y, al enviarse, también redirige a WhatsApp del administrador.

## ✅ Características

- Formulario desplegable con campos:
  - Nombre
  - Teléfono (10 dígitos)
  - Email
  - Fecha
  - Mensaje (hasta 100 caracteres)
- Validación de:
  - Teléfono exacto de 10 dígitos (solo números)
  - Email válido
  - Campo mensaje con contador de caracteres
  - Captcha dinámico de suma con check verde
- Conexión con Google Sheets (hoja: `CONTACTO`)
- Redirección automática a WhatsApp del administrador (`9991832064`)
- Aparición de los mensajes en el panel de administración con botones de "Aprobar" y "Eliminar"

## 📌 Cómo se conecta con Google Sheets

Al enviar el formulario, los datos se mandan vía `POST` a la Web App de Google Apps Script. Se incluye el parámetro `tipo=contacto`, lo que permite al script identificar la hoja correcta (`CONTACTO`) y almacenar los datos.

## 📋 Estructura esperada en la hoja CONTACTO

| nombre | telefono | email | fecha | mensaje | estatus |
|--------|----------|-------|--------|---------|----------|
| Juan Pérez | 9991234567 | juan@gmail.com | 2025-05-07 | Estoy interesado... | pendiente |

## 🛠 Enlace al script

```
https://script.google.com/macros/s/AKfycbzb4ZvKX-6kpTni3cudJEs650tGoSEQNAPM9WuAhnXLcP0EJkpjvbmaI0u14Uqc6Za0/exec
```

## 👁 Revisión desde el panel de administración

Una vez enviado, el mensaje aparece automáticamente en la pestaña "Mensajes de Contacto" del panel. Desde ahí puedes:

- ✅ Aprobar el mensaje (marca "aprobado" en la columna `estatus`)
- ❌ Eliminarlo (borra la fila de la hoja de cálculo)

## 🚀 Importante

- Este formulario no requiere intervención adicional del administrador para conectarse.
- La sección es 100% funcional desde GitHub Pages.
- Está sincronizada con las demás pestañas del panel sin interferencias.

---

🧩 Proyecto: Adopta un Sabio  
✍️ Sección No. 9 — Contáctanos
