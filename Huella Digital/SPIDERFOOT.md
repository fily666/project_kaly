# SPIDERFOOT — OSINT automatizado

> **Categoría:** Huella Digital
> **Objetivo:** automatizar la recopilación de información pública (OSINT) sobre un objetivo.
>
> ⚠️ Usar únicamente sobre objetivos propios, autorizados o dentro de un laboratorio.

---

## 1. Verificar si SpiderFoot está instalado

```bash
spiderfoot -h
```

Si muestra la ayuda, está disponible. También se puede comprobar la versión:

```bash
spiderfoot --version
```

## 2. Iniciar SpiderFoot

```bash
spiderfoot -l 127.0.0.1:5001
```

- `-l` → dirección y puerto donde escuchará SpiderFoot.

Después abrir en el navegador: <http://127.0.0.1:5001>

## 3. Crear un escaneo desde la interfaz web

1. Abrir <http://127.0.0.1:5001>
2. Seleccionar **New Scan**
3. Introducir el objetivo

**Ejemplos de objetivos:**

```text
dominio.com
usuario@dominio.com
203.0.113.10
```

## 4. Elegir el tipo de objetivo

El tipo depende de qué información queremos investigar:

| Tipo          | Ejemplo               |
|---------------|-----------------------|
| `DOMAIN_NAME` | `dominio.com`         |
| `IP_ADDRESS`  | `203.0.113.10`        |
| `EMAILADDR`   | `usuario@dominio.com` |
| `USERNAME`    | `usuario`             |

## 5. Seleccionar los módulos

SpiderFoot utiliza módulos para obtener distintos tipos de información:

- DNS
- WHOIS
- Subdominios
- Direcciones IP
- Correos electrónicos
- Nombres de usuario
- Certificados
- Datos públicos

Se puede usar el **perfil de escaneo recomendado** o seleccionar módulos manualmente.

## 6. Ejecutar el escaneo

Después de seleccionar **TARGET**, **SCAN PROFILE** y **MODULES**, iniciar el escaneo.
SpiderFoot recopilará información pública y mostrará los resultados en la interfaz.

## 7. Revisar los resultados

Los resultados se organizan por categorías:

- Dominios y subdominios
- IPs y DNS
- Emails y usuarios
- URLs
- Certificados
- Tecnologías

Los resultados dependen del objetivo y de los módulos habilitados.

## 8. Buscar información concreta

Usar los filtros de SpiderFoot para localizar resultados específicos.

**Ejemplos:**

- Todos los subdominios encontrados
- Direcciones IP
- Correos electrónicos
- Tecnologías detectadas

## 9. Visualizar relaciones

SpiderFoot puede representar los resultados como relaciones entre elementos:

```text
DOMINIO
   |
   +---- SUBDOMINIO
   |
   +---- IP
   |
   +---- CERTIFICADO
   |
   +---- EMAIL
```

Esto ayuda a comprender cómo se relacionan los datos encontrados.

## 10. Guardar / exportar resultados

Desde la interfaz se pueden consultar y exportar los resultados del escaneo para analizarlos o documentarlos después.

## 11. Ejemplo de flujo de trabajo

**Objetivo autorizado:** `example.com`

1. Iniciar SpiderFoot: `spiderfoot -l 127.0.0.1:5001`
2. Abrir <http://127.0.0.1:5001>
3. Clic en **New Scan**
4. Introducir `example.com`
5. Seleccionar el tipo `DOMAIN_NAME`
6. Seleccionar un perfil de escaneo
7. Ejecutar
8. Revisar: dominios, subdominios, DNS, IPs, certificados, emails públicos, URLs
9. Exportar / documentar los resultados

---

## Resumen

| Acción                     | Comando / Acción                                     |
|----------------------------|------------------------------------------------------|
| Comprobar instalación      | `spiderfoot -h`                                      |
| Iniciar SpiderFoot         | `spiderfoot -l 127.0.0.1:5001`                       |
| Abrir interfaz web         | <http://127.0.0.1:5001>                              |
| Crear nuevo escaneo        | **New Scan**                                         |
| Introducir objetivo        | `example.com`                                        |
| Seleccionar tipo           | `DOMAIN_NAME`                                        |
| Seleccionar perfil/módulos | **SCAN PROFILE**                                     |
| Ejecutar escaneo           | **START SCAN**                                       |
| Analizar resultados        | Domains, Subdomains, DNS, IP, Email, Certificates, URLs |
