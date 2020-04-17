# ProjectBoomX
b = int(input("Si posee una cuenta en curso ingrese 1 , para empezar una nueva cuenta, ingrese 0: "))
a = input("Digite el nombre del archivo que posee las nuevas transacciones: ")

if b == 0 :
    caja = 0
    apSocial = 0
elif b ==1 :
    historial = open("Obri.txt","r+")
    for i in historial:
        if i.split()[4] == "caja":
            caja = int(i.split()[0])
        elif i.split()[4] == "aporte":
            apSocial = int(i.split()[0])
    historial.close()

lectura = open(a,"r")
respuesta = open("Obri.txt","w")

for i in lectura:
    if i.split()[1] == "1105" :
       caja += int(i.split()[2])
       respuesta.write(str(caja) + " Se poseen en caja al día: " + i.split()[0] + " \n")
    elif i.split()[1] == "3115":
       apSocial += int(i.split()[2])
       respuesta.write(str(apSocial) + " Se poseen en aporte social al día: " + i.split()[0] + " \n")
    
    
lectura.close()    
respuesta.close()
