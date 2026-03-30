Sección c: desarrollo de software - Sistema Case y selectores múltiples

Breve descripción: 
Cajero automático de finanzas cripto con menú interactivo de 4 opciones

Constantes:
BTC: 60,000,00
Variables: 
Saldo disponible: 5000,00

Ciclo de control: 
según (switch)
Ciclo repetitivo hasta finalizar sesión (opción 4)

opciones de segun: 
1. consultar saldo disponible.
2. Retiro con validación de fondos
3. Compra BTC con validación y calculo
4. Cierre de sesión.
5. manejo de errores para opciones inválidas (de otro modo..)


CÓDIGO PSEINT

Algoritmo secciónc_desarrollo_software
    definir saldo_disponible, monto_retiro, monto_inversión, btc_comprados como real
    definir opción como entero
    definir precio_btc Como Real
    
    saldo_disponible <- 5000
    precio_btc <- 60000
    
    Repetir
        Escribir "menú"
        Escribir "1. Consultar estado de cuenta corriente"
        Escribir "2. Retiro estricto de fondos usd"
        Escribir "3. Ejecutar orden de compra de bitcoin (BTC)"
        Escribir "4. Finalizar sesión"
        Escribir "Selecciona una opción"
        leer opcion 
        
        segun opcion hacer 
            1:
                Escribir "saldo disponible: ", saldo_disponible, " USD"
                
            2: 
                Escribir "retirar dinero"
                Escribir "ingrese el monto a retirar"
                leer monto_retiro
                
                si monto_retiro > saldo_disponible entonces 
                    Escribir "EXCEPCIÓN: Flujo de fondos insuficientes en la bóveda actual"
                sino 
                    saldo_disponible <- saldo_disponible - monto_retiro
                    Escribir "Retiro exitoso, saldo restante: ", saldo_disponible
                FinSi
                
            3: 
                Escribir "precio actual de BTC: ", precio_btc, " usd"
                Escribir "ingrese monto usd para invertir"
                leer monto_inversión
                
                si monto_inversión > saldo_disponible Entonces
                    Escribir "Flujo de fondos insuficientes"
                sino 
                    btc_comprados <- monto_inversión / precio_btc
                    saldo_disponible <- saldo_disponible - monto_inversión
                    Escribir "BTC adquiridos: ", btc_comprados
                    Escribir "saldo actual: ", saldo_disponible, " usd"
                FinSi
                
            4: 
                Escribir "cerrando sesión"
                Escribir "Gracias por usar el cajero cripto"
                
            De Otro Modo: 
                Escribir "ERROR, OPCION INVALIDA"
                Escribir "Por favor seleccione una opcion valida (1 - 4)"
        FinSegun
        
    Hasta Que opcion = 4
    
FinAlgoritmo



![Código PSEINT] ![alt text](<Capturas/captura ejercicio5(seccion c)                        .png>)

![Código PSEINT] ![alt text](<Capturas/captura ejercicio5(seccion c)                       .png>)

![Barra de opciones] ![alt text](<Capturas/captura ejercicio5(seccion c)                      .png>)
![opción 1 - Estado de cuenta corriente] ![alt text](<Capturas/captura ejercicio5(seccion c)                     .png>)
![opción 2 - Retirar dinero] ![alt text](<Capturas/captura ejercicio5(seccion c)                    .png>)
[opción 3 - comprar btc (fondos insuficiente )] ![alt text](<Capturas/captura ejercicio5(seccion c)                   .png>)
[opción 3 - comprar btc (fondo suficiente, compra correcta)] ![alt text](<Capturas/captura ejercicio5(seccion c)                  .png>)
[opcion 4 - cerrar sesión] ![alt text](<Capturas/captura ejercicio5(seccion c)                 .png>)
[Error - opción incorrecta]  ![alt text](<Capturas/captura ejercicio5(seccion c)                .png>)