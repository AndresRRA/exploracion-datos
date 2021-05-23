# Datos hidrológicos, ejercicio explorativo

## Cargando los datos del archivo CSV dentro de RStudio.

Es importante asegurarse fijar el _"working directory"_ en el folder donde se encuentre el archivo CSV, ya que si no el programa RStudio no puede hallar el archivo. Esto se logra mediante la función `setwd("C:/Users/[[nombre del usuario]]/[[dirección que de directamente al folder donde se encuentra el archivo]")`. La función `head(inp)` le ayuda a uno a verificar que se escogió el archivo correcto mostrando el comienzo de dicho documento; la función `dim(inp)` le da a uno las dimensiones del documento, en este caso siendo 3845 líneas y 3 columnas.  

> inp <- read.csv("FDC.csv", na.strings="")
>  
> head(inp)   
> dim(inp)
  
 ## Graficación de los datos.
 
 Una vez cargados los datos del CSV en la memoria, se procede a graficar los datos de la columna 2 y columna 3 del archivo CSV.
 
> plot(inp[,2], type = "l", col="blue",   
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; main= 'Comparación de datos entre Río Estrella y Río Banano',  
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; xlab = 'Fecha', ylab = 'Datos')  
>lines(inp[,3],col="green")  
>legend(1, 140, legend=c("Río Estrella", "Río Banano"),   
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; col=c("blue","green"),lty=1:1, cex=0.8)
