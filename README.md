# Segundo proyecto individual para el BootCamp de Soy Henry.

## Extracción y Análisis de la Api de CoinGecko Para Criptomonedas

Readme para el proyecto de data analitycs



### Objetivo
Realizar un análisis utilizando datos de la API de CoinGecko para entender mejor el mercado de criptomonedas.

En este proyecto las tareas a realizar son las siguientes:
* Extracción de datos de la api de **https://www.coingecko.com/es/api/documentation**
* Análisis Exploratorio de los Datos(EDA) de los datos obtenidos de la api.
* Contrucción de un dashboard en cualquier herramienta para tal fin.

Para la instalación de las librerías usadas, ver el archivo requirements.txt.  

Para comenzar, la extracción de los datos se hizo mediante la librería de CoinGeckoAPI, esta librería
implementa unos métodos que facilitan la extracción, ya que los métodos son casi iguales en nombre, los
parámetros son los mismos y evita tener que colocar unas líneas mas de código que cuando se traen los datos
con otra librería como request, igualmente se visita la página sugerida para revisar parámetros y documentación.

En el archivo ETL_cripto.ipynb, se detallan los pasos realizados para la extracción de los datos para su posterior 
análisis, se creyó conveniente despues de extraer los datos con cada método, construir dataframe separados, lo
cual faciltaría el análisis y la transformación en caso de necesitarla.

Como resultado, tenemos los siguientes .csv:
* df_datos_globales.csv
* df_historico_primeras4_monedas.csv
* df_olhc_binance.csv
* df_olhc_bitcoin.csv
* df_olhc_ethereum.csv
* df_olhc_tether.csv
* df_precio_10_monedas.csv


### Detalles de los Dataframes
A continuación un resúmen de los dataframes construidos:  
1-**df_global_data.**  
Datos globales de las criptomonedas en la página con las siguientes columnas:
**criptomonedas_activas:** El número de criptomonedas que están activas en el mercado, es decir, que se pueden comprar, vender o intercambiar.
**icos_activas:** El número de ofertas iniciales de monedas que están en curso, es decir, que aún no han finalizado su periodo de recaudación de fondos.
**icos_finalizadas:** El número de ofertas iniciales de monedas que han terminado, es decir, que ya han cerrado su periodo de recaudación de fondos y han distribuido sus criptomonedas a los inversores. 
**mercados** El número de mercados o plataformas donde se pueden comprar, vender o intercambiar criptomonedas.
**fecha_actualizacion:** La fecha y hora en la que se actualizó la información del dataframe, expresada en formato ISO 8601.

Se eligió el valor de las criptomonedas en la columna precio, el dólar($) y el euro(€), por ser monedas de referencia global. Sin embargo, hay otras monedas que podrían establecerse como referencia mundial, debido a múltiples factores como el crecimiento económico sostenido en el tiempo de una nación, su solidez económica y su estabilidad política. 

2-**df_precio_10_monedas.**  
Datos relevantes de las 10 primeras criptomonedas.  
**nombre:**							
**dolar:** Es el precio de la criptomoneda en dólares estadounidenses. Es una medida del valor de mercado de la criptomoneda en relación con la moneda más utilizada y aceptada del mundo.
**dolar_mercado_cap:** Es el valor total de mercado de la criptomoneda en dólares estadounidenses. Se calcula multiplicando el precio de la criptomoneda por el número total de unidades en circulación. Es una medida del tamaño y la importancia de la criptomoneda en el ecosistema cripto.
**dolar_24h_vol:** Es el volumen total de transacciones de la criptomoneda en dólares estadounidenses en las últimas 24 horas. Es una medida de la actividad y la liquidez de la criptomoneda en el mercado.
**dolar_24h_cambio:** Es el porcentaje de cambio del precio de la criptomoneda en dólares estadounidenses en las últimas 24 horas. Es una medida de la volatilidad y la tendencia de la criptomoneda en el corto plazo.
**euro:** Es el precio de la criptomoneda en euros. Es una medida del valor de mercado de la criptomoneda en relación con la moneda oficial de la Unión Europea y otras zonas económicas.
**euro_mercado_cap:** Igual que dolar_mercado_cap pero en euros.  
**euro_24h_vol:** Igual a dolar_24h_vol pero en euros

**euro_24h_cambio:** Igual a dolar_24h_cambio pero en euros.  

**ultima_actualizacion:** Última fecha de actualización.


3-**df_historico_primeras4_monedas.**    
**fecha:** Fecha del dato.  
**precio_btc:** Precio histórico del bitcoin.  
**mercado_cap_btc:** Capitalización del mercado de bitcoin.  
**total_volumen_btc:** Volúmen total de transacciones del bitcoin.  
**precio_ethereum:** Precio histórico de ethereum.  
**mercado_cap_ethereum:** Capitalización del mercado de ethereum.  
**total_volumen_ethereum:** Volúmen total de transacciones del ethereum.  
**precio_tether:** Precio histórico de tether.  
**mercado_cap_tether:** Capitalización del mercado de tether.  
**total_volumen_tether:** Volúmen total de transacciones del tether.  
**precio_binance:** Precio histórico de binance.  
**mercado_caps_binance:** Capitalización del mercado de binance.  
**total_volumen_binance:** Volúmen total de transacciones del binance.  



4-**df_olhc_btc.**  
**fecha:** Fecha
**precio_apertura_bitcoin:** Precio de apertura.  
**precio_maximo_bitcoin:** Precio máximo.  
**precio_minimo_bitcoin:** Precio mínimo.  
**precio_cierre_bitcoin:** Precio de cierre.

5-**df_olhc_ethereum**  
Igual al anterior, pero para ethereum.  

6-**df_olhc_tether**
Igual al primero. pero para el tether.

7-**df_olhc_binance.**  
Igual al primero. pero para el binace.


**enlace al unforme:** https://drive.google.com/file/d/1uyFkoGIuvIRqx3fRFE6c1BWHaQQ4vGaf/view?usp=sharing

