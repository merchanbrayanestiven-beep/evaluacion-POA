ef evaluar_compromiso(duración, clics):
    if duración >180 and clics > 8:
        return "Alto"
    elif duración < 60 or clics < 3:
        return "Bajo"
    else:
        return "Medio"
    
sesiones = [
     [101,200,12],
    [102,120,5],
    [103,45,2],
    [104,300,4],
    [105,190,15],
]
    
print("---INFORME DE COMPROMISO DE SESIONES ---")
print(f"{'ID Cliente':<12} | {'Clasificación':<15}")
print("-"*30)
    
for sesion in sesiones:
    id_cliente = sesion[0]
    duración = sesion[1]
    clics = sesion[2]
        
    clasificación = evaluar_compromiso (duración, clics)   
    print(f"ID{id_cliente:<9} | {clasificación:<15}")
