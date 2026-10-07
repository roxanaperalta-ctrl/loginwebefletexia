# EfletexIA - Acceso a T1 y T2

Pantallas para el botón "Iniciar sesión" de la web de EfletexIA, con el mismo diseño del login actual
(Tailwind + Inter + paleta naranja/oscura).

| Archivo | Qué es |
|---|---|
| `acceso-t1t2.html` | Pantalla para elegir la plataforma: T1 o T2. |
| `login-t1.html` | Login de la plataforma T1 (distribución primaria). |
| `login-t2.html` | Login de la plataforma T2 (distribución secundaria). |
| `index.html` | Solo redirige a `acceso-t1t2.html`. |

## Cómo integrarlo

1. Copiar los tres archivos HTML junto a `index.html` de la web.
2. Enlazar el botón "Log in / Iniciar sesión" a `acceso-t1t2.html` (o reemplazar el contenido de `login.html`).
3. Las tarjetas T1 y T2 abren `login-t1.html` y `login-t2.html`. Las direcciones están en `CONFIG`, al final de `acceso-t1t2.html`.

## Pendiente para desarrollo

- Los formularios de `login-t1.html` y `login-t2.html` son de diseño: el botón "Iniciar sesión" muestra un aviso
  y no autentica. Hay que conectarlos al inicio de sesión real de cada plataforma:
  - T1: https://efletexia.com/login/inicio
  - T2: https://pruebast2.dtdevops.com/login (ambiente de pruebas; reemplazar por la URL de producción)
- "¿Olvidaste tu contraseña?" y los enlaces de Soporte abren https://portal-usuarios.dtdevops.com/
  (las cuentas y contraseñas las gestiona Soporte; no hay registro abierto).
- "Regístrate" en T1 debe enlazarse al registro actual de T1.

## Nota técnica

Los textos con tildes están escritos como entidades HTML (`&#243;`, etc.) para que no se dañen al enviarse por correo.
Los íconos usan Iconify; cada `data-icon` necesita la clase `iconify` (se agrega por script al final de cada página).
