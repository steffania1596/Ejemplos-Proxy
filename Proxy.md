# Patrón estructual proxy

# Proposito:

“El patrón proxy trata de proporcionar un objeto intermediario que represente o sustituya al objeto original con motivo de controlar el acceso y otras características del mismo.” 

# Aplicaciones:

Proxy remoto: representa un objeto en otro espacio de direcciones.
Proxy virtual: retrasa la creación de objetos costosos.
Proxy de protección: controla el acceso a un objeto.
Referencia inteligente: tiene la misma finalidad que un puntero pero además ejecuta acciones adicionales sobre el objeto, como por ejemplo el control de concurrencia.

# Caracteristica:
El cliente ignora totalmente que una mediación se está llevando acabo debido a que el objeto recibe un objeto identico en estructura al esperado y no es consciente de la implementación tras la interface ejecutada, así el cliente interactua con el proxy sin saberlo. 

# Componentes del diagrama de clases:[1]
 ![alt text](https://reactiveprogramming.io/public/books/patterns/img/patterns-articles/proxy-diagram.png) 

-IObject: Interfaz común entre el Objet y el Proxy.

-Object: El objeto al que el cliente quiere ejecutar.

-Proxy: Clase que implementa IObject y delega la responsabilidad al Object, sin embargo, puede realizar una acción antes y después de llamar al Object.

   
   # Diagrama de secuencias: [1]
   
 ![alt text](https://reactiveprogramming.io/public/books/patterns/img/patterns-articles/proxy-sequence.png) 
 
 
-Cliente solicita al Factory un Objeto.
-Factory crea un Proxy que encapsule al Object.
-Cliente ejecuta el Proxy creado por el Factory.
-Proxy realiza una o varias acciones previas a la ejecución del Object.
-Proxy delega la ejecución al Object.
-Proxy realiza una o varias acciones después de la ejecución del Object.
-Proxy regresa un resultado.
 
Referencias:
[1]https://reactiveprogramming.io/books/design-patterns/es/catalog/proxy
