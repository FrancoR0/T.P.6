[T.P.7.py](https://github.com/user-attachments/files/22981876/T.P.7.py)
"""
1) Escribir una clase llamada Rectángulo que contenga una base y una altura, y que contenga un método que devuelva el área
del rectángulo.
"""
#class rectangulo:
#    def __init__(self, base, altura):
#        self.base = base
#        self.altura = altura
#    def area(self):
#        return self.base * self.altura
#mi_rectangulo = rectangulo(4,8)
#are_del_rectangulo = mi_rectangulo.area()
#print(f"el area del rectangulo es {are_del_rectangulo}")

"""
2) Modelar una clase Mate que describa el funcionamiento de la conocida bebida tradicional argentina. La clase debe contener
como miembros:
   o Un atributo para la cantidad de cebadas restantes hasta que se lava el mate (representada por un número).
   o Un atributo para el estado (lleno o vacío).
   o Un atributo n, que indica la cantidad máxima de cebadas.
   o Un método cebar, que llena el mate con agua. Si se intenta cebar con el mate lleno, se debe lanzar una
excepción que imprima el mensaje ¡Cuidado! ¡Te quemaste!
   o Un método beber, que vacía el mate y le resta una cebada disponible. Si se intenta beber un mate vacío, se
debe lanzar una excepción que imprima el mensaje: ¡El mate está vacío!
   o Es posible seguir cebando y bebiendo el mate aunque no haya cebadas disponibles. En ese caso la cantidad
de cebadas restantes se mantendrá en 0, y cada vez que se intente beber se debe imprimir un mensaje de aviso:
“Advertencia: el mate está lavado.” pero no se debe lanzar una excepción.
"""

#class mate():
#    def __init__(self):
#        self.lavar = 0
#        self.cebar = 3
#        self.estado = "vacio"
#    def lavar(self):
#        if self.lavar == 0:
#            print("as lavado el mate")
#        else:
#            print("la llerva aun esta buena")
#    def estado(self):
#        if self.estado == "vacio":
#            print("el mate esta vasio")
#        else:
#            print("el mate esta lleno")
#    def cebadas_maximas(self):
#        print(f"cebaste el maximas {self.cebar}")
#    def llenar_mate(self):
#        if self.cebar == 0:
#            print("no te quedan cebadas.")
#        elif self.estado == "vacio":
#            self.estado = "lleno"
#            self.lavar = 3
#            self.cebar = self.cebar - 1
#            print("llenaste el mate con agua")
#        else:
#            print("¡Cuidado! ¡Te quemaste!")
#            self.cebar = self.cebar - 1
#    def beber(self):
#        if self.lavar == 0 and self.cebar == 0:
#            print("Advertencia: el mate está lavado.")
#        elif self.lavar == 0:
#            print("¡El mate está vacío!")
#            self.estado = "vacio"
#        else:
#            self.lavar = self.lavar - 1
#            print("tomaste mate")
#mate1 = mate()
#mate.beber(mate1)
#mate.estado(mate1)
#mate.llenar_mate(mate1)
#mate.llenar_mate(mate1)
#mate.estado(mate1)
#mate.beber(mate1)
#mate.beber(mate1)
#mate.cebadas_maximas(mate1)
#mate.beber(mate1)
#mate.beber(mate1)
#mate.llenar_mate(mate1)
#mate.beber(mate1)
#mate.beber(mate1)
#mate.beber(mate1)
#mate.beber(mate1)

"""
3) Botella y Sacacorchos
 Escribir una clase Corcho, que contenga un atributo bodega (cadena con el nombre de la bodega).
 Escribir una clase Botella que contenga un atributo corcho con una referencia al corcho que la tapa, o None si está
destapada.
 Escribir una clase Sacacorchos que tenga un método destapar que le reciba una botella, le saque el corcho y se guarde
una referencia al corcho sacado. Debe lanzar una excepción en el caso en que la botella ya esté destapada, o si el
sacacorchos ya contiene un corcho.
 Agregar un método limpiar, que saque el corcho del sacacorchos, o lance una excepción en el caso en el que no haya
un corcho.
"""
"""
class corcho():
    def __init__(self,bodega):
        self.bodega = bodega
    def __str__(self):
        return f"corcho de la bodega {self.bodega}"

class botella():
    def __init__(self,corcho):
        self.corcho = corcho
    def __str__(self):
        return self.corcho is not None
    
class sacacorcho():
    def __init__(self):
        self.corcho_guardado = None
    def destapar(self, botella):
        if self.corcho_guardado is not None:
            raise Exception("La botella ya está destapada.")
            
        elif self.corcho_guardado is None:
            raise Exception("Ya hay un corcho en el sacacorchos.")
        
        self.corcho_guardado = botella.corcho
        botella.corcho = None
        return self.corcho_guardado

    def limpiar(self):
        if self.corcho_guardado is None:
            raise Exception("No hay corcho para limpiar.")
        
        corcho_limpio = self.corcho_guardado
        self.corcho_guardado = None
        return corcho_limpio
try:
    corcho1 = corcho("bodega")
    botella = botella(corcho1)
    sacacorchos = sacacorcho()
except Exception as e:
    print("error:", e)
"""
"""
4) Una heladería es un tipo especial de restaurante. Cree una clase Restaurante, cuyo método __init__() guarde dos atributos:
restaurante_nombre y tipo_comida. Cree un método describir_restaurante() que muestre estas piezas de información, y un
método abrir_restaurante() que muestre un mensaje indicando que el restaurante ahora está abierto. Luego cree una clase
Heladeria que herede de Restaurante, y agregue a los existentes un atributo llamado sabores que almacene una lista de los
sabores de helado disponibles. Escriba también un método que muestre estos valores, cree una instancia de la clase y llame
al método. 
"""
#class restaurante():
#    def __init__(self,restaurante_nombre,tipo_comida):
#        self.restaurante_nombre = restaurante_nombre
#        self.tipo_comida = tipo_comida
#        
#    def describir_restaurante(self):
#        print(f"bienvenidi a restaurante {self.restaurante_nombre} tipo de comidas {self.tipo_comida}")

#    def abrir_restaurante(self):
#        print(f"el {self.restaurante_nombre} esta abierto")

#class heladeria(restaurante):
#    def __init__(self, restaurante_nombre, tipos_comida, lista_sabores):
#        super().__init__(restaurante_nombre, tipos_comida)
#        self.sabores = lista_sabores
#
#    def sabore(self):
#        print("sabores:")
#        for lista_sabores in self.sabores:
#            print(f"{lista_sabores}")

#mi_heladeria = heladeria("pepe", "helados", ["frutilla","vainilla","chocolate","limon"])
#restaurante.abrir_restaurante(mi_heladeria)
#restaurante.describir_restaurante(mi_heladeria)
#mi_heladeria.sabore()

"""
5) Escribir una clase Personaje que contenga los atributos vida, posicion y velocidad, y los métodos recibir_ataque, que
reduzca la vida según una cantidad recibida y lance una excepción si la vida pasa a ser menor o igual que cero, y mover
que reciba una dirección y se mueva en esa dirección la cantidad indicada por velocidad.
 Escribir una clase Soldado que herede de Personaje, y agregue el atributo ataque y el método atacar, que reciba otro
personaje, al que le debe hacer el daño indicado por el atributo ataque.
 Escribir una clase Campesino que herede de Personaje, y agregue el atributo cosecha y el método cosechar, que
devuelva la cantidad cosechada
"""
class personaje():
    def __init__(self, vida, posicion, velocidad):
        self.vida = vida
        self.posicion = posicion
        self.velocidad = velocidad

    def recibir_ataque(self, daño):
        self.vida = self.vida - daño
        print(f"as recibido {daño} de daño. cantidad de vida restante {self.vida}")
        if self.vida <= 0:
            print("as muerto")

    def moverse(self, posicion):
        if posicion == "izquierda":
            self.posicion = self.posicion + self.velocidad
            print(f"avanzas a la izquierda {self.velocidad} de lugares")
        elif posicion == "derecha":
            self.posicion = self.posicion - self.velocidad
            print(f"avanzas a la derecha {self.velocidad} de lugares")
class soldado(personaje):
    def __init__(self, vida, posicion, velocidad, ataque):
     super().__init__(vida, posicion, velocidad) 
     self.ataque = ataque

    def daño_hecho(self, enemigo):
        print(f"soldado ataca causando {self.ataque}")
        self.vida = self.vida - self.ataque
class campesino(personaje):
    def __init__(self, vida, posicion, velocidad, cosecha):
     super().__init__(vida, posicion, velocidad) 
     self.cosecha = cosecha
    def cosechar(self):
        print(f"as cosechó {self.cosecha} unidades.")
        return self.cosecha

soldado1 = soldado(100, (3,6,9,40,2), 0, 200)
campesino1 = campesino(50, (-3,7,-8,63,9), 0, 10)
personaje_yo = soldado(150 , 0, 1 , 100)

soldado.moverse(personaje_yo, "derecha")
soldado.moverse(personaje_yo, "derecha")
soldado.moverse(personaje_yo, "derecha")
soldado.daño_hecho(soldado1, personaje_yo)






















"""
6) Usuarios: Cree una clase Usuario. Cree también dos atributos nombre y apellido, así como otros atributos que típicamente
se guardan en un perfil de usuario. Escriba un método describir_usuario() que muestre un resumen de la información del
usuario. Escriba otro método saludar_usuario() que muestre un saludo personalizado al usuario.
Cree varias instancias que representen distintos usuarios y llame ambos métodos para cada uno.
"""
"""
class usuario:
    def __init__(self, nombre, apellido, email, edad):
        self.nombre = nombre
        self.apellido = apellido
        self.email = email
        self.edad = edad

    def describir_usuario(self):
        print(f"Información del usuario:\n",
                f"Nombre completo: {self.nombre} {self.apellido}\n",
                f"Email: {self.email}\n"
                f"Edad: {self.edad}")

    def saludar_usuario(self):
        print(f"¡Hola, {self.nombre}! Es un placer verte.")

#usuario1 = usuario("Ana", "García", "anacia@email.com", 30, "bannear personas")
#usuario2 = usuario("Juan", "Pérez", "juarez@email.com", 25)
#usuario3 = usuario("María", "López", "maripez@email.com", 35)

#usuario1.describir_usuario()
#usuario1.saludar_usuario()

#usuario2.describir_usuario()
#usuario2.saludar_usuario()

#usuario3.describir_usuario()
#usuario3.saludar_usuario()
"""
"""
7) Admin: Un administrador es un tipo de usuario con privilegios especiales. Cree una clase Admin que herede de la clase
Usuario del ejercicio anterior y agréguele un atributo privilegios que almacene una lista de strings tales como “puede
postear en el foro”, “puede borrar un post”, “puede banear usuario”, etc. Escriba un método mostrar_privilegios() que
muestre el conjunto de privilegios del administrador, cree una instancia de la clase y llame al método.
"""
"""
class privilegios(usuario):
    def __init__(self, nombre, apellido, email, edad, privilegios):
        super().__init__(nombre, apellido, email, edad)
        self.privilegios = privilegios

#    def mostrar_privilegios(self):
#        print("Los privilegios del usuario son:")
#        for privilegio in self.privilegios:
#            print(f"- {privilegio}")

usuario1 = usuario("Ana", "García", "anacia@email.com", 30, "banner")
usuario1.describir_usuario(usuario1)
print(usuario1.privilegios)
"""





















