# 🌤️ Portfolio PBI Weather Dashboard

[English](#english) | [Español](#español)

---

<a name="english"></a>
# 🌤️ Portfolio PBI Weather Dashboard

Interactive Power BI dashboard that displays real-time weather data and forecasts for multiple locations using the new **PBIP** (Power BI Project) format.

## 📋 Description

This project is a Power BI dashboard developed with the new **PBIP** file model that allows visualization of current weather data, hourly and daily forecasts for different locations around the world. Data is obtained in real-time from the [Open-Meteo](https://open-meteo.com/) API using Power Query and TMDL (Tabular Model Definition Language). The report is fully bilingual, supporting both **English** and **Spanish** languages.

## 🔗 Published Dashboard

**👉 [View Dashboard on Power BI Service](https://app.powerbi.com/view?r=eyJrIjoiMmU4MzEwYmYtZWM5ZC00ZjQyLWFmY2UtMThkM2UzMDc0YzI0IiwidCI6Ijg2ZDVlYWY3LWNjOGEtNDkzMC04MjhlLWIwNGJmYzlhYzQ1ZiJ9)**

Explore the interactive dashboard published on Power BI Service with real-time weather data.

## ✨ Features

- 🌍 **Multiple locations**: Weather data visualization for several configured cities
- 📊 **Real-time data**: Current weather information automatically updated
- 📈 **Forecasts**: Hourly and daily data with up to 9 days ahead
- 🔄 **Centralized configuration**: Easy maintenance and scalability through TMDL and Power Query
- 🌐 **Bilingual report**: Fully bilingual dashboard supporting both English and Spanish (en-US and es-ES) with dynamic language switching
- 🎨 **Custom visualizations**: Interactive dashboard with multiple visuals and bookmarks
- 📦 **PBIP format**: Uses the new Power BI project format for better version control

## 🏗️ Project Structure

```
weather/
├── portfolio-pbi-weather.pbip             # Main project file
├── portfolio-pbi-weather.Report/          # Report definition
│   ├── definition/
│   │   ├── pages/                         # Dashboard pages
│   │   └── bookmarks/                     # Report bookmarks
│   └── StaticResources/                   # Static resources (images, icons)
└── portfolio-pbi-weather.SemanticModel/   # Semantic model
    ├── definition/
    │   ├── tables/                        # TMDL table definitions
    │   ├── relationships.tmdl             # Model relationships
    │   └── cultures/                      # Translations (es-ES, en-US)
    └── TMDLScripts/                       # TMDL scripts and measures

# Shared assets at the repo root:
../Icons/                                  # Icons used in the dashboard
../Backgrounds/                            # Backgrounds for visualizations
../weather_icons.csv                       # Weather icons mapping
```

## 🚀 Prerequisites

### Power BI Desktop
- Power BI Desktop (recent version supporting PBIP format)

## 📦 Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/rafaelm79dev/porfolio-pbi.git
   cd porfolio-pbi/weather
   ```

2. **Open the project in Power BI Desktop**
   - Open Power BI Desktop
   - Select `File` → `Open` → `Open Power BI project`
   - Select `portfolio-pbi-weather.pbip`

3. **Update data**
   - Power BI will automatically refresh data from the Open-Meteo API when opening the project
   - Data connections are configured through Power Query and TMDL definitions

## 🔧 Configuration

### Adding a New Location

To add a new location, you need to:

1. Create new tables in the semantic model following the existing pattern:
   - `{location}_current_df` - Current data
   - `{location}_hourly_df` - Hourly data
   - `{location}_daily_df` - Daily data
   - `{location}_apiURL` - API URL configuration

2. Update consolidated tables (`current_df`, `hourly_df`, `daily_df`) to include the new location data

3. Configure the API URLs and parameters in the respective table definitions using Power Query M language

## 📊 Included Data

### Current Data
- Current temperature
- Precipitation
- Rain
- Day/night indicator
- Weather code
- Relative humidity
- Wind speed and direction
- Surface pressure

### Hourly Data
- Temperature per hour
- Relative humidity per hour

### Daily Data
- Maximum UV index
- Maximum and minimum temperature
- Total precipitation
- Precipitation hours
- Maximum precipitation probability
- Weather code
- Sunrise and sunset

## 🎯 Configured Locations

The project currently includes data for:

- 🇺🇾 **Montevideo, Uruguay** (`mdeo_weather`)
- 🇧🇷 **Porto de Galinhas, Brazil** (`pdg_weather`)
- 🇲🇽 **Playa del Carmen, Mexico** (`pdc_weather`)

## 📝 Usage

1. Open the `.pbip` file in Power BI Desktop
2. Data will refresh automatically from the API
3. Explore the dashboard with interactive visualizations
4. Use filters and bookmarks to navigate between different views

## 🛠️ Technologies Used

- **Power BI Desktop**: Data visualization and analysis
- **Power Query**: Data transformation and API connections
- **Open-Meteo API**: Weather data source
- **TMDL**: Tabular Model Definition Language for the semantic model
- **DAX**: Data Analysis Expressions for measures and calculations

## 🙏 Acknowledgments

- [Open-Meteo](https://open-meteo.com/) for providing the free weather API

---

<a name="español"></a>
# 🌤️ Portfolio PBI Weather Dashboard

Dashboard interactivo de Power BI que muestra datos meteorológicos en tiempo real y pronósticos para múltiples ubicaciones utilizando el nuevo formato **PBIP** (Power BI Project).

## 📋 Descripción

Este proyecto es un dashboard de Power BI desarrollado con el nuevo modelo de archivos **PBIP** que permite visualizar datos meteorológicos actuales, pronósticos horarios y diarios de diferentes ubicaciones alrededor del mundo. Los datos se obtienen en tiempo real desde la API de [Open-Meteo](https://open-meteo.com/) utilizando Power Query y TMDL (Tabular Model Definition Language). El reporte es completamente bilingüe, soportando tanto **Español** como **Inglés**.

## 🔗 Dashboard Publicado

**👉 [Ver Dashboard en Power BI Service](https://app.powerbi.com/view?r=eyJrIjoiMmU4MzEwYmYtZWM5ZC00ZjQyLWFmY2UtMThkM2UzMDc0YzI0IiwidCI6Ijg2ZDVlYWY3LWNjOGEtNDkzMC04MjhlLWIwNGJmYzlhYzQ1ZiJ9)**

Explora el dashboard interactivo publicado en Power BI Service con datos meteorológicos en tiempo real.

## ✨ Características

- 🌍 **Múltiples ubicaciones**: Visualización de datos meteorológicos para varias ciudades configuradas
- 📊 **Datos en tiempo real**: Información meteorológica actual actualizada automáticamente
- 📈 **Pronósticos**: Datos horarios y diarios con hasta 9 días de anticipación
- 🔄 **Configuración centralizada**: Fácil mantenimiento y escalabilidad a través de TMDL y Power Query
- 🌐 **Reporte bilingüe**: Dashboard completamente bilingüe que soporta tanto inglés como español (en-US y es-ES) con cambio dinámico de idioma
- 🎨 **Visualizaciones personalizadas**: Dashboard interactivo con múltiples visuales y bookmarks
- 📦 **Formato PBIP**: Utiliza el nuevo formato de proyecto de Power BI para mejor control de versiones

## 🏗️ Estructura del Proyecto

```
weather/
├── portfolio-pbi-weather.pbip             # Archivo principal del proyecto
├── portfolio-pbi-weather.Report/          # Definición del reporte
│   ├── definition/
│   │   ├── pages/                         # Páginas del dashboard
│   │   └── bookmarks/                     # Marcadores del reporte
│   └── StaticResources/                   # Recursos estáticos (imágenes, iconos)
└── portfolio-pbi-weather.SemanticModel/   # Modelo semántico
    ├── definition/
    │   ├── tables/                        # Definiciones de tablas TMDL
    │   ├── relationships.tmdl             # Relaciones del modelo
    │   └── cultures/                      # Traducciones (es-ES, en-US)
    └── TMDLScripts/                       # Scripts y medidas TMDL

# Recursos compartidos en la raíz del repo:
../Icons/                                  # Iconos utilizados en el dashboard
../Backgrounds/                            # Fondos para visualizaciones
../weather_icons.csv                       # Mapeo de iconos meteorológicos
```

## 🚀 Requisitos Previos

### Power BI Desktop
- Power BI Desktop (versión reciente que soporte formato PBIP)

## 📦 Instalación

1. **Clonar el repositorio**
   ```bash
   git clone https://github.com/rafaelm79dev/porfolio-pbi.git
   cd porfolio-pbi/weather
   ```

2. **Abrir el proyecto en Power BI Desktop**
   - Abre Power BI Desktop
   - Selecciona `Archivo` → `Abrir` → `Abrir proyecto de Power BI`
   - Selecciona `portfolio-pbi-weather.pbip`

3. **Actualizar datos**
   - Power BI actualizará automáticamente los datos desde la API de Open-Meteo al abrir el proyecto
   - Las conexiones de datos están configuradas a través de Power Query y definiciones TMDL

## 🔧 Configuración

### Agregar una Nueva Ubicación

Para agregar una nueva ubicación, necesitas:

1. Crear nuevas tablas en el modelo semántico siguiendo el patrón existente:
   - `{ubicacion}_current_df` - Datos actuales
   - `{ubicacion}_hourly_df` - Datos horarios
   - `{ubicacion}_daily_df` - Datos diarios
   - `{ubicacion}_apiURL` - Configuración de URL de API

2. Actualizar las tablas consolidadas (`current_df`, `hourly_df`, `daily_df`) para incluir los datos de la nueva ubicación

3. Configurar las URLs de API y parámetros en las definiciones de tabla correspondientes usando el lenguaje M de Power Query

## 📊 Datos Incluidos

### Datos Actuales (Current)
- Temperatura actual
- Precipitación
- Lluvia
- Indicador día/noche
- Código del clima
- Humedad relativa
- Velocidad y dirección del viento
- Presión superficial

### Datos Horarios (Hourly)
- Temperatura cada hora
- Humedad relativa cada hora

### Datos Diarios (Daily)
- Índice UV máximo
- Temperatura máxima y mínima
- Precipitación total
- Horas de precipitación
- Probabilidad máxima de precipitación
- Código del clima
- Amanecer y atardecer

## 🎯 Ubicaciones Configuradas

Actualmente el proyecto incluye datos para:

- 🇺🇾 **Montevideo, Uruguay** (`mdeo_weather`)
- 🇧🇷 **Porto de Galinhas, Brasil** (`pdg_weather`)
- 🇲🇽 **Playa del Carmen, México** (`pdc_weather`)

## 📝 Uso

1. Abre el archivo `.pbip` en Power BI Desktop
2. Los datos se actualizarán automáticamente desde la API
3. Explora el dashboard con las visualizaciones interactivas
4. Usa los filtros y bookmarks para navegar entre diferentes vistas

## 🛠️ Tecnologías Utilizadas

- **Power BI Desktop**: Visualización y análisis de datos
- **Power Query**: Transformación de datos y conexiones API
- **Open-Meteo API**: Fuente de datos meteorológicos
- **TMDL**: Tabular Model Definition Language para el modelo semántico
- **DAX**: Expresiones de análisis de datos para medidas y cálculos

## 🙏 Agradecimientos

- [Open-Meteo](https://open-meteo.com/) por proporcionar la API meteorológica gratuita
