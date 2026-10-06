// ========================================
// OSINT CON SPIDERFOOT EN KALI LINUX
// ========================================

// SpiderFoot permite automatizar la recopilación
// de información pública (OSINT) sobre un objetivo.
//
// USAR ÚNICAMENTE sobre objetivos propios,
// autorizados o dentro de un laboratorio.

// --- 1. VERIFICAR SI SPIDERFOOT ESTÁ INSTALADO ---

spiderfoot -h

// Si muestra la ayuda, está disponible.

// También podemos comprobar la versión:

spiderfoot --version


// --- 2. INICIAR SPIDERFOOT ---

spiderfoot -l 127.0.0.1:5001

// -l = dirección y puerto donde escuchará SpiderFoot
//
// Después abrir en el navegador:
//
// http://127.0.0.1:5001


// --- 3. CREAR UN ESCANEO DESDE LA INTERFAZ WEB ---

// Desde el navegador:
//
// 1. Abrir:
//    http://127.0.0.1:5001
//
// 2. Seleccionar "New Scan"
//
// 3. Introducir el objetivo
//
// Ejemplos de objetivos:
//
// dominio.com
// usuario@dominio.com
// 203.0.113.10
//
// Usar únicamente objetivos autorizados.


// --- 4. ELEGIR EL TIPO DE OBJETIVO ---

// SpiderFoot puede trabajar con diferentes tipos
// de objetivos.
//
// Ejemplos:
//
// DOMAIN_NAME
// IP_ADDRESS
// EMAILADDR
// USERNAME
//
// El tipo depende de qué información queremos
// investigar.


// --- 5. SELECCIONAR LOS MÓDULOS ---

// SpiderFoot utiliza módulos para obtener
// diferentes tipos de información.
//
// Algunos módulos pueden buscar:
//
// - DNS
// - WHOIS
// - subdominios
// - direcciones IP
// - correos electrónicos
// - nombres de usuario
// - certificados
// - datos públicos
//
// Podemos utilizar el perfil de escaneo recomendado
// o seleccionar módulos manualmente.


// --- 6. EJECUTAR EL ESCANEO ---

// Después de seleccionar:
//
// TARGET
// SCAN PROFILE
// MODULES
//
// iniciar el escaneo.
//
// SpiderFoot recopilará información pública
// y mostrará los resultados en la interfaz.


// --- 7. REVISAR LOS RESULTADOS ---

// SpiderFoot organiza los resultados en diferentes
// categorías.
//
// Podemos encontrar información relacionada con:
//
// Dominios
// Subdominios
// IPs
// DNS
// Emails
// URLs
// Certificados
// Tecnologías
// Usuarios
//
// Los resultados dependen del objetivo y de los
// módulos habilitados.


// --- 8. BUSCAR INFORMACIÓN CONCRETA ---

// Utilizar los filtros de SpiderFoot para localizar
// resultados específicos.
//
// Ejemplo:
//
// Buscar todos los subdominios encontrados
//
// Buscar direcciones IP
//
// Buscar correos electrónicos
//
// Buscar tecnologías detectadas


// --- 9. VISUALIZAR RELACIONES ---

// SpiderFoot puede representar los resultados
// mediante relaciones entre diferentes elementos.
//
// Ejemplo:
//
// DOMINIO
//    |
//    +---- SUBDOMINIO
//    |
//    +---- IP
//    |
//    +---- CERTIFICADO
//    |
//    +---- EMAIL
//
// Esto ayuda a comprender la relación entre
// los datos encontrados.


// --- 10. GUARDAR / EXPORTAR RESULTADOS ---

// Desde la interfaz de SpiderFoot se pueden
// consultar y exportar los resultados del escaneo.
//
// Guardar los resultados permite posteriormente
// analizarlos o documentarlos.


// --- 11. EJEMPLO DE FLUJO DE TRABAJO ---

// Objetivo autorizado:
//
// example.com
//
// 1. Iniciar SpiderFoot
//
// 2. Abrir:
//
// http://127.0.0.1:5001
//
// 3. New Scan
//
// 4. Introducir:
//
// example.com
//
// 5. Seleccionar el tipo:
//
// DOMAIN_NAME
//
// 6. Seleccionar un perfil de escaneo
//
// 7. Ejecutar
//
// 8. Revisar:
//
// - dominios
// - subdominios
// - DNS
// - IPs
// - certificados
// - emails públicos
// - URLs
//
// 9. Exportar/documentar los resultados


// ========================================
// RESUMEN
// ========================================

// Comprobar instalación
spiderfoot -h

// Iniciar SpiderFoot
spiderfoot -l 127.0.0.1:5001

// Abrir interfaz web
http://127.0.0.1:5001

// Crear nuevo escaneo
New Scan

// Introducir objetivo autorizado
example.com

// Seleccionar tipo de objetivo
DOMAIN_NAME

// Seleccionar perfil/módulos
SCAN PROFILE

// Ejecutar escaneo
START SCAN

// Analizar resultados
DOMAINS
SUBDOMAINS
DNS
IP
EMAIL
CERTIFICATES
URLS

// ========================================
