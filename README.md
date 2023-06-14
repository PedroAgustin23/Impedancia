#IMPEDANCIA
#Suma de Impedancias en serie
from math import sin,cos,atan2
print("================================================")
print("ESCRIBA LAS ÓRDENES EN MINÚSCULA Y SIN ESPACIOS")
print("================================================")
F=input("¿Tienen ambas impedancias en la misma forma?")
if F=="si":
   F1=input("\n¿En qué forma los tiene? ")
#Ambos vectores en forma polar
   if F1=="polar":
      M1=float(input("Módulo de Z1= "))
      θ1=float(input("Ángulo θ1 en °= "))
      M2=float(input("Módulo de Z2= "))
      θ2=float(input("Ángulo θ2 en °= "))
#Paso a cartesiana para la suma 
#R= parte real 
#J= parte imaginaria
      θ11=(θ1*3,1415926536)/180
      R1=cos(θ11)*M1
      J1=sin(θ11)*M1
      θ22=(θ2*3,1415926536)/180
      R2=cos(θ22)*M2
      J2=sin(θ22)*M2
#Producto
#Pm=producto de los módulos
#Pθ=ángulo del producto
      Pm=M1*M2
      Pθ=θ1+θ2
#Suma 
      Req=R1+R2
      Jeq=θ1+θ2
#Devuelta a polar 
#Ms=módulo de la suma
#θs=ángulo de la suma
      Ms=(Req**2+Jeq**2)**0.5
      θs1=atan2(Jeq,Req)
      θs=(θs1*180)/3.1415926536
#División
#Meq=módulo equivalente
#θeq=ángulo equivalente
      Meq=Pm/Ms
      θeq=Pθ-θs
#Resultado
      print("\nIMPEDANCIA EN FORMA POLAR=",round(Meq,2),"Ω [_",round(θeq,2),"°")
#Ambos vectores en forma cartesiana
   elif F1=="cartesiana":
   	R1=float(input("Ingrese la parte real 1= "))
   	J1=float(input("Ingrese la parte imaginaria 1= "))
   	R2=float(input("Ingrese la parte real 2= "))
   	J2=float(input("Ingrese la parte imaginaria 2= "))
#Paso a forma polar para el producto
#Mm=módulo para la multiplicación
#θm= ángulo para la multiplicación
   	Mm1=(R1**2+J1**2)**0.5
   	θm11=atan2(J1,R1)
   	θm1=(θm11*180)/3.1415926536
   	Mm2=(R2**2+J2**2)**0.5
   	θm22=atan2(J2,R2)
   	θm2=(θm22*180)/3.1415926536
#Producto
#Pm=producto de los módulos
#Pθ=ángulo del producto
   	Pm=Mm1*Mm2
   	Pθ=θm1+θm2
#Suma
   	Req=R1+R2
   	Jeq=J1+J2
#Paso a polar el resultado de la suma
#Ms=módulo de la suma
#θs=ángulo de la suma
   	Ms=(Req**2+Jeq**2)**0.5
   	θs1=atan2(Jeq,Req)
   	θs=(θs1*180)/3.1415926536
#División
#Meq=módulo equivalente
#θeq=ángulo equivalente
   	Meq=Pm/Ms
   	θeq=Pθ-θs
#Paso el resultado a forma cartesiana
#Req=parte real equivalente
#Jeq=parte imaginaria equivalente
   	θeq1=(θeq*3.1415926536)/180
   	Req=cos(θeq1)*Meq
   	Jeq=sin(θeq1)*Meq
#Resultado
   	print("\nIMPEDANCIA EN FORMA POLAR=",round(Meq,2),"Ω [_",round(θeq,2),"°")
   	print("\nIMPEDANCIA EN FORMA CARTESIANA=",round(Req,2),"+ J",round(Jeq,2))
#Errores de sintáxis
   else:
   	print("\nHa tenido un error de sintáxis, reescriba las órdenes nuevamente prestando atención a las letras y recuerde escribir todo en MINÚSCULAS y SIN ESPACIOS")
else:
   	print("\nHa tenido un error de sintáxis, reescriba las órdenes nuevamente prestando atención a las letras y recuerde escribir todo en MINÚSCULAS y SIN ESPACIOS")
print("\nFin del programa, espero que le de un buen uso")
