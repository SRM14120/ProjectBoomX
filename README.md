b = int(input("Si posee una cuenta en curso ingrese 1 , para empezar una nueva cuenta, ingrese 0: "))
g = int(input("Para crear un archivo digite 0, para subir un archivo digite 1: "))
if g == 1:
   a = input("Digite el nombre del archivo que posee las transacciones: ")
else:
   h = int(input("Digite el número de transacciones a declarar: "))
   f = input("Digite la fecha de la transacción a digitar")
   v = f +".txt"
   hola = open(v,"w")
   hola.write("FECHA      CODIGO      VALOR \n")
   for i in range (0,h):
       r = input("Digite el código a declarar: ")
       d = input("Digite el valor del código: ")
       hola.write(f + "      "+r+"      "+d+"\n")
   hola.close()
   a = v

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
    Licencias = 0
    Patentes = 0
    DeudasSocios = 0
    AcreedoresVa = 0
    RteFte = 0
    ImpRenta = 0
    ImpValor = 0
    CapitalA = 0
    AportesE = 0
    FondoSoci = 0
    Donaciones = 0
    AjustesInfl = 0
    Utilidad = 0
    Perdidas = 0
    Valorizaciones = 0
    EquipoTrans = 0
    Proviciones = 0
    Materias = 0
    ProductosT = 0
    
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
        elif i.split()[4] == "Licencias":
             Licencias = int(i.split()[0])
        elif i.split()[4] == "Patentes":
             Patentes = int(i.split()[0])
        elif i.split()[4] == "Deudas":
             DeudasSocios = int(i.split()[0])
        elif i.split()[4] == "Acreedores":
             AcreedoresVa = int(i.split()[0])
        elif i.split()[4] == "Retencion":
             RteFte = int(i.split()[0])
        elif i.split()[4] == "Impuesto" and i.split()[6] == "valorizacion":
             ImpValor = int(i.split()[0])
        elif i.split()[4] == "Capital":
             CapitalA = int(i.split()[0])
        elif i.split()[4] == "Aportes":
             AportesE = int(i.split()[0])
        elif i.split()[4] == "Fondo":
             FondoSoci = int(i.split()[0])
        elif i.split()[4] == "Donaciones":
             Donaciones = int(i.split()[0])
        elif i.split()[4] == "Ajustes":
             AjustesInfl = int(i.split()[0])
        elif i.split()[4] == "Utilidad":
             Utilidad = int(i.split()[0])
        elif i.split()[4] == "Pérdidas":
             Perdidas = int(i.split()[0])
        elif i.split()[4] == "Equipos" and i.split()[6] == "transportes":
             EquipoTrans = int(i.split()[0])
        elif i.split()[4] == "Proviciones":
             Proviciones = int(i.split()[0])
        elif i.split()[4] == "Materias":
             Materias = int(i.split()[0])
        elif i.split()[4] == "Productos":
             ProductosT = int(i.split()[0])
        elif i.split()[4] == "Valorizaciones":
             Valorizaciones = int(i.split()[0])
        elif i.split()[4] == "impuesto" and i.split()[6] == "renta":
             ImpRenta = int(i.split()[0])
             
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
    elif i.split()[1] == "1635":
       try:
            Licencias += int(i.split()[2])
       except:
            Licencias = 0
            Licencias += int(i.split()[2])
    elif i.split()[1] == "1615":
       try:
           Patentes += int(i.split()[2])
       except:
            Patentes = 0
            Patentes += int(i.split()[2])
    elif i.split()[1] == "2355":
       try:
            DeudasSocios += int(i.split()[2])
       except:
            DeudasSocios = 0
            DeudasSocios += int(i.split()[2])
      
    elif i.split()[1] == "2380":
      try:
           AcreedoresVa += int(i.split()[2])
      except:
           AcreedoresVa = 0
           AcreedoresVa += int(i.split()[2])
          
    elif i.split()[1] == "2365":
       try:
            RteFte += int(i.split()[2])
       except:
            RteFte = 0
            RteFte += int(i.split()[2])

    elif i.split()[1] == "2404":
       try:
            ImpRenta += int(i.split()[2])
       except:
            ImpRenta = 0
            ImpRenta += int(i.split()[2])

    elif i.split()[1] == "2424":
       try:
            ImpValor += int(i.split()[2])
       except:
            ImpValor = 0
            ImpValor += int(i.split()[2])
    elif i.split()[1] == "3120":
       try:
            CapitalA += int(i.split()[2])
       except:
            CapitalA = 0
            CapitalA += int(i.split()[2])
    elif i.split()[1] == "3135":
       try:
            AportesE += int(i.split()[2])
       except:
            AportesE = 0
            AportesE += int(i.split()[2])
    elif i.split()[1] == "3140":
       try:
            FondoSoci += int(i.split()[2])
       except:
            FondoSoci = 0
            FondoSoci += int(i.split()[2])
    elif i.split()[1] == "3210":
       try:
            Donaciones += int(i.split()[2])
       except:
            Donaciones = 0
            Donaciones += int(i.split()[2])
    elif i.split()[1] == "3405":
       try:
            AjustesInfl += int(i.split()[2])
       except:
            AjustesInfl = 0
            AjustesInfl += int(i.split()[2])
    elif i.split()[1] == "3605":
       try:
            Utilidad += int(i.split()[2])
       except:
            Utilidad = 0
            Utilidad += int(i.split()[2])
    elif i.split()[1] == "3610":
       try:
            Perdidas += int(i.split()[2])
       except:
            Perdidas = 0
            Perdidas += int(i.split()[2])
    elif i.split()[1] == "3810":
       try:
            Valorizaciones += int(i.split()[2])
       except:
            Valorizaciones = 0
            Valorizaciones += int(i.split()[2])
    elif i.split()[1] == "1540":
       try:
            EquipoTrans += int(i.split()[2])
       except:
            EquipoTrans = 0
            EquipoTrans += int(i.split()[2])
    elif i.split()[1] == "1599":
       try:
            Proviciones += int(i.split()[2])
       except:
            Proviciones = 0
            Proviciones += int(i.split()[2])
    elif i.split()[1] == "1405":
       try:
            Materias += int(i.split()[2])
       except:
            Materias = 0
            Materias += int(i.split()[2])
    elif i.split()[1] == "1430":
       try:
            ProductosT += int(i.split()[2])
       except:
            ProductosT = 0
            ProductosT += int(i.split()[2])
            
