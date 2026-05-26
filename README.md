# Sistema-de-Control-de-Horas-Laborales-en-Python
Proyecto en Python que registra las horas trabajadas por un equipo durante la semana. El programa calcula el total de horas semanales por recurso y clasifica la jornada como “Horario Estándar” o “Sobretiempo” usando matrices, funciones, ciclos y condicionales.
## Maryerly_Ceron
## Ingeniería de sistemas
# Matriz con los recursos y horas trabajadas de lunes a viernes
recursos = [
    ["Carlos", 8, 9, 8, 10, 9],
    ["Ana", 7, 8, 7, 8, 7],
    ["Luis", 9, 10, 9, 8, 10],
    ["María", 6, 7, 8, 7, 6]
]

# Función para calcular total de horas y clasificación
def calcular_horas(recurso):
    nombre = recurso[0]
    horas = recurso[1:]
    
    total = sum(horas)
    
    if total > 40:
        clasificacion = "Sobretiempo"
    else:
        clasificacion = "Horario Estándar"
    
    return nombre, total, clasificacion

# Recorrer la matriz e imprimir resultados
for recurso in recursos:
    nombre, total, clasificacion = calcular_horas(recurso)
    
    print("Recurso:", nombre)
    print("Total de horas:", total)
    print("Clasificación:", clasificacion)
    print("---------------------------")
