class Veiculo:
    def _init_(self, modelo, ano, marca):
        self.marca = marca
        self.modelo = modelo
        self.ano = ano
        self.ligado = False

    def ligar(self):
        self.ligado = True
        print(f"{self.modelo} está ligado")

    def desligar(self):
        self.ligado = False
        print(f"{self.modelo} está desligado")

    def exibir_info(self):
        print(f"Veículo: {self.marca} {self.modelo} ({self.ano})")

class Carro(Veiculo):
    def _init_(self, nome, modelo, ano, portas):
        super()._init_(nome, modelo, ano)
        self.portas = portas

    def exibir_info(self):
        super().exibir_info()
        print(f"Tipo: Carro com {self.portas} portas")

    def buzinar(self):
        print("Buzinando")

meu_carro = Carro("Toyota", "Corolla", 2022, 4)
meu_carro.exibir_info()
meu_carro.ligar()
meu_carro.buzinar()
meu_carro.desligar()
