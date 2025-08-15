# [Visibilidad de Miembros](README.md)

* Los miembros declarados ***public*** son accesibles desde cualquier código exterior al paquete
* Los miembros declarados ***private*** sólo son accesibles desde el código de esa clase

* Los miembros declarados ***protected*** son accesibles desde el código de esa clase, de sus clases derivadas de cualquier paquete, y del resto de clases de ese paquete (no de sus subpaquetes)
* Los miembros que **no especifican ningún modificador** de acceso sólo son accesibles desde las clases de ese paquete (no de sus subpaquetes)


| Modificador   | Desde su clase | Desde su paquete | Desde sus subclases | Desde el resto |
|---------------|:--------------:|:----------------:|:-------------------:|:--------------:|
| `public`      | Sí             | Sí               | Sí                  | Sí             |
| `protected`   | Sí             | Sí               | Sí                  | No             |
| *(ninguno)*   | Sí             | Sí               | No                  | No             |
| `private`     | Sí             | No               | No                  | No             |

**Notas:**
- Los miembros `public` son accesibles desde cualquier código.
- Los miembros `private` sólo desde la propia clase.
- Los miembros `protected` desde la clase, subclases (aunque estén en otros paquetes) y el mismo paquete.
- Sin modificador (`package-private`): sólo accesibles desde el mismo paquete.



---

[Anterior](../u3classifierImporting/README.md) | [Subir nivel](../README.md) | [Siguiente](../u5packagesAndInheritance/README.md)
