<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 9 


<!-- Su documentación aquí -->

Actividad:

-Crear un proyecto de Python y utilizar la librería pandas para realizar la limpieza de datos del siguiente conjunto de datos de venta de vehículos
-Descargar - Conjunto de Datos "Venta de Vehiculos"
-Documentar los problemas de datos encontrados

```
import streamlit as st
import pandas as pd
import matplotlib.pyplot as plt

data= pd.read_csv('ventas_vehiculos .csv')
st.header('TABLA PRINCIPAL')
data

st.header("Antes de limpieza de datos")
data
#datos vacios
data = data.dropna()

#datos atipicos
#plt.hist(data["Kilometraje"])
#st.pyplot()

#plt.boxplot(data["Kilometraje"])
#st.pyplot()

#data.plot.scatter(x="Estado", y="Kilometraje")
#st.pyplot()

data = data[~((data["Estado"] == "Nuevo") & (data["Kilometraje"] > 0))]

#datos duplicados
duplicates = data[data.duplicated(keep=False)]
#st.write(duplicates)

#formato de datos
#st.write(data.dtypes)
data["Fecha"] = pd.to_datetime(data["Fecha"])
#st.write(data.dtypes)

st.header("Despues de Limpieza de Datos")
data
```
[Ver en Streamlit](https://sesion9-bjgrzkd9nxvqepcmdwmdgr.streamlit.app/)





