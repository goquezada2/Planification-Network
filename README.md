# Planification-Network

'''
Para solucionar este problema de asignación de rutas se propone implementar un
simulador que sea capaz de planificar y asignar a algún cliente, un set de rutas viables y
mostrar ciertas características de cada ruta seleccionada, esto a través de algoritmos de
rutas más cortas que cumplan las condiciones de calidad de transmisión (QoT) basado
en la métrica de BER y SNR, esto para que el cliente pueda seleccionar que ruta le
conviene más según sus necesidades.

El algoritmo estará dividido en 6 etapas, la cuales son:
Etapa 1: Requisitos de entrada
Aqu´ı se pedir´an por teclado al usuario una serie de datos que nos ayudar´a a que
el algoritmo obtenga los mejores resultados para los requerimientos de calidad de
servicio que desee. Estos datos ser´an la topolog´ıa de red, la banda de operaci´on,
la tasa de bits, el umbral del BER eficiente y los nodos de origen y destino del
servicio requerido.
Etapa 2: Lectura de datos y construcci´on de la red
Aqu´ı se leer´a el archivo que tiene la topolog´ıa y la construir´a mediante una
funci´on explicada mas adelante. A dem´as se leen los datos ingresados por teclado
y se crea una funci´on que calcula el par´ametro de calidad de servicio.
Etapa 3: B´usqueda de la ruta m´as corta
En esta etapa se buscar´an las rutas m´as cortas seg´un su cantidad de salto y
distancia, las cuales se obtendr´an con una funci´on de la librer´ıa networkX. La
idea es encontrar un grupo de rutas y para eso se dise˜nar´a una funci´on que realice
todo este proceso.
Etapa 4: Calculo del SNR
En esta etapa tomaremos las rutas seleccionadas en la etapa 3, para obtener
el SNR, el cual usaremos para cuantificar y poder comparar con el par´ametro
de QoS que nos requiere el servicio. A dem´as se contara el numero de saltos, la
distancia total de la ruta y el numero de amplificadores necesarios en la ruta.
Etapa 5: Filtro final
Ya con el OSNR calculado, se calcula el BER para poder compararlo con el
BER requerido por teclado. Si el valor obtenido es menor al requerido la ruta es
'''
