# GEO-RECON — Geolocalización de direcciones IP

> **Categoría:** Geolocalización
> **Objetivo:** obtener la ubicación aproximada e información pública de una dirección IP.
> **Repositorio:** <https://github.com/radioactivetobi/geo-recon>
>
> ⚠️ Usar únicamente sobre objetivos propios, autorizados o dentro de un laboratorio.

---

## 1. Clonar el proyecto

```bash
git clone https://github.com/radioactivetobi/geo-recon.git
```

## 2. Instalar pip para Python

```bash
sudo apt install python3-pip
```

## 3. Instalar los requerimientos del proyecto

```bash
cd geo-recon
pip3 install -r requirements.txt
```

## 4. Ejecutar el escaneo

```bash
python3 geo-recon.py <IP>
```

**Ejemplo:**

```bash
python3 geo-recon.py 138.121.128.19
```

---

## Resumen

| Acción                 | Comando                                                       |
|------------------------|---------------------------------------------------------------|
| Clonar proyecto        | `git clone https://github.com/radioactivetobi/geo-recon.git`  |
| Instalar pip           | `sudo apt install python3-pip`                                |
| Instalar requerimientos| `cd geo-recon && pip3 install -r requirements.txt`            |
| Ejecutar escaneo       | `python3 geo-recon.py <IP>`                                   |
