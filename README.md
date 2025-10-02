# taller_poo_modificadores_acceso_python

En este repositorio se encuentra el taller de POO y modificadores de acceso en Python junto con sus respuestas. 

Respuestas : 
1.
  A) a.x
  
  B) a._y
  
  D) a._A__z

  
2.
  R: False True

  
3. 
  A) R: Falso: _nombre es solo una convención que indica “uso interno” pero no impide el acceso.

  B) R: Falso: __nombre aplica name-mangling pero no es imposible acceder ya que se puede con
  
      _Clase__nombre.
      
  C) R: Verdadero: El atributo __x se transforma a _Clase__x, por ello depende del nombre de la clase
      donde se definió.

      
5. 
  R: Imprime: abc
  No hay error de acceso debido a que usa la convención de protegido pero sigue siendo accesible
  desde la subclase, por lo que no hay como tal una restricción a su acceso.


6.  
  R : (2, 1)


7. 
  R: Cuando se intenta reasignar el valor ocurre un error debido a que __slots__ solo permite
  x, no permite y.


8.
  R: self._b = 99


9.
  R: True False True
  Imprime esto debido a que el primero '_step' está protegido, pero se puede
  acceder a él e imprime true, el segundo como fue mangleado y no fue
  correctamente llamado imprime false, y el ultimo si fue bien llamado
  entonces imprime true


10.
  R: print(s._S__data)


11.
  R: El mas probable es _D__a debido a que es un atributo privado entonces lo renombra de esta
  manera _NombreDeLaClase__nombre y lo muestra de esta manera.


12.
  return self._saldo
   if value < 0:
   raise ValueError("El saldo no puede ser negativo")
   self._saldo = value


13. 
  ra_f(self):
   return self._c * 9/5 + 32


14. 
  :
 def nombre(self, value):
   if not isinstance(value, str):
 raise TypeError("nombre debe ser str")
 self._nombre = value


15. 
  R: def items(self):
     return tuple(self.__items)


16. 
  @property
   def velocidad (self):
  return self._velocidad
  @velocidad.setter
  def velocidad (self,value):
  if not (0 <= value <= 200):
  raise ValueError("velocidad debe estar entre 0 y 200")
  self._velocidad = value


17. 
  R: El _atributo se usaría como para marcar un atributo que solo se puede usar o acceder a el si
  es necesario, ósea como tratar de acceder a el lo menos posible pero si es necesario hacerlo, y el
  __atributo considero que solo se usaría para evitar confundir atributos entre clases o para
  dificultar un poco su acceso haciéndolo un poco mas privado, sin embargo se sigue logrando
  acceder a el.


18.
  R: El problema es que al devolver la lista, se devuelve la original no una copia, entonces si la llega
a modificar se pueden perder datos.

  R: Cambiar “def get_data(self):” por esta ya que esta no es modificable.
def get_data(self):
 return tuple(self._data)


18. 
  R: Fallara al momento de intentar acceder a self.__x desde la subclase por lo que la solución es
  dejar el atributo protegido y no privado, de esta manera self._x


19.
  R:
def guardar(self, k, v):
 self.__repo.guardar(k, v)


20. 
R:
  class ContadorSeguro:
   def __init__(self):
   self._n = 0
   def inc(self):
   self._n += 1
   self.__log()
   @property
   def n(self):
   return self._n
   def __log(self):
   print("tick")
  # El uso básico
  c = ContadorSeguro()
  c.inc() # imprime "tick"
  c.inc() # imprime "tick"
  print(c.n) # imprime 2






  






