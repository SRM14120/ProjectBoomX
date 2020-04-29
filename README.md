b = int(input("Si posee una cuenta en curso ingrese 1 , para empezar una nueva cuenta, ingrese 0: "))
g = int(input("Para crear un archivo digite 0, para subir un archivo digite 1: "))
if g == 1:
   a = input("Digite el nombre del archivo que posee las transacciones: ")
else:
   h = int(input("Digite el número de transacciones a declarar: "))
   f = input("Digite la fecha de la transacción a digitar en formato día-mes-año sin dejas espacios: ")
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
    Activos = 0
    Pasivos = 0
    Patrimonio = 0
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
    ImpVehiculo = 0
    ImpLicores = 0
    SalariosPagar = 0
    Cesantias = 0
    Prima = 0
    Prestaciones = 0
    Indemnizaciones = 0
    PenJubilacion = 0
    CargosDif = 0
    UsoConst = 0
    UsoVehiculos = 0
    ActividadFinanciera = 0
    UsoPersonal = 0
    ValorizacionesA = 0
    
    
elif b ==1 :
    Activos = 0
    Pasivos = 0
    Patrimonio = 0
    historial = open("Obri.txt","r+")
    for i in historial:
        if i.split()[0] == "1105":
            caja = int(i.split()[3])
        elif i.split()[0] == "3115":
            apSocial = int(i.split()[4])
        elif i.split()[0] == "1110":
            bancos = int(i.split()[3])
        elif i.split()[0] == "1435":
             MercanciasNF = int(i.split()[3])
        elif i.split()[0] == "1504":
             Terrenos = int(i.split()[3])
        elif i.split()[0] == "1516":
             Construcciones = int(i.split()[3])
        elif i.split()[0] == "1520":
             Maquinaria = int(i.split()[3])
        elif i.split()[0] == "1528":
             EquiposCompu= int(i.split()[5])
        elif i.split()[0] == "1524":
             EquipoDeOficina = int(i.split()[5])
        elif i.split()[0] == "2105":
             BancosNal = int(i.split()[4])
        elif i.split()[0] == "2110":
             BancosExtra = int(i.split()[4])
        elif i.split()[0] == "2205":
             ProveedoresNal = int(i.split()[4])
        elif i.split()[0] == "2210":
             ProveedoresExt = int(i.split()[4])
        elif i.split()[0] == "1635":
             Licencias = int(i.split()[3])
        elif i.split()[0] == "1615":
             Patentes = int(i.split()[3])
        elif i.split()[0] == "2355":
             DeudasSocios = int(i.split()[5])
        elif i.split()[0] == "2380":
             AcreedoresVa = int(i.split()[4])
        elif i.split()[0] == "2365":
             RteFte = int(i.split()[6])
        elif i.split()[0] == "2424":
             ImpValor = int(i.split()[4])
        elif i.split()[0] == "3120":
             CapitalA = int(i.split()[4])
        elif i.split()[0] == "3135":
             AportesE = int(i.split()[5])
        elif i.split()[0] == "3140":
             FondoSoci = int(i.split()[4])
        elif i.split()[0] == "3210":
             Donaciones = int(i.split()[3])
        elif i.split()[0] == "3405":
             AjustesInfl = int(i.split()[5])
        elif i.split()[0] == "3605":
             Utilidad = int(i.split()[3])
        elif i.split()[0] == "3610":
             Perdidas = int(i.split()[3])
        elif i.split()[0] == "1540":
             EquipoTrans = int(i.split()[5])
        elif i.split()[0] == "1599":
             Proviciones = int(i.split()[3])
        elif i.split()[0] == "1405":
             Materias = int(i.split()[4])
        elif i.split()[0] == "1430":
             ProductosT = int(i.split()[4])
        elif i.split()[0] == "3810":
             Valorizaciones = int(i.split()[3])
        elif i.split()[0] == "2404":
             ImpRenta = int(i.split()[5])
        elif i.split()[0] == "2435":
             ImpVehiculo = int(i.split()[5])
        elif i.split()[0] == "2464":
             ImpLicores = int(i.split()[5])
        elif i.split()[0] == "2505":
             SalariosPagar = int(i.split()[5])
        elif i.split()[0] == "2510" :
             Cesantias = int(i.split()[3])
        elif i.split()[0] == "2520" :
             Prima = int(i.split()[3])
        elif i.split()[0] == "2530" :
             Prestaciones = int(i.split()[3])
        elif i.split()[0] == "2540" :
             Indemnizaciones = int(i.split()[3])
        elif i.split()[0] == "2620":
             PenJubilacion = int(i.split()[5])
        elif i.split()[0] == "1710":
             CargosDif = int(i.split()[4])
        elif i.split()[0] == "6130":
             UsoConst = int(i.split()[5])
        elif i.split()[0] == "6145":
             UsoVehiculos = int(i.split()[5])
        elif i.split()[0] == "6150":
             ActividadFinanciera = int(i.split()[4])
        elif i.split()[0] == "6170":
             UsoPersonal = int(i.split()[5])
        elif i.split()[0] == "19":
             ValorizacionesA = int(i.split()[5])
        
        
             
             
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
    elif i.split()[1] == "2436":
       try:
            ImpVehiculo += int(i.split()[2])
       except:
            ImpVehiculo = 0
            ImpVehiculo += int(i.split()[2])
    elif i.split()[1] == "2464":
       try:
            ImpLicores += int(i.split()[2])
       except:
            ImpLicores = 0
            ImpLicores += int(i.split()[2])
    elif i.split()[1] == "2505":
       try:
            SalariosPagar += int(i.split()[2])
       except:
            SalariosPagar = 0
            SalariosPagar += int(i.split()[2])
    elif i.split()[1] == "2510":
       try:
            Cesantias += int(i.split()[2])
       except:
            Cesantias = 0
            Cesantias += int(i.split()[2])
    elif i.split()[1] == "2520":
       try:
            Prima += int(i.split()[2])
       except:
            Prima = 0
            Prima += int(i.split()[2])
    elif i.split()[1] == "2530":
       try:
            Prestaciones += int(i.split()[2])
       except:
            Prestaciones = 0
            Prestaciones += int(i.split()[2])
    elif i.split()[1] == "2540":
       try:
            Indemnizaciones += int(i.split()[2])
       except:
            Indemnizaciones = 0
            Indemnizaciones += int(i.split()[2])
    elif i.split()[1] == "2620":
       try:
            PenJubilacion += int(i.split()[2])
       except:
            PenJubilacion = 0
            PenJubilacion += int(i.split()[2])
    elif i.split()[1] == "1524":
        try:
            EquipoDeOficina += int(i.split()[2])
        except:
            EquipoDeOficina = 0
            EquipoDeOficina += int(i.split()[2])
    elif i.split()[1] == "1710":
        try:
            CargosDif += int(i.split()[2])
        except:
            CargosDif = 0
            CargosDif += int(i.split()[2])
    elif i.split()[1] == "6130":
        try:
            UsoConst += int(i.split()[2])
        except:
            UsoConst = 0
            UsoConst += int(i.split()[2])
    elif i.split()[1] == "6145":
        try:
            UsoVehiculos += int(i.split()[2])
        except:
            UsoVehiculos = 0
            UsoVehiculos += int(i.split()[2])
    elif i.split()[1] == "6150":
        try:
            ActividadFinanciera += int(i.split()[2])
        except:
            ActividadFinanciera = 0
            ActividadFinanciera += int(i.split()[2])
    elif i.split()[1] == "6170":
        try:
            UsoPersonal += int(i.split()[2])
        except:
            UsoPersonal = 0
            UsoPersonal += int(i.split()[2])
    elif i.split()[1] == "19":
        try:
            ValorizacionesA += int(i.split()[2])
        except:
           ValorizacionesA = 0
           ValorizacionesA += int(i.split()[2])

            
            
