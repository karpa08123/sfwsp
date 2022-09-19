# Pilas
Una pila es una lista ordenada o estructura de datos que permite almacenar y recuperar dtos, siendo el modo de acceso a sus elementos de tipo ***LIFO*** (Last In, First Out. Ultimo en entrar, primero en salir). Esta estructura se aplica en multitud de supuestos en el area de la informatica debido a su simplicidad y capacidad de dar respuesta a numerososo procesos.

Para el manejo de los datos cuenta con dos operaciones basicas:
**apilar (push)**, que coloca un objeto en la pila, y su operacion inversa, **retirar** (o desapilar, **pop**), que retira el ultimo elemento apilado.

En cada momento solamente se tiene acceso a la parte superior de la pila, es decir al ultimo objeto apilado (denominato ***TOS***, Top of Stack). La operacion ***retirar*** permite la obtencion de este elemento, que es retirado de la pila permitiendo el acceso al anterior (apilado con anterioridad), que pasa a ser el ultimo, el nuevo TOS.


## Sintaxis Java

### Pila.java

```SQL
Public interface Pila{
	public int longitud();
	public boolean esVacia();
	public void push(Object o);
	public Object pop();
	public onject primero();
}
```


#### PilaArray.java

```SQL
Public class PilaArray implements Pila{
	pivrate int top = 1;
	private Object s[];
	private int capacidad = 0;

	public PilaArray(){
	this(1000);
	}

	public PilaArray(int cap){
	capacidad=cap;
	s=new Object[capacidad];
	}

	public int longitud(){
	return(top+1);
	}

	public boolean esVacia(){
	return (top<0);
	}
}
```
