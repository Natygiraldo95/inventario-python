# ------------------------------------------------------------
# Programa: Auditoría de Inventario
# Autor: Natalia Giraldo Romero
# Curso: Fundamentos de Programación - UNAD
# Fase 5 - Evaluación Final POA
# ------------------------------------------------------------

# Función para calcular la cantidad a pedir
def calcular_pedido(stock_actual, stock_minimo):
    if stock_actual < stock_minimo:
        return stock_minimo - stock_actual
    else:
        return 0

# Matriz de artículos [Código, Nombre, Stock Actual, Stock Mínimo]
inventario = [
    ["A01", "Teclado", 3, 5],
    ["A02", "Mouse", 10, 8],
    ["A03", "Monitor", 2, 4],
    ["A04", "Cable HDMI", 6, 6],
    ["A05", "Impresora", 1, 3]
]

# Encabezado del informe
print("=== Auditoría de Inventario ===")
print("Artículo\tStock Actual\tStock Mínimo\tPedido")

# Procesamiento de la matriz
for articulo in inventario:
    codigo, nombre, stock_actual, stock_minimo = articulo
    pedido = calcular_pedido(stock_actual, stock_minimo)
    print(f"{nombre}\t{stock_actual}\t\t{stock_minimo}\t\t{pedido}")

# Mensaje final
print("\nProceso completado. Lista de pedidos generada correctamente.")
