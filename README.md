# Analisis-ENUT-INEGI
Análisis descriptivo de la ENUT 2024 con Python y Power BI para visibilizar la brecha de género, la doble jornada y la pobreza de tiempo en México.

# 📊 El trabajo invisible y la pobreza de tiempo en México: Análisis de la ENUT 2024

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-2C2D72?style=for-the-badge&logo=pandas&logoColor=white)
![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Data Analysis](https://img.shields.io/badge/Data_Analysis-100000?style=for-the-badge&logo=data&logoColor=white)

> **Un análisis exploratorio y visual sobre la brecha de género, la doble jornada y el impacto de la economía de cuidados en la sociedad mexicana.**


## Resumen
Este proyecto presenta un análisis exploratorio de la distribución del tiempo en México mediante los microdatos de la Encuesta Nacional sobre Uso del Tiempo (ENUT) 2024 del INEGI. Utilizando Python y Power BI, se procesó la información de tareas simultáneas (cuidados pasivos) y se normalizó mediante promedios por individuo para evitar sesgos poblacionales. El análisis multidimensional revela hallazgos estadísticos críticos sobre el trabajo invisible y la "pobreza de tiempo".

## Hallazgos Principales (Perfiles de Análisis)
1. **La Cuidadora Invisible:** Las mujeres dedicadas exclusivamente al hogar sostienen cargas de trabajo no remunerado de hasta **59 horas semanales**, superando la jornada laboral máxima legal de un empleo formal.
2. **La Doble Jornada:** La inserción laboral femenina no redistribuye el trabajo doméstico. Las mujeres ocupadas sostienen una carga total de **casi 88 horas semanales**, superando ampliamente a los hombres en la misma condición.
3. **El Proveedor Tradicional:** Los hombres ocupados mantienen una participación marginal en tareas ineludibles de soporte vital, permitiéndoles capitalizar un mayor margen de cuidado personal y descanso.
4. **El Efecto de la Escolaridad:** Alcanzar estudios superiores no libera a la mujer de la doble jornada; el trabajo no remunerado se sostiene a costa de sacrificar horas críticas de descanso fisiológico.

## Metodología y Desarrollo Tecnológico
El proyecto se desarrolló en dos fases principales enfocadas en el rigor estadístico y la visualización de datos:

* **Data Wrangling (Python / Pandas):** Se estandarizaron variables y se imputaron valores nulos. El principal reto analítico fue el tratamiento de valores atípicos (*outliers*): en lugar de eliminarlos estadísticamente —lo que habría borrado la evidencia de sobreexplotación del tiempo—, se aplicaron topes lógicos de dominio (ej. limitando traslados a un máximo de 42 horas semanales). Además, se conservaron intactos los registros de "cuidados pasivos" para poder cuantificar la simultaneidad de tareas.
* **Business Intelligence (Power BI):** Mediante funciones DAX, el cálculo de horas totales se transformó en promedios por individuo, neutralizando el sesgo visual que hubieran generado los grupos poblacionales asimétricos. Se construyó un *dashboard* interactivo utilizando Parámetros de Campo, permitiendo segmentar la información dinámicamente.

## Estructura del Repositorio
```text
├── data/                   # Base de datos cruda y procesada (o enlace al INEGI si es muy pesada)
├── notebooks/              # Jupyter Notebooks con el código de limpieza (Pandas)
├── dashboard/              # Archivo .pbix de Power BI interactivo
├── images/                 # Capturas de pantalla de los gráficos y perfiles de análisis
└── README.md               # Resumen del proyecto
