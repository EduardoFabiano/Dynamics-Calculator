import math

def calcular_segunda_lei():
    print("SEGUNDA LEI DE NEWTON (F = m * a)")
    print("1 - Calcular Força Resultante (F)")
    print("2 - Calcular Massa (m)")
    print("3 - Calcular Aceleração (a)")
    op = input("Escolha: ")
    
    if op == '1':
        m = float(input("Massa (kg): "))
        a = float(input("Aceleração (m/s²): "))
        print(f"\n=> Força Resultante: {m * a:.2f} N")
    elif op == '2':
        f = float(input("Força Resultante (N): "))
        a = float(input("Aceleração (m/s²): "))
        print(f"\n=> Massa: {f / a:.2f} kg" if a != 0 else "\n=> Erro: Aceleração não pode ser zero.")
    elif op == '3':
        f = float(input("Força Resultante (N): "))
        m = float(input("Massa (kg): "))
        print(f"\n=> Aceleração: {f / m:.2f} m/s²" if m != 0 else "\n=> Erro: Massa não pode ser zero.")

def calcular_peso():
    print("FORÇA PESO (P = m * g)")
    m = float(input("Massa do corpo (kg): "))
    g = float(input("Aceleração da gravidade (m/s²) [Padrão da Terra ~ 9.8]: ") or 9.8)
    peso = m * g
    print(f"\n=> Força Peso: {peso:.2f} N")

def calcular_normal():
    print("FORÇA NORMAL (N)")
    print("1 - Superfície Plana Horizontal (Sem forças verticais extras)")
    print("2 - Plano Inclinado")
    op = input("Escolha o cenário: ")
    
    m = float(input("Massa do corpo (kg): "))
    g = float(input("Gravidade (m/s²) [Padrão 9.8]: ") or 9.8)
    
    if op == '1':
        normal = m * g
        print(f"\n=> Força Normal: {normal:.2f} N (Igual ao Peso)")
        return normal
    elif op == '2':
        angulo = float(input("Ângulo de inclinação da rampa (em graus): "))
        angulo_rad = math.radians(angulo)
        normal = m * g * math.cos(angulo_rad)
        print(f"\n=> Força Normal no Plano Inclinado: {normal:.2f} N")
        return normal
    return 0.0

def calcular_atrito():
    print("FORÇA DE ATRITO (Fat = u * N)")
    u = float(input("Coeficiente de atrito (µ): "))
    print("Como deseja informar a Força Normal (N)?")
    print("1 - Digitar o valor da Normal diretamente")
    print("2 - Calcular a Normal dinamicamente (Plana ou Inclinada)")
    op = input("Escolha: ")
    
    if op == '1':
        n = float(input("Valor da Força Normal (N): "))
    else:
        n = calcular_normal()
        
    fat = u * n
    print(f"\n=> Força de Atrito: {fat:.2f} N")

def menu_principal():
    while True:
        print("\nCALCULADORA DE DINÂMICA")
        print("1 - Segunda Lei de Newton")
        print("2 - Força Peso")
        print("3 - Força Normal")
        print("4 - Força de Atrito")
        print("0 - Sair")
        
        opcao = input("\nEscolha uma opção: ")
        
        if opcao == '1':
            calcular_segunda_lei()
        elif opcao == '2':
            calcular_peso()
        elif opcao == '3':
            calcular_normal()
        elif opcao == '4':
            calcular_atrito()
        elif opcao == '0':
            print("\nEncerrando o programa.")
            break
        else:
            print("\nOpção inválida! Tente novamente.")

menu_principal()
