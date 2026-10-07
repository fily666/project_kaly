# NMAP — Escaneo de equipos en la red

> **Categoría:** Mapeo de Red
> **Objetivo:** descubrir equipos activos en una red y analizar sus puertos y servicios.
>
> ⚠️ Usar únicamente sobre redes propias, autorizadas o dentro de un laboratorio.

---

## 1. Ver mi IP

```bash
ifconfig
```

También se puede usar:

```bash
ip addr
```

## 2. Identificar la red

**Ejemplo:**

```text
IP:      10.0.2.15
MÁSCARA: 255.255.255.0   (= /24)
RED:     10.0.2.0/24
```

Para ver la red y la puerta de enlace:

```bash
ip route
```

## 3. Ver equipos en la red

```bash
sudo nmap -sn 10.0.2.0/24
```

- `-sn` → descubre equipos activos **sin** escanear puertos.

## 4. Escanear un equipo

```bash
sudo nmap <IP>
```

**Ejemplo:**

```bash
sudo nmap 10.0.2.20
```

## 5. Ver servicios y versiones

```bash
sudo nmap -sV <IP>
```

**Ejemplo:**

```bash
sudo nmap -sV 10.0.2.20
```

**Salida posible:**

```text
22/tcp  open  ssh
80/tcp  open  http
443/tcp open  https
```

## 6. Escanear puertos específicos

```bash
sudo nmap -p 22,80,443 <IP>
```

**Ejemplo:**

```bash
sudo nmap -p 22,80,443 10.0.2.20
```

## 7. Escanear todos los puertos

```bash
sudo nmap -p- <IP>
```

**Ejemplo:**

```bash
sudo nmap -p- 10.0.2.20
```

## 8. Guardar resultado

```bash
sudo nmap -sV <IP> -oN resultado.txt
```

**Ejemplo:**

```bash
sudo nmap -sV 10.0.2.20 -oN resultado.txt
```

---

## Resumen

| Acción                       | Comando                                |
|------------------------------|----------------------------------------|
| Ver IP                       | `ifconfig`                             |
| Ver red                      | `ip route`                             |
| Ver equipos                  | `sudo nmap -sn 10.0.2.0/24`            |
| Escanear equipo              | `sudo nmap <IP>`                       |
| Ver servicios y versiones    | `sudo nmap -sV <IP>`                   |
| Escanear puertos específicos | `sudo nmap -p 22,80,443 <IP>`          |
| Todos los puertos            | `sudo nmap -p- <IP>`                   |
| Guardar resultado            | `sudo nmap -sV <IP> -oN resultado.txt` |
