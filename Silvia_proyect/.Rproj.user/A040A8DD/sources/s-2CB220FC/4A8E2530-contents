# install_github("jtextor/dagitty/r")
require(dagitty)

# install.packages("ggdag")
require(ggdag)

# install.packages("wesanderson")
require(wesanderson)

## Representación de  diagrama causal  

#Quiero conocer el efeto de la disponibilidad  de refugios(D) sobre el % de superposición de los ámbitos de descanso (S) entre los grupos de Thyroptera tricolor. Pero tambien deseo saber  si el tamaño del grupo (TG) afecta % de superposicion de los ámbitos de descanso. 

#Modelo con un DAG:
  
# x = D
# z = TG
# y = S

# Crear DAG
dag1 <- dagify(S ~ D,
                   S ~ TG,
                   exposure = "D",
                   outcome = "S")

# compactar
tidy_dagitty(dag1)

# graficar  
ggdag(dag1, layout = "circle") + theme_dag() 

# La densidad de  refugios y el Tamaño del grupo son independientes entre sí, por lo que en mi analisis debería condicionar por ninguna de estas dos variables.
