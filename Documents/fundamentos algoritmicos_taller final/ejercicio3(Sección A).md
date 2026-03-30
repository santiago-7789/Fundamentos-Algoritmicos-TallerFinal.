Algoritmo SelectorCandidatos
    Leer estatura_ingresada
    Leer peso_ingresado
    Si estatura_ingresada > 1.70 O peso_ingresado < 80 Entonces
        Escribir "Validación del perfil: Correcta."
    Sino
        Escribir "Validación del perfil: Fallida."

correción de errores
1. Falta FinAlgoritmo - el Algoritmo nunca cierra
2. Falta FinSi - el condicional (si) no cierra
3. No se definieron variables
4. operador o(or) incorrecto - deber ser y(AND) y no o(OR)
5. sin "escribir" antes de "leer" - no hay mensaje que indique datos a ingresar