respuesta.write("Su resumen de cuentas al día: " + a + "\n")
respuesta.write("Código\t\tCategoría\t\tDescripción\t\t\tValor\n")
               
try:        
  if caja != 0:
    respuesta.write("1105\t\tActivo\t\t\tCaja\t\t\t\t" + str(caja) + " \n")
    Activos += caja
except:
    None
    
try:
 if apSocial != 0:
    respuesta.write("3115\t\tPatrimonio\t\tAporte Social\t\t\t" + str(apSocial) + " \n")
    Patrimonio += apSocial
except:
    None
    
try:
 if bancos != 0:
    respuesta.write("1110\t\tActivo\t\t\tBancos\t\t\t\t" + str(bancos) + " \n")
    Activos += bancos
except:
    None
    
try:
  if MercanciasNF != 0:
    respuesta.write("1435\t\tActivo\t\t\tMercancias\t\t\t" + str(MercanciasNF) + " \n")
    Activos += MercanciasNF
except:
    None
    
try: 
   if  Terrenos != 0:
    respuesta.write("1504\t\tActivo\t\t\tTerrenos\t\t\t" + str(Terrenos) + " \n")
    Activos += Terrenos
except:
    None
    
try:
  if Construcciones != 0:
    respuesta.write("1516\t\tActivo\t\t\tConstrucciones\t\t\t" + str(Construcciones) + " \n")
    Activos += Construcciones
