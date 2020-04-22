b = int(input("Si posee una cuenta en curso ingrese 1 , para empezar una nueva cuenta, ingrese 0: "))
a = input("Digite el nombre del archivo que posee las nuevas transacciones: ")

if b == 0 :
    caja = 0
    apSocial = 0
    bancos = 0
    MercanciasNF = 0
    Terrenos = 0
    Construcciones = 0
    Maquinaria = 0
    EquiposCompu = 0
    EquipoDeOficina = 0
    BancosNal = 0
    BancosExtra = 0
    ProveedoresNal = 0
    ProveedoresExt = 0
elif b ==1 :
    historial = open("Obri.txt","r+")
    for i in historial:
        if i.split()[4] == "caja":
            caja = int(i.split()[0])
        elif i.split()[4] == "aporte":
            apSocial = int(i.split()[0])
        elif i.split()[4] == "bancos":
            bancos = int(i.split()[0])
        elif i.split()[4] == "Mercancias":
            MercanciasNF = int(i.split()[0])
        elif i.split()[4] == "Terrenos":
             Terrenos = int(i.split()[0])
        elif i.split()[4] == "Construcciones":
             Construcciones = int(i.split()[0])
        elif i.split()[4] == "Maquinaria":
             Maquinaria = int(i.split()[0])
        elif i.split()[4] == "Equipos" and i.split()[6] == "computo":
             EquiposCompu= int(i.split()[0])
        elif i.split()[4] == "Equipos" and i.split()[6] == "oficina":
             EquiposDeOficina = int(i.split()[0])
        elif i.split()[4] == "Bancos" and i.split()[5] == "nacionales":
             BancosNal = int(i.split()[0])
        elif i.split()[4] == "Bancos" and i.split()[5] == "extranjeros":
             BancosExtra = int(i.split()[0])
        elif i.split()[4] == "Proveedores" and i.split()[5] == "nacionales":
             ProveedoresNal = int(i.split()[0])
        elif i.split()[4] == "Proveedores" and i.split()[5] == "extranjeros":
             ProveedoresExt = int(i.split()[0])
    historial.close()

lectura = open(a,"r")
respuesta = open("Obri.txt","w")

for i in lectura:
    a = i.split()[0]
    if i.split()[1] == "1105" :
      try: 
       caja += int(i.split()[2])
      except:
         caja = 0
         caja += int(i.split()[2])
    elif i.split()[1] == "3115":
      try:
       apSocial += int(i.split()[2])
      except:
       apSocial = 0
       apSocial += int(i.split()[2])
    elif i.split()[1] == "1110":
       try:
         bancos += int(i.split()[2])
       except:
         bancos = 0
         bancos += int(i.split()[2])
    elif i.split()[1] == "1435":
       try:
         MercanciasNF += int(i.split()[2])
       except:
         MercanciasNF = 0
         MercanciasNF += int(i.split()[2])
    elif i.split()[1] == "1504":
       try:
          Terrenos += int(i.split()[2])
       except:
           Terrenos = 0
           Terrenos += int(i.split()[2])
    elif i.split()[1] == "1516": 
        try:
            Construcciones += int(i.split()[2])
        except:
            Construcciones = 0
            Construcciones += int(i.split()[2])
    elif i.split()[1] == "1520":
        try:
            Maquinaria += int(i.split()[2])
        except:
            Maquinaria = 0
            Maquinaria += int(i.split()[2])
    elif i.split()[1] == "1528":
        try:
            EquiposCompu += int(i.split()[2])
        except:
            EquiposCompu = 0
            EquiposCompu += int(i.split()[2])
    elif i.split()[1] == "1524" :
        try:
            EquipoDeOficina += int(i.split()[2])
        except:
            EquipoDeOficina = 0
            EquipoDeOficina += int(i.split()[2])
    elif i.split()[1] == "2105":
        try:
            BancosNal += int(i.split()[2])
        except:
            BancosNal = 0
            BancosNal += int(i.split()[2])
    elif i.split()[1] == "2110":
       try:
            BancosExtra += int(i.split()[2])
       except:
            BancosExtra = 0
            BancosExtra += int(i.split()[2])
    elif i.split()[1] == "2205":
        try:
            ProveedoresNal += int(i.split()[2])
        except:
            ProveedoresNal = 0
            ProveedoresNal += int(i.split()[2])
    elif i.split()[1] == "2210":
       try:
            ProveedoresExt += int(i.split()[2])
       except:
            ProveedoresExt = 0
            ProveedoresExt += int(i.split()[2])
    

try:        
 if caja != 0:
    respuesta.write(str(caja) + " Se poseen en caja al día: " + a + " \n")
except:
    None
try:
 if apSocial != 0:
    respuesta.write(str(apSocial) + " Se poseen en aporte social al día: " + a + " \n")
except:
    None
try:
 if bancos != 0:
    respuesta.write(str(bancos) + " Se poseen en bancos al día: " + a + " \n")
except:
    None
try:
  if MercanciasNF != 0:
    respuesta.write(str(MercanciasNF) + " Se poseen en Mercancías no fabricadas por la empresa al día: " + a + " \n")
except:
    None
try: 
   if  Terrenos != 0:
    respuesta.write(str(Terrenos) + " Se poseen en Terrenos al día: " + a + " \n")
except:
    None
try:
  if Construcciones != 0:
    respuesta.write(str(Construcciones) + " Se poseen en Construcciones y edificaciones al día: " + a + " \n")
except:
    None
try:
 if Maquinaria != 0:
    respuesta.write(str(Maquinaria) + " Se poseen en Maquinaria y Equipos al día: " + a + " \n")
except:
    None
try:
 if EquiposCompu != 0:
    respuesta.write(str(EquiposCompu) + " Se poseen en Equipos de computo y comunicaciones al día: " + a + " \n")
except:
    None
try:
 if EquipoDeOficina != 0:
    respuesta.write(str(EquipoDeOficina) + " Se poseen en Equipos de oficina al día: " + a + " \n")
except:
    None
try:
 if BancosNal != 0:
    respuesta.write(str(BancosNal) + " Se deben a Bancos Nacionales al día: " + a + " \n")    
except:
    None
try:
 if BancosExtra!= 0:
    respuesta.write(str(BancosExtra) + " Se deben a Bancos Extranjeros al día: " + a + " \n")    
except:
    None
try:
 if ProveedoresNal != 0:
    respuesta.write(str(ProveedoresNal) + " Se deben a Proveedores Nacionales al día: " + a + " \n")    
except:
    None
try:
 if ProveedoresExt!= 0:
    respuesta.write(str(ProveedoresExt) + " Se deben a Proveedores Extranjeros  al día: " + a + " \n")
except:
    None

lectura.close()    
respuesta.close()
