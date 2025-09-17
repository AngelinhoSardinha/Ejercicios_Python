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


## Ejercicio_5

