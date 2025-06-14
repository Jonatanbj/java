# Visibilidad de Miembros









| 
* Los miembros declarados ***public*** son accesibles desde cualquier código exterior al paquete
* Los miembros declarados ***private*** sólo son accesibles desde el código de esa clase


 | 
* Los miembros declarados ***protected*** son accesibles desde el código de esa clase, de sus clases derivadas de cualquier paquete, y del resto de clases de ese paquete (no de sus subpaquetes)
* Los miembros que **no especifican ningún modificador** de acceso sólo son accesibles desde las clases de ese paquete (no de sus subpaquetes)


 |
| 
* **Modificador**


	+ *public*
	+ *protected*
	+ ninguno
	+ *private*



 | 
* **Desde su clase**


	+ **Si**
	+ **Si**
	+ **Si**
	+ **Si**



 | 
* **Desde su paquete**


	+ **Si**
	+ **Si**
	+ **Si**
	+ **No**



 | 
* **Desde sus subclases**


	+ **Si**
	+ **Si**
	+ **No**
	+ **No**



 | 
* **Desde el resto**


	+ **Si**
	+ **No**
	+ **No**
	+ **No**



 |


---

[Volver al nivel superior](../README.md)

[Siguiente sección: Paquetes y Herencia](../u5packagesAndInheritance/README.md)
