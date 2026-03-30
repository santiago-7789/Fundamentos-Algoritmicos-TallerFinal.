resultado_logico <- No(var_A O var_B) Y (var_C Y No(var_B))
solución
 No(var_A O var_B) Y (var_C Y No(var_B))
1. se sustituye: no(verdadero o falso) y (verdadero y no (falso))
2. se resuelve el parentesis izquierdo aplicando el o(or): no(verdadero)  y (verdadero y no (falso))
3. se aplica el no(not): falso y (verdadero y verdadero)
4. se resuelve el parentesis derecho: falso y verdadero
5. se aplica y(and): falso

Código PSEINT

Algoritmo ejercicio2_booleano 
	
		
		var_A <- Verdadero;
		var_B <- Falso;
		var_C <- Verdadero;
		
		
		resultado_logico <- No(var_A O var_B) Y (var_C Y No(var_B));
		
		
		
		Escribir "Ejercicio 2 - Álgebra Booleana";
		
		Escribir "var_A = ", var_A;
		Escribir "var_B = ", var_B;
		Escribir "var_C = ", var_C;
		
		Escribir "Expresión: No(var_A O var_B) Y (var_C Y No(var_B))";
		Escribir "Paso 1: (verdadero o Falso) = verdadero";
		Escribir "Paso 2: No(verdadero) = Falso";
		Escribir "Paso 3: No(Falso) = verdadero";
		Escribir "Paso 4: ( verdadero y verdadero) = verdadero";
		Escribir "Paso 5: falso y verdadero = Falso";
		
		Escribir "resultado_logico = ", resultado_logico;

FinAlgoritmo

![código PSEINT] ![alt text](<Capturas/captura ejercicio2 .png>)
![resultado]     ![alt text](<Capturas/captura ejercicio2.png>)