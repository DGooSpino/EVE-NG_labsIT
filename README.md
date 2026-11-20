# 🌐 Portafolio de Laboratorios de Redes — EVE-NG
Repositorio dedicado a la documentación, diseño de topologías y respaldo de configuraciones (`startup-config`) de escenarios de redes implementados y probados en **EVE-NG**.
---
## 📂 Estructura del Repositorio

Cada laboratorio sigue una estructura modular para facilitar su reproducción y auditoría:
```text
├── lab-01.../             # Name del Lab
│   ├── assets/            # Capturas de topología y evidencias de pruebas
│   ├── startups_configs/  # Archivos de configuración inicial 
│   └── README.md          # Documentación específica del laboratorio
└── README.md              # Índice general del portafolio (este archivo)
```

## 🧪 Índice de Laboratorios
| # | Laboratorio |
| :--- 
| **01** |(./lab-01makeLAN) | Switching Multicapa (Core / Distribución), Enrutamiento base | 
| **02** |(./lab02-ServerDHCP/) | Servidor DHCP (`dnsmasq` en Alpine Linux)
| **03** |(./lab03-VLans&NAt) | Topologia de la LAN
---
## 🛠️ Herramientas y Entorno Utilizado
* **Emulación de Red:** EVE-NG Community Edition (Bare-Metal)
* **Dispositivos Virtuales:** Cisco IOS / IOU (Routers y Switches L2/L3), Alpine Linux (Servicios ligeros de red)
