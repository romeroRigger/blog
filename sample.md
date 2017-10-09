# Conocer las funciones aplicables a un nodo con Pymel en Maya. Parte 1
Cuando se esta escribiendo un script normalmente se hace necesario conocer que funciones puedo aplicar a determinados nodos, la documentación de Maya es extensa y toma tiempo acostumbrarse a reconocer las funciones que sirven para cada caso particular.

```
La respuesta a este pequeño problema la he encontrado usando pyMEL, donde con el uso de pyNode y  see() , podemos tener un listado de las funciones que podemos usar.
```

Teniendo como punto de partida lo anterior, explicare los pasos a seguir:

1. instalar python (opcional)  [Download Python | Python.org](https://www.python.org/downloads/) 
2. descargar y/o instalar see()  [see 1.3.2 : Python Package Index](https://pypi.python.org/pypi/see) 
3. copiar *see()* en la carpeta de [scripts de Maya](https://knowledge.autodesk.com/support/maya/learn-explore/caas/CloudHelp/cloudhelp/2016/ENU/Maya/files/GUID-228CCA33-4AFE-4380-8C3D-18D23F7EAC72-htm.html)

4. Ejemplo con funciones aplicables al /shape/ de un polígono 

![pasos](/var/folders/rv/czftgw5500x8kdbchwj14zk00000gn/T/net.shinyfrog.bear/BearTemp.P8cwDy/pasos.jpg)



aclaro que podemos usar dir() de igual forma que see(), la visualización de los resultados as mas amigable con see().

La próxima semana, la *Parte 2* de este pequeño tutorial, donde aplicaremos en un caso particular lo anteriormente descrito.


### referencias:
[Why PyMEL? — PyMEL 1.0.8 documentation](http://help.autodesk.com/cloudhelp/2016/ENU/Maya-Tech-Docs/PyMel/why_pymel.html)
[PyNodes — PyMEL 1.0.8 documentation](http://help.autodesk.com/cloudhelp/2016/ENU/Maya-Tech-Docs/PyMel/pynodes.html?highlight=pynode)
[GitHub - LumaPictures/pymel: Python in Maya Done Right](https://github.com/LumaPictures/pymel)
[python Built -in functions](https://docs.python.org/2/library/functions.html)
