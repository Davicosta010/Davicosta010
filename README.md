- 👋 Hi, I’m @Davicosta010
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
EXERCICIO NUMERO 1
def cadastrar_pessoa():
    nome = input("Digite o nome da pessoa: ")
    idade = int(input("Digite a idade da pessoa: "))
    cpf = input("Digite o CPF da pessoa: ")
    pessoa = {"nome": nome, "idade": idade, "cpf": cpf}
    return pessoa

def separar_pessoas_menores(pessoas):
    menores = {}
    for cpf, pessoa in pessoas.items():
        if pessoa["idade"] < 18:
            menores[cpf] = pessoa
    return menores

num_pessoas = int(input("Digite o número de pessoas a cadastrar: "))
pessoas = {}
for i in range(num_pessoas):
    print(f"\nCadastro da pessoa {i+1}:")
    pessoa = cadastrar_pessoa()
    cpf = pessoa["cpf"]
    pessoas[cpf] = pessoa

menores = separar_pessoas_menores(pessoas)

print("\nDicionário de todas as pessoas:")
for cpf, pessoa in pessoas.items():
    print(f"CPF: {cpf}, Nome: {pessoa['nome']}, Idade: {pessoa['idade']}")

print("\nDicionário das pessoas menores de 18 anos:")
for cpf, pessoa in menores.items():
    print(f"CPF: {cpf}, Nome: {pessoa['nome']}, Idade: {pessoa['idade']}")

NUMERO 2
dados_principal = {}  # Dicionário principal
dados_backup = {}  # Dicionário de backup

def realizar_backup():
    global dados_principal, dados_backup
    dados_backup.update(dados_principal)
    dados_principal.clear()
    print("Backup realizado com sucesso!")

def inserir_dado(chave, valor):
    global dados_principal
    dados_principal[chave] = valor
    print(f"Dado inserido: {chave} => {valor}")
    
    if len(dados_principal) == 5:
        realizar_backup()

inserir_dado("chave1", "valor1")
inserir_dado("chave2", "valor2")
inserir_dado("chave3", "valor3")
inserir_dado("chave4", "valor4")
inserir_dado("chave5", "valor5")
inserir_dado("chave6", "valor6") 

NUMERO 3
class Automovel:
    def __init__(self, marca, modelo):
        self.marca = marca
        self.modelo = modelo

    def acelerar(self):
        raise NotImplementedError("Método 'acelerar' precisa ser implementado na subclasse.")

    def frear(self):
        raise NotImplementedError("Método 'frear' precisa ser implementado na subclasse.")

class Carro(Automovel):
    def __init__(self, marca, modelo, num_portas):
        super().__init__(marca, modelo)
        self.num_portas = num_portas

    def acelerar(self):
        print("Carro acelerando...")

    def frear(self):
        print("Carro freando...")

class Moto(Automovel):
    def __init__(self, marca, modelo, cilindradas):
        super().__init__(marca, modelo)
        self.cilindradas = cilindradas

    def acelerar(self):
        print("Moto acelerando...")

    def frear(self):
        print("Moto freando...")

class Caminhao(Automovel):
    def __init__(self, marca, modelo, capacidade_carga):
        super().__init__(marca, modelo)
        self.capacidade_carga = capacidade_carga

    def acelerar(self):
        print("Caminhão acelerando...")

    def frear(self):
        print("Caminhão freando...")

class aviao(Automovel):
    def __init__(self, marca, modelo, tipo):
        super().__init__(marca, modelo)
        self.tipo = tipo

    def acelerar(self):
        print("aviao acelerando...")

    def frear(self):
        print("aviao freando...")

exercicio 4 

class Produto:
    def __init__(self, nome, preco):
        self.nome = nome
        self.preco = preco

    def exibir_detalhes(self):
        print(f"Nome: {self.nome}")
        print(f"Preço: R${self.preco:.2f}")

class Camisa(Produto):
    def __init__(self, nome, preco, time, tamanho):
        super().__init__(nome, preco)
        self.time = time
        self.tamanho = tamanho

    def exibir_detalhes(self):
        super().exibir_detalhes()
        print(f"Time: {self.time}")
        print(f"Tamanho: {self.tamanho}")

class Bola(Produto):
    def __init__(self, nome, preco, cor, tamanho):
        super().__init__(nome, preco)
        self.cor = cor
        self.tamanho = tamanho

    def exibir_detalhes(self):
        super().exibir_detalhes()
        print(f"Cor: {self.cor}")
        print(f"Tamanho: {self.tamanho}")

class Chuteira(Produto):
    def __init__(self, nome, preco, marca, tamanho):
        super().__init__(nome, preco)
        self.marca = marca
        self.tamanho = tamanho

    def exibir_detalhes(self):
        super().exibir_detalhes()
        print(f"Marca: {self.marca}")
        print(f"Tamanho: {self.tamanho}")

while True:
    print("Escolha uma opção:")
    print("1. Camisa")
    print("2. Bola")
    print("3. Chuteira")
    print("0. Sair")

    opcao = input("Opção: ")

    if opcao == "0":
        break
    elif opcao == "1":
        nome = input("Digite o nome da camisa: ")
        preco = float(input("Digite o preço da camisa: "))
        time = input("Digite o time da camisa: ")
        tamanho = input("Digite o tamanho da camisa: ")

        camisa = Camisa(nome, preco, time, tamanho)
        camisa.exibir_detalhes()
    elif opcao == "2":
        nome = input("Digite o nome da bola: ")
        preco = float(input("Digite o preço da bola: "))
        cor = input("Digite a cor da bola: ")
        tamanho = input("Digite o tamanho da bola: ")

        bola = Bola(nome, preco, cor, tamanho)
        bola.exibir_detalhes()
    elif opcao == "3":
        nome = input("Digite o nome da chuteira: ")
        preco = float(input("Digite o preço da chuteira: "))
        marca = input("Digite a marca da chuteira: ")
        tamanho = input("Digite o tamanho da chuteira: ")

        chuteira = Chuteira(nome, preco, marca, tamanho)
        chuteira.exibir_detalhes()
    else:
        print("Opção inválida! Por favor, escolha uma opção válida.")



<!---
Davicosta010/Davicosta010 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
