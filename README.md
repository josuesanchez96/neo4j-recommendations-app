# Descripción del proyecto

Este proyecto demuestra el uso de bases de datos de grafos con Neo4j y Flask, mostrando recomendaciones de películas basadas en relaciones entre usuarios y películas.
---

## Instrucciones para instalar dependencias y ejecutar la app

1. _Clonar el repositorio en la terminal de windows_    
git clone https://github.com/josuesanchez96/neo4j-recommendations-app
2. _Crear y activar un entorno virtual en la raiz del proyecto_  
python -m venv venv
venv\Scripts\activate
3. _Instalar Flask y Neo4j_  
pip install flask neo4j
4. _Ejecutar la aplicación Flask_  
python app.py
5. _Abrir el navegador y acceder a la dirección siguiente_  
http://localhost:5000

---
## Capturas o explicación del funcionamiento básico

El programa cuenta con la interfaz desarrollada en Flask que permite consultar recomendaciones por usuario como por producto. El usuario puede ingresar un ID que puede ser el número **1** al **20** para obtener películas sugeridas basadas en los hábitos de otros usuarios similares. 
Alternativamente puede ingresar el nombre de una película y visualizaer títulos relacionados que han sido valorados por los mismos usuarios.  
![image](https://github.com/user-attachments/assets/4145ea15-c12b-4489-a0f4-b6d9c4b3a311)

## Detalles de la conexión a la base de datos demo
Este programa se conecta a la base de datos de demostración pública de Neo4j, proporcionada por Neo4j Labs.
Los detalles de conexión utilizados en el código son los siguientes:
- Host: demo.neo4jlabs.com
- Puerto: 7687
- Protocolo: neo4j+s (conexión segura)
- Base de datos: recommendations
- Usuario: recommendations
- Contraseña: recommendations

## Código de conexión en app.py: 
URI = "neo4j+s://demo.neo4jlabs.com:7687"  
USERNAME = "recommendations"  
PASSWORD = "recommendations"  

driver = GraphDatabase.driver(URI, auth=(USERNAME, PASSWORD))
