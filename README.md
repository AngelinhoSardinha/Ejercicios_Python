# Ejercicios_Python

## Ejercicio_1

def calculo_agua(litros):

     if litros < 50:
             return 6
     elif litros >= 50 and litros <= 200:
             return litros * 0.1
     else:
             return litros * 0.3

litros = int(input('¿Cuantos litros ha consumido?\n'))
¿Cuantos litros ha consumido?
14

print(calculo_agua(litros))
6

## Ejercicio_2

def menu():

     print(""" Escoge el billete que quieres:
             1.- Billet senzill
             2.- TCasual
             3.- TMes
             4.- TTrimestre
             5.- TJove
             6.- Salir """)	 
     opcion = int(input('Selecciona el numero de la opcion que quieras\n'))
     seleccion_zona(opcion)
	 
def seleccion_zona(opcion):

	precio_total = 0
	match opcion:
		case 1:
			zona = int(input('seleccione la zona 1, 2 o 3\n'))
			if zona == 1:
				precio_total = 2.20 * 1
			elif zona == 2:
				precio_total = 2.20 * 1.35
			elif zona == 3:
				precio_total = 2.20 * 1.89
			else:
				print("zona no valida")
				return
			pago(precio_total) 
		case 2:
			zona = int(input('seleccione la zona 1, 2 o 3\n'))
			if zona == 1:
				precio_total = 10.20 * 1
			elif zona == 2:
				precio_total = 10.20 * 1.35
			elif zona == 3:
				precio_total = 10.20 * 1.89
			else:
				print("zona no valida")
				return
			pago(precio_total)
		case 3: 
			zona = int(input('seleccione la zona 1, 2 o 3\n'))
			if zona == 1:
				precio_total = 54.00 * 1
			elif zona == 2:
				precio_total = 54.00 * 1.35
			elif zona == 3:
				precio_total = 54.00 * 1.89
			else:
				print("zona no valida")
				return 
			pago(precio_total)
		case 4: 
			zona = int(input('seleccione la zona 1, 2 o 3\n'))
			if zona == 1:
				precio_total = 145.30 * 1
			elif zona == 2:
				precio_total = 145.30 * 1.35
			elif zona == 3:
				precio_total = 145.30 * 1.89
			else:
				print("zona no valida")
				return
			pago(precio_total)
		case 5:
			zona = int(input('seleccione la zona 1, 2 o 3\n'))
			if zona == 1:
				precio_total = 105.00 * 1
			elif zona == 2:
				precio_total = 105.00 * 1.35
			elif zona == 3:
				precio_total = 105.00 * 1.89
			else:
				print("zona no valida")
				return
			pago(precio_total) 
		case 6:
			print("saliendo...")
		case _:
			menu()
   
def pago(precio_total):

    print(f"Debes pagar {precio_total:.2f} €")
    precio_nuevo = precio_total
    billetes_validos = [0.01, 0.05, 0.10, 0.20, 0.50,
                        1.00, 5.00, 10.00, 20.00,
                        50.00, 100.00, 200.00, 500.00]
    while precio_nuevo > 0:
        money = float(input("¿Con qué billete/moneda quieres pagar? "))
        if money in billetes_validos:
            precio_nuevo -= money
            if precio_nuevo > 0:
                print(f"Faltan {precio_nuevo:.2f} €")
        else:
            print("El billete/moneda no es válido")
    # cuando el while termina, es porque precio_nuevo <= 0
    if precio_nuevo == 0:
        print("Pago completo, gracias por tu compra")
    else:
        print(f"Pago completo, tu cambio es {abs(precio_nuevo):.2f} €")
    menu()  

## Ejercicio_3


## Ejercicio_4

def fibonacci(cantidad):

    a, b = 1, 1  
    for i in range(cantidad):
        print(a, end=' ')
        a, b = b, a + b

def menu():

    opcion = int(input(print(""" Selecciona tu opcion (1 o 2)
              1.- Visualizar los n primero numeros de fibonacci.
              2.- Visualizar en un rango dado por ti\n""")))
    
    seleccion_de_metodo(opcion)

def seleccion_de_metodo(opcion):

    match opcion:
        case 1:
            cantidad = int(input("Diga un numero n para calcular los n primeros numeros de fobonacci:\n"))
            fibonacci(cantidad)
        case 2:
            rango_1 = int(input("Seleccione desde donde quiere empezar el calculo:\n"))
            rango_2 = int(input("Seleccione el rango 2, que es en donde quiere termiar la serie:\n"))
            fibonacci_por_rango(rango_1, rango_2)
        case _:
            print("NO ES UNA OPCION VALIDA")
            menu()

def fibonacci_por_rango(rango_1, rango_2):

    a, b = 1, 1
    contador = 0  
    while contador < rango_2:  
        if a >= rango_1:  
            print(a, end=' ')
        a, b = b, a + b
        contador += 1 

## Ejercicio_5

