def adicionar_tarefa(tarefas, nome_tarefa):

  # tarefa: nome da tarefa
  # finalizada: indicar se essa tarefa ja foi finalizada ou nao
  tarefa = {"tarefa": nome_tarefa, "finalizada": False}
  tarefas.append(tarefa)
  print(f"Tarefa {nome_tarefa} adicionada com sucesso!")
  return

def visualizar_tarefas(tarefas):
  print("\nLista de tarefas:")
  for indice, tarefa in enumerate(tarefas, start=1):
    status = "✓" if tarefa["finalizada"] else " "
    nome_tarefa = tarefa["tarefa"]
    print(f"{indice}. [{status}] {nome_tarefa}")

def atualizar_tarefa(tarefas, indice_tarefa, novo_nome_tarefa):
  indice_tarefa_ajustado = int(indice_tarefa) - 1
  # len = quantidade de tarefas 
  if indice_tarefa_ajustado >= 0 and indice_tarefa_ajustado < len(tarefas):
    tarefas[indice_tarefa_ajustado]["tarefa"] = novo_nome_tarefa
    print(f"Tarefa {indice_tarefa} atualizada para {novo_nome_tarefa}.")
  else:
    print("Índice de tarefas inválido.")
  return

def completar_tarefa(tarefas, indice_tarefa):
  indice_tarefa_ajustado = int(indice_tarefa) - 1
  tarefas[indice_tarefa_ajustado]["finalizada"] = True
  print(f"Tarefa {indice_tarefa} marcada como finalizada.")
  return

def deletar_tarefas_finalizadas(tarefas):
  for tarefa in tarefas:
    if tarefa["finalizada"]:
      tarefas.remove(tarefa)
  print("Tarefas finalizadas foram deletadas.")

  return

tarefas = []
while True:
  print("\nMenu do Gerenciador de Lista de tarefas:")
  print("1. Adicionar Tarefa")
  print("2. Ver Tarefas")
  print("3. Atualizar Tarefa")
  print("4. Completar Tarefa")
  print("5. Deletar Tarefas Finalizadas")
  print("6. Sair")

  escolha = input("Digite sua escolha: ")

  if escolha == "1":
    nome_tarefa = input("Digite a tarefa que deseja adicionar: ")
    adicionar_tarefa(tarefas, nome_tarefa)
  elif escolha == "2":
    visualizar_tarefas(tarefas)
  elif escolha == "3":
    visualizar_tarefas(tarefas)
    indice_tarefa = input("Digite o número da tarefa que deseja atualizar: ")
    novo_nome = input("Digite o novo nome da tarefa: ")
    atualizar_tarefa(tarefas, indice_tarefa, novo_nome)
  elif escolha == "4":
    visualizar_tarefas(tarefas)
    indice_tarefa = input("Digite o número da tarefa realizada: ")
    completar_tarefa(tarefas, indice_tarefa)
  elif escolha == "5":
    deletar_tarefas_finalizadas(tarefas)
    visualizar_tarefas(tarefas)
  elif escolha == "6":
    print("Programa finalizado.")
    break
