tarefas = []

def menu():
    print("\n1 - Adicionar tarefa")
    print("2 - Listar tarefas")
    print("3 - Remover tarefa")
    print("4 - Sair")

while True:
    menu()
    opcao = input("Escolha: ")

    if opcao == "1":
        tarefa = input("Digite a tarefa: ")
        tarefas.append(tarefa)

    elif opcao == "2":
        if len(tarefas) == 0:
            print("Nenhuma tarefa cadastrada")
        else:
            for i, t in enumerate(tarefas):
                print(f"{i} - {t}")

    elif opcao == "3":
        index = int(input("Digite o número da tarefa: "))
        if index < len(tarefas):
            tarefas.pop(index)
        else:
            print("Tarefa inválida")

    elif opcao == "4":
        break
