# HOLEHE — Verificar registros de un correo

> **Categoría:** Huella Digital
> **Objetivo:** comprobar en qué sitios web está registrada una dirección de correo electrónico.
> **Repositorio:** <https://github.com/megadose/holehe>
>
> ⚠️ Usar únicamente sobre objetivos propios, autorizados o dentro de un laboratorio.

---

## 1. Instalar pipx

```bash
sudo apt install -y pipx
pipx ensurepath
```

- `pipx ensurepath` → agrega los programas de pipx al `PATH` (reiniciar la terminal después).

## 2. Instalar Holehe

```bash
pipx install holehe
```

## 3. Verificar la instalación

```bash
holehe --help
```

Si muestra la ayuda, está disponible.

## 4. Analizar un correo

```bash
holehe <CORREO>
```

**Ejemplo:**

```bash
holehe test@gmail.com
```

**Salida posible:**

```text
[+] Email used
[-] Email not used
[x] Rate limit
```

---

## Resumen

| Acción             | Comando                                       |
|--------------------|-----------------------------------------------|
| Instalar pipx      | `sudo apt install -y pipx && pipx ensurepath` |
| Instalar Holehe    | `pipx install holehe`                         |
| Verificar          | `holehe --help`                               |
| Analizar un correo | `holehe <CORREO>`                             |
