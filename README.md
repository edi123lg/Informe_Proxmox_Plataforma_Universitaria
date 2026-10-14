# Diseño y Transformación de Plataforma Virtualizada con Proxmox VE
**Proyecto de Infraestructura TI Universitaria - Servidor HP Z820**

Este repositorio contiene la propuesta técnica e informe de ingeniería para transformar un servidor de laboratorio en una plataforma de virtualización organizada, segura y escalable basada en **Proxmox VE**.

## 📄 Archivos del Repositorio
* `Informe_Proxmox_Plataforma_Universitaria.pdf`: Informe técnico completo enviado a la Dirección de TI.
* `diagrama_arquitectura.jpg`: Diagrama de arquitectura lógica, red y almacenamiento.

## 🎯 Resumen de la Solución
El diseño contempla una **capacidad objetivo ampliada a 256 GB RAM RDIMM** y un esquema de almacenamiento híbrido (SSD LVM-thin para operaciones y HDD RAID 1 para respaldos aislados), distribuido en 4 entornos:

1. **Producción (35% RAM / 40% SSD / `cpuunits = 2048`):** Servicios críticos (LMS, BD, Web).
2. **Laboratorios Docentes (25% RAM / 25% SSD / `cpuunits = 1024`):** Capacidades para 4 docentes y 100 estudiantes mediante LXC/VMs.
3. **Desarrollo (20% RAM / 15% SSD / `cpuunits = 1024`):** Proyectos en construcción.
4. **Pruebas (15% RAM / 20% SSD / `cpuunits = 512`):** Instancias temporales y experimentación.

## 📐 Arquitectura
![Diagrama de Arquitectura](diagrama_arquitectura.jpg)

---
*Proyecto elaborado para la asignatura de Infraestructura de TI.*
