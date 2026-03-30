SECCIÓN B - CONDICIONALES ANIDADAS




SISTEMA QUE LIQUIDA EL SALARIO NETO MENSUAL:
- Tarifa de $35,000 COP por hora
- Límite de 160 horas regulares
- Recargo del 35% para horas extras
- Deducciones 

PROCEDIMIENTO

1.
   - Si horas > 160: separar en regulares (160) y extras (resto)
   - Si horas ≤ 160: todas son regulares

2. **Cálculo del Subtotal A 
   - Horas regulares × tarifa
   - Horas extras × tarifa × 1.35 (recargo 35%)

3. **Deducciones 
   - Deducción 1 (< $1,500,000): 4% salud 
   - Deducción 2 ($1,500,000 - $3,000,000): 6% salud + 2% pensión
   - Deducción 3 (≥ $3,000,000): 8% salud + 4% pensión + 1% fondo solidario

Código PSEINT

Algoritmo SistemadeLiquidacióndeNómina
	definir nombre_operador Como Caracter
	definir horas_ejecutadas,tarifa,horas_extra,horas_regulares como real
	definir subtotalA,deduccion,salario_bruto,salario_neto Como real
	definir salud, pension,fondos_solid como real
	tarifa<-35000
	Escribir "sistema de nómina"
	Escribir "ingrese el nombre del operador"
	leer nombre_operador
	Escribir "ingrese las horas ejecutadas"
	leer horas_ejecutadas
	si horas_ejecutadas>160 entonces
		horas_extras<-horas_ejecutadas-160
		horas_regulares<-160
	sino 
		horas_extras<-0
		horas_regulares<-horas_ejecutadas
	FinSi
	salario_bruto<- (horas_regulares * tarifa) + (horas_extras * tarifa * 1.35)
	subtotalA<-salario_bruto
	si subtotalA<1500000 Entonces
		salud<-subtotalA * 0.04
		pension<-0
		fondos_solid<-0
	SiNo
		si subtotalA>=1500000 y subtotalA<3000000 Entonces
			salud<-subtotalA * 0.06
			pension<-subtotalA * 0.02
			fondos_solid<-0
		sino 
			si  subtotalA>=3000000
				salud<-subtotalA * 0.08
				pension<-subtotalA * 0.04
				fondos_solid<-subtotalA * 0.01
				
			FinSi
		FinSi
		deduccion<-salud+pension+fondos_solid
		salario_bruto<-subtotalA-deduccion
		
		
	FinSi
	Escribir "desprendible de pago ( Comand Line Interface)"  , nombre_operador
	Escribir "subtotal salario: ",subtotalA
	Escribir "Total de retenciones tributarias: ",deduccion
	Escribir "salario neto validado: ",salario_bruto
	
	
finAlgoritmo


![Código PSEINT] ![alt text](<Capturas/captura ejercicio4(seccion b)     .png>)
![Código PSEINT] ![alt text](<Capturas/captura ejercicio4(seccion b)    .png>)
![Resultado código] ![alt text](<Capturas/captura ejercicio4(seccion b)   .png>)