print(ImpRenta)
                    
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
    respuesta.write(str(MercanciasNF) + " Se poseen en Mercancias no fabricadas por la empresa al día: " + a + " \n")
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
    respuesta.write(str(BancosNal) + " Se deben a Bancos nacionales al día: " + a + " \n")    
except:
    None
    
try:
 if BancosExtra!= 0:
    respuesta.write(str(BancosExtra) + " Se deben a Bancos extranjeros al día: " + a + " \n")    
except:
    None
    
try:
 if ProveedoresNal != 0:
    respuesta.write(str(ProveedoresNal) + " Se deben a Proveedores nacionales al día: " + a + " \n")    
except:
    None
    
try:
 if ProveedoresExt!= 0:
    respuesta.write(str(ProveedoresExt) + " Se deben a Proveedores extranjeros  al día: " + a + " \n")
except:
    None

try:
 if Licencias != 0:
    respuesta.write(str(Licencias) + " Se poseen en Licencias al día: " + a + " \n")
except:
    None

try:
 if Patentes != 0:
    respuesta.write(str(Patentes) + " Se poseen en Patentes al día: " + a + " \n")
except:
    None

try:
 if DeudasSocios != 0:
    respuesta.write(str(DeudasSocios) + " Se deben a Deudas con socios al día: " + a + " \n")
except:
    None
    
try:
 if AcreedoresVa != 0:
    respuesta.write(str(AcreedoresVa) + " Se deben a Acreedores varios al día: " + a + " \n")
except:
    None

try:
 if RteFte != 0:
    respuesta.write(str(RteFte) + " Se deben de Retencion en la fuente al día: " + a + " \n")
except:
    None
    
try:
 if ImpValor != 0:
    respuesta.write(str(ImpValor) + " Se deben a Impuesto de valorizacion al día: " + a + " \n")
except:
    None
    
try:
 if CapitalA != 0:
    respuesta.write(str(CapitalA) + " Se archivan a Capital Asignado al día: " + a + " \n")
except:
    None
    
try:
 if AportesE != 0:
    respuesta.write(str(AportesE) + " Se archivan a Aportes del Estado al día: " + a + " \n")
except:
    None

try:
 if FondoSoci != 0:
    respuesta.write(str(FondoSoci) + " Se archivan a Fondo Social al día: " + a + " \n")
except:
    None
    
try:
 if Donaciones != 0:
    respuesta.write(str(Donaciones) + " Se archivan a Donaciones al día: " + a + " \n")
except:
    None 
  
try:
 if AjustesInfl != 0:
    respuesta.write(str(AjustesInfl) + " Se archivan a Ajustes por inflación al día: " + a + " \n")
except:
    None 
  
try:
 if Utilidad != 0:
    respuesta.write(str(Utilidad) + " Se archivan a Utilidad al día: " + a + " \n")
except:
    None   

try:
 if Perdidas != 0:
    respuesta.write(str(Perdidas) + " Se archivan a Pérdidas al día: " + a + " \n")
except:
    None 
 
try:
 if Valorizaciones!= 0:
    respuesta.write(str(Valorizaciones) + " Se archivan a Valorizaciones al día: " + a + " \n")
except:
    None

try:
 if EquipoTrans != 0:
    respuesta.write(str(EquipoTrans) + " Se poseen en Equipos de transportes al día: " + a + " \n")
except:
    None
    
try:
 if Proviciones != 0:
    respuesta.write(str(Proviciones) + " Se poseen en Proviciones al día: " + a + " \n")
except:
    None
    
try:
 if Materias != 0:
    respuesta.write(str(Materias) + " Se poseen en Materias primas al día: " + a + " \n")
except:
    None
    
try:
 if ProductosT != 0:
    respuesta.write(str(ProductosT) + " Se poseen en Productos terminados al día: " + a + " \n")
except:
    None
    
try:
    if ImpRenta != 0:
        respuesta.write(str(ImpRenta)+" Se deben a impuesto de renta al día: " + a + "\n")
except:
    None

lectura.close()    
respuesta.close()
