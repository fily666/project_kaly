// ========================================
// ESCANEO DE EQUIPOS EN LA RED
// ========================================

// --- 1. VER MI IP ---

ifconfig

// También se puede usar:

ip addr

// --- 2. IDENTIFICAR LA RED ---

// Ejemplo:

IP: 10.0.2.15
MASCARA: 255.255.255.0

// 255.255.255.0 = /24
// Red:

10.0.2.0/24

// *** 3. VER EQUIPOS EN LA RED ***

sudo nmap -sn 10.0.2.0/24

// -sn = descubrir equipos activos
// sin escanear todos los puertos

// --- 4. ESCANEAR UN EQUIPO ---

sudo nmap <IP>

// Ejemplo:

sudo nmap 10.0.2.20

// *** 5. VER SERVICIOS Y VERSIONES ***

sudo nmap -sV <IP>

// Ejemplo:

sudo nmap -sV 10.0.2.20

// Puede mostrar:

22/tcp open ssh
80/tcp open http
443/tcp open https

// --- 6. ESCANEAR PUERTOS ESPECIFICOS ---

sudo nmap -p 22,80,443 <IP>

// Ejemplo:

sudo nmap -p 22,80,443 10.0.2.20

// *** 7. ESCANEAR TODOS LOS PUERTOS ***

sudo nmap -p- <IP>

// Ejemplo:

sudo nmap -p- 10.0.2.20

// --- 8. GUARDAR RESULTADO ---

sudo nmap -sV <IP> -oN resultado.txt

// Ejemplo:

sudo nmap -sV 10.0.2.20 -oN resultado.txt

// ========================================
// RESUMEN
// ========================================

// Ver IP
ifconfig

// Ver red
ip route

// Ver equipos
sudo nmap -sn 10.0.2.0/24

// Escanear equipo
sudo nmap <IP>

// Ver servicios y versiones
sudo nmap -sV <IP>

// Escanear puertos específicos
sudo nmap -p 22,80,443 <IP>

// Todos los puertos
sudo nmap -p- <IP>

// Guardar resultado
sudo nmap -sV <IP> -oN resultado.txt

// ========================================