except:
    None
    
try:
 if Maquinaria != 0:
    respuesta.write("1520\t\tActivo\t\t\tMaquinaria\t\t\t" + str(Maquinaria) + " \n")
    Activos += Maquinaria
except:
    None
    
try:
 if EquiposCompu != 0:
    respuesta.write("1528\t\tActivo\t\t\tEquipos de Computo\t\t" + str(EquiposCompu) + " \n")
    Activos += EquiposCompu
except:
    None
        
try:
 if BancosNal != 0:
    respuesta.write("2105\t\tPasivo\t\t\tBancos Nacionales\t\t" + str(BancosNal) + " \n")    
    Pasivos += BancosNal
except:
    None
    
try:
 if BancosExtra != 0:
    respuesta.write("2110\t\tPasivo\t\t\tBancos Extranjeros\t\t" + str(BancosExtra) + " \n")    
    Pasivos += BancosExtra
except:
    None
    
try:
 if ProveedoresNal != 0:
    respuesta.write("2205\t\tPasivo\t\t\tProveedores Nacionales\t\t" + str(ProveedoresNal) + " \n")
    Pasivos += ProveedoresNal    
except:
    None
    
try:
 if ProveedoresExt!= 0:
    respuesta.write("2210\t\tPasivo\t\t\tProveedores Extranjeros\t\t" + str(ProveedoresExt) + " \n")
    Pasivos += ProveedoresExt
except:
    None

try:
 if Licencias != 0:
    respuesta.write("1635\t\tActivo\t\t\tLicencias\t\t\t" + str(Licencias) + " \n")
    Activos += Licencias
except:
    None

try:
 if Patentes != 0:
    respuesta.write("1615\t\tActivo\t\t\tPatentes\t\t\t" + str(Patentes) + " \n")
    Activos += Patentes
except:
    None

try:
 if DeudasSocios != 0:
    respuesta.write("2355\t\tPasivo\t\t\tDeudas con socios\t\t" + str(DeudasSocios) + " \n")
    Pasivos += DeudasSocios
except:
    None
    
try:
 if AcreedoresVa != 0:
    respuesta.write("2380\t\tPasivo\t\t\tAcreedores Varios\t\t" + str(AcreedoresVa) + " \n")
    Pasivos += AcreedoresVa
except:
    None

try:
 if RteFte != 0:
    respuesta.write("2365\t\tPasivo\t\t\tRetención en la fuente\t\t" + str(RteFte) + " \n")
    Pasivos += RteFte
except:
    None
    
try:
 if ImpValor != 0:
    respuesta.write("2424\t\tPasivo\t\t\tImpuesto valorización\t\t" + str(ImpValor) + " \n")
    Pasivos += ImpValor
except:
    None
    
try:
 if CapitalA != 0:
    respuesta.write("3120\t\tPatrimonio\t\tCapital Asignado\t\t" + str(CapitalA) + " \n")
    Patrimonio += CapitalA
except:
    None
    
try:
 if AportesE != 0:
    respuesta.write("3135\t\tPatrimonio\t\tAportes del Estado\t\t" + str(AportesE) + " \n")
    Patrimonio += AportesE
except:
    None

try:
 if FondoSoci != 0:
    respuesta.write("3140\t\tPatrimonio\t\tFondo Social\t\t\t" + str(FondoSoci) + " \n")
    Patrimonio += FondoSoci
except:
    None
    
try:
 if Donaciones != 0:
    respuesta.write("3210\t\tPatrimonio\t\tDonaciones\t\t\t" + str(Donaciones) + " \n")
    Patrimonio += Donaciones
except:
    None 
  
try:
 if AjustesInfl != 0:
    respuesta.write("3405\t\tPatrimonio\t\tAjustes por inflación\t\t" + str(AjustesInfl) + " \n")
    Patrimonio += AjustesInfl
except:
    None 
  
try:
 if Utilidad != 0:
    respuesta.write("3605\t\tPatrimonio\t\tUtilidad\t\t\t" + str(Utilidad) + " \n")
    Patrimonio += Utilidad
except:
    None   

try:
 if Perdidas != 0:
    respuesta.write("3610\t\tPatrimonio\t\tPérdidas\t\t\t" + str(Perdidas) + " \n")
    Patrimonio += Perdidas
except:
    None 
 
try:
 if Valorizaciones!= 0:
    respuesta.write("3810\t\tPatrimonio\t\tValorizaciones\t\t\t" + str(Valorizaciones) + " \n")
    Patrimonio += Valorizaciones
except:
    None

try:
 if EquipoTrans != 0:
    respuesta.write("1540\t\tActivo\t\t\tEquipo de Transportes\t\t" + str(EquipoTrans) + " \n")
    Activos += EquipoTrans
except:
    None
    
try:
 if Proviciones != 0:
    respuesta.write("1599\t\tActivo\t\t\tProviciones\t\t\t" + str(Proviciones) + " \n")
    Activos += Proviciones
except:
    None
    
try:
 if Materias != 0:
    respuesta.write("1405\t\tActivo\t\t\tMaterias Primas\t\t\t" + str(Materias) + " \n")
    Activos += Materias
except:
    None
    
try:
 if ProductosT != 0:
    respuesta.write("1430\t\tActivo\t\t\tProductos terminados\t\t" + str(ProductosT) + " \n")
    Activos += ProductosT
except:
    None
    
try:
  if ImpRenta != 0:
        respuesta.write("2404\t\tPasivo\t\t\tImpuesto de renta\t\t" + str(ImpRenta) + " \n")
        Pasivos += ImpRenta
        
except:
    None
try:
    if ImpVehiculo != 0:
        respuesta.write("2435\t\tPasivo\t\t\tImpuesto de vehiculo\t\t" + str(ImpVehiculo) + " \n")
        Pasivos += ImpVehiculo
except:
    None
try:
    if ImpLicores != 0:
        respuesta.write("2464\t\tPasivo\t\t\tImpuesto de Licores\t\t" + str(ImpLicores) + " \n")
        Pasivos += ImpLicores
except:
    None
try:
    if SalariosPagar != 0:
        respuesta.write("2505\t\tPasivo\t\t\tSalarios por pagar\t\t" + str(SalariosPagar) + " \n")
        Pasivos += SalariosPagar
except:
    None
try:
    if Cesantias != 0:
        respuesta.write("2510\t\tPasivo\t\t\tCesantias\t\t\t" + str(Cesantias) + " \n")
        Pasivos += Cesantias
except:
    None
try:
    if Prima != 0:
        respuesta.write("2520\t\tPasivo\t\t\tPrima\t\t\t\t" + str(Prima) + " \n")
        Pasivos += Prima
except:
    None
try:
    if Prestaciones != 0:
        respuesta.write("2530\t\tPasivo\t\t\tPrestaciones\t\t\t" + str(Prestaciones) + " \n")
        Pasivos += Prestaciones
except:
    None
try:
    if Indemnizaciones != 0:
        respuesta.write("2540\t\tPasivo\t\t\tIndemnizaciones\t\t\t" + str(Indemnizaciones) + " \n")
        Pasivos += Indemnizaciones
except:
    None
try:
    if PenJubilacion != 0:
        respuesta.write("2620\t\tPasivo\t\t\tPensiones de Jubulación\t\t" + str(PenJubilacion) + " \n")
        Pasivos += PenJubilacion
except:
    None

try:
    if EquipoDeOficina != 0:
        respuesta.write("1524\t\tActivo\t\t\tEquipo de oficina\t\t" + str(EquipoDeOficina) + " \n")
        Activos += EquipoDeOficina
except:
    None
try:
    if CargosDif != 0:
        respuesta.write("1710\t\tActivo\t\t\tCargos diferidos\t\t" + str(CargosDif) + " \n")
        Activos += CargosDif
except:
    None
try:
    if UsoConst != 0:
        respuesta.write("6130\t\tActivo\t\t\tUso de contrucción\t\t" + str(UsoConst) + " \n")
        Activos += UsoConst
except:
    None
try:
    if UsoVehiculos != 0:
        respuesta.write("6145\t\tActivo\t\t\tUso de vehículos\t\t" + str(UsoVehiculos) + " \n")
        Activos += UsoVehiculos
except:
    None
try:
    if ActividadFinanciera != 0:
        respuesta.write("6150\t\tActivo\t\t\tActividad financiera\t\t" + str(ActividadFinanciera) + " \n")
        Activos += ActividadFinanciera
except:
    None
try:
    if UsoPersonal != 0:
        respuesta.write("6170\t\tActivo\t\t\tUso de personal\t\t\t" + str(UsoPersonal) + "\n")
        Activos += UsoPersonal
except:
    None
try:
    if ValorizacionesA != 0:
        respuesta.write("19\t\tActivo\t\t\tValorizaciones de activos\t" + str(ValorizacionesA) + "\n")
        Activos += ValorizacionesA
except:
    None

respuesta.write("Se poseen en Activos : " + str(Activos) + "\n")
respuesta.write("Se poseen en Pasivos : " + str(Pasivos) + "\n")
respuesta.write("Se archivan en Patrimonio : " + str(Patrimonio) + "\n")

if Activos == Pasivos + Patrimonio :
    respuesta.write("Su cuenta está equilibrada ")
else:
    respuesta.write("Su cuenta no está equilibrada\n")
    respuesta.write("Verifique los siguientes posibles errores\n")
    try:
        if apSocial != 0:
            respuesta.write("- Verifique que haya registrado el aporte social en caja o en una cuenta bancaria\n")
    except:
        None
    try:
        if BancosNal != 0:
            respuesta.write("- Verifique que haya registrado el crédito de un banco nacional en caja o cuenta bancaria\n")
    except:
        None
    try:
        if BancosExtra != 0:
            respuesta.write("- Verifique que haya registrado el credito de un banco extranjero en caja o en una cuenta bancaria\n")
    except:
        None
    try:
        if ProveedoresNal != 0:
            respuesta.write("- Verifique que haya registrado la deuda con un proveedor nacional en mercancias\n")
    except:
        None
    try:
        if ProveedoresExt != 0:
            respuesta.write("- Verifique que haya registrado la deuda con un proveedor extranjero en mercancias\n")
    except:
        None
    try:
        if DeudasSocios != 0:
            respuesta.write("- Verifique que haya registrado la deuda con un socio de la empresa en caja o en una cuenta bancaria\n")
    except:
        None
    try:
        if AcreedoresVa != 0:
            respuesta.write("- Verifique que haya registrado la deuda con un acreedor en caja o en una cuenta bancaria\n")
    except:
        None
    try:
        if RteFte != 0:
            respuesta.write("- Verifique que haya registrado la retención en la fuente en cargos diferidos\n")
    except:
        None
    try:
        if ImpRenta != 0:
            respuesta.write("- Verifique que haya registrado el impuesto de renta en uso de construcciones\n")
    except:
        None
    try:
        if ImpValor != 0:
            respuesta.write("- Verifique que haya registrado el impuesto de valorización en uso de construcciones\n")
    except:
        None
    try:
        if ImpVehiculo != 0:
            respuesta.write("- Verifique que haya registrado el impuesto de vehículos en uso de vehículos\n")
    except:
        None
    try:
        if ImpLicores != 0:
            respuesta.write("- Verifique que haya registrado el impuesto de licores en actividad financiera\n")
    except:
        None
    try:
        if SalariosPagar != 0:
            respuesta.write("- Verifique que haya registrado los salarios por pagar en uso de personal\n")
    except:
        None
    try:
        if Cesantias != 0:
            respuesta.write("- Verifique que haya registrado las  cesantias en uso de personal\n")
    except:
        None
    try:
        if Prima != 0:
            respuesta.write("- Verifique que haya registrado la prima en uso de personal\n")
    except:
        None
    try:
        if Prestaciones != 0:
            respuesta.write("- Verifique que haya registrado las prestaciones en uso de personal\n")
    except:
        None
    try:
        if Indemnizaciones != 0:
            respuesta.write("- Verifique que haya registrado las indemnizaciones en uso de personal o actividad financiera\n")
    except:
        None
    try:
        if PenJubilacion != 0:
            respuesta.write("- Verifique que haya registrado la pension por jubilación en uso de personal\n")
    except:
        None
    try:
        if CapitalA!= 0:
            respuesta.write("- Verifique que haya registrado el capital asignado en caja o en una cuenta bancaria\n")
    except:
        None
    try:
        if AportesE != 0:
            respuesta.write("- Verifique que haya registrado el aportes del estado en caja o en una cuenta bancaria\n")
    except:
        None
    try:
        if FondoSoci != 0:
            respuesta.write("- Verifique que haya registrado el fondo social en caja o en una cuenta bancaria\n")
    except:
        None
    try:
        if Donaciones != 0:
            respuesta.write("- Verifique que haya registrado las donaciones en caja o en una cuenta bancaria\n")
    except:
        None
    try:
        if AjustesInfl != 0:
            respuesta.write("- Verifique que haya registrado los ajustes por inflación en caja o en una cuenta bancaria\n")
    except:
        None
    try:
        if Utilidad != 0:
            respuesta.write("- Verifique que haya registrado la utilidad en caja o en una cuenta bancaria\n")
    except:
        None
    try:
        if Perdidas != 0:
            respuesta.write("- Verifique que haya registrado las perdidas en caja o en una cuenta bancaria\n")
    except:
        None
    try:
        if Valorizaciones != 0:
            respuesta.write("- Verifique que haya registrado las valorizaciones en valorización de activos\n")
    except:
        None
    
    
  
    
    
    
        
        
lectura.close()    
respuesta.close()

print("\nSe ha creado un archivo llamado Obri.txt, alli encontrará el resumen de su cuenta hasta la última actualización")
