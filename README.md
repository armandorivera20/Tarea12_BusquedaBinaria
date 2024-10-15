# Tarea12_BusquedaBinaria
Tarea codigo python de Busqueda Binaria:

    def busqueda_binaria(A, ele):
    if len(A) == 0:
        return -1
    m = len(A) // 2
    if A[m] == ele:
        return m
    elif A[m] > ele:
        return busqueda_binaria(A[:m], ele)
    else:
        resultado = busqueda_binaria(A[m+1:], ele)
        return -1 if resultado == -1 else m + 1 + resultado

#Ejemplo de uso
A = [1, 3, 5, 7, 9, 11]
ele = 7
indice = busqueda_binaria(A, ele)
print(f'El índice de {ele} es {indice}')
