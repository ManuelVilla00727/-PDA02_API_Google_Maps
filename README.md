# 🗺️ Práctica 02: API Google Maps — LogiTech

![Estado](https://img.shields.io/badge/Estado-Completado-success)
![GCP](https://img.shields.io/badge/Google_Cloud-Platform-4285F4?logo=googlecloud&logoColor=white)
![Postman](https://img.shields.io/badge/Postman-API_Testing-FF6C37?logo=postman&logoColor=white)

## 📋 Descripción

Práctica de laboratorio de la **Maestría en Software** — Asignatura: **Patrones de Diseño de APIs**.

**Objetivo:** Interpretar la necesidad de los sistemas basados en APIs para los negocios, mediante el consumo, análisis arquitectónico y evaluación económica de **Google Maps Platform** (Geocoding API y Distance Matrix API) en el contexto de la startup de última milla **LogiTech**.

---

## 🎯 Contexto de Negocio

**LogiTech** es una startup de última milla que busca **optimizar rutas de entrega para reducir costos de combustible en un 15%**. En lugar de construir un motor cartográfico propio (años de desarrollo y millones de dólares), la junta directiva decidió apalancarse en el ecosistema de **Google Maps Platform**.

### APIs evaluadas:
- **Geocoding API:** Convierte direcciones en coordenadas geográficas (lat/lng).
- **Distance Matrix API:** Calcula distancia y tiempo estimado entre múltiples orígenes y destinos.

---

## 🛠️ Tecnologías Utilizadas

| Herramienta | Uso |
| :--- | :--- |
| **Google Cloud Platform (GCP)** | Aprovisionamiento y gobierno de APIs |
| **Geocoding API** | Conversión de direcciones a coordenadas |
| **Distance Matrix API** | Cálculo de distancias y tiempos |
| **Postman** | Cliente HTTP para pruebas de API |
| **JSON** | Formato de intercambio de datos |
| **Redis (propuesto)** | Caché de respuestas para resiliencia |
| **OpenStreetMap (propuesto)** | Fallback ante caídas de Google Maps |

---

## 🚀 Pasos Realizados

### Paso 1: Aprovisionamiento y Gobierno en GCP

1. Creación de cuenta en Google Cloud Platform (crédito gratuito de $300).
2. Creación del proyecto **`Maestria-APIs-Logitech`**.
3. Habilitación de las APIs:
   - ✅ **Geocoding API**
   - ✅ **Distance Matrix API**
4. Creación de **API Key** en `Credentials > Create Credentials > API Key`.
5. **Gobierno y Seguridad:** Restricción de la API Key para permitir únicamente las dos APIs habilitadas.

### Paso 2: Geocoding API — Dirección a Coordenadas

**Endpoint:**
