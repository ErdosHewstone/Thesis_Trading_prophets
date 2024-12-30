# Trading prophets

Deseamos modelar la situación de una persona que buscar maximizar sus ganancias al comprar y luego vender un producto en múltiples ocasiones a distintos precios.


El modelo de trading prophets considera un agente que observa $n$ precios provenientes de distribuciones independientes $F_1,F_2...,F_n$ el agente puede en cada período:

1. Si no tiene el artículo puede decidir comprar una sola unidad.
2. Si tiene el artículo puede decidir venderlo.
3. En la última iteración siempre se venderá si se tiene el artículo.

Se desea encontrar una estrategia que le indique frente a que precios comprar y/o vender respectivamente con tal que se maximice la ganancia esperada del agente en comparación con la ganancia esperada de un "profeta" que conoce toda la secuencia de precios y actúa acorde:

#### Estrategia óptima
![image](https://github.com/user-attachments/assets/bcfcb120-4086-4a3b-a797-09a32ed1154c)

Considerando $\text{OPT}(X_{\sigma(1)},...,X_{\sigma(n)})$ como la ganancia del profeta sobre una secuencia específica de precios a los que se enfrenta de forma aleatoria según $\sigma$ y $\text{ALG}(X_{\sigma(1)},...,X_{\sigma(n)})$ como la ganancia del \textbf{algoritmo online} elegido como estrategia frente a la misma secuencia de precios. Anreviaremos en adelante $\text{OPT}$ y $\text{ALG}$ respectivamente a menos que se indique especificamente. 

Entonces buscaremos el algoritmo que nos entregue la mayor fracción $\alpha$ posible en

![image](https://github.com/user-attachments/assets/4ec129a3-7d72-4574-974b-1ca3d853c486)

### Estrategia de threshold simple
LLamaremos algoritmo de umbral simple a aquel que consiste en la estrategia de comprar y vender según un umbral $T$. 

En cada iteración $i$
1. Si no se tiene el articulo se comprará solamente si el precio es menor que $T$
2. Si se tiene el artículo se venderá si el precio es mayor o igual a $T$ o si $i=n$

#### Threshold simple
![image](https://github.com/user-attachments/assets/f0054435-4a67-4192-beaf-1ca569d6b9db)
