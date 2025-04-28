# Atividade na Unidade 3 - Programação de Computadores


## 📄 Descrição
Simulação em Python de navegação segura em um campo de asteroides, utilizando loops `while` para detectar proximidade de perigos, emitir alertas e garantir que a nave alcance espaço livre de forma didática e interativa.

## 📑 Tabela de Conteúdos
- [Descrição](#descrição)
- [Tecnologias](#tecnologias)
- [Pré-requisitos](#pré-requisitos)
- [Como Usar](#como-usar)
- [Link no Google Colab](#link-no-google-colab)
- [Estrutura do Projeto](#estrutura-do-projeto)
- [Código Principal](#código-principal)
- [Contribuição](#contribuição)
- [Licença](#licença)

---

## 📚 Tecnologias
- **Linguagens:** Python 3.x, Markdown
- **Ambiente de Desenvolvimento:** Google Colab

---

## 🐍 Sobre Python e Comandos Utilizados

Breve explicação do Python e dos principais comandos usados neste projeto:

- **Python:** linguagem de programação de alto nível, interpretada e multiplataforma, ideal para automação e prototipagem rápida.
- **`import random`**: módulo para gerar números aleatórios.
- **`random.randint(a, b)`**: retorna um inteiro entre `a` e `b` (inclusive).
- **`import time`**: módulo para funcionalidades de tempo.
- **`time.sleep(segundos)`**: pausa a execução por um número de segundos.
- **`while condição:`** laço que repete o bloco enquanto a condição for verdadeira.
- **`break`**: interrompe o loop imediatamente.
- **`if condição:`** executa código quando a condição for satisfeita.
- **`input(prompt)`**: lê entrada do usuário como string.
- **`int()`**: converte string para inteiro.
- **`print()`**: exibe mensagens na tela.
- **f-strings (`f"texto {var}"`)**: facilita a formatação de strings com variáveis.

## 🔧 Pré-requisitos
- Conta Google para acessar o Google Colab
- Navegador web atualizado

---

## 🚀 Como Usar
1. **Clonar o repositório:**
   ```bash
   git clone https://github.com/seu-usuario/seu-repositorio.git
   cd seu-repositorio
   ```
2. **Abrir no Google Colab:**
   Clique no link abaixo para acessar o notebook pronto para execução.

---

## 🌐 Link no Google Colab
[Abra este notebook no Colab](https://colab.research.google.com/drive/1z5R9ueQ-WTB3sEHl0agXc6_U2OaBM4mE?usp=sharing)

---

## 📂 Estrutura do Projeto
```
├── README.md
├── Atividade2_NavegacaoSegura.md   # Documento com explicação e código comentado
└── notebook_colab.ipynb            # Versão interativa no Google Colab
```

---

## 💻 Código Principal com Interação do Usuário
```python
import random
import time

def navegar_campo_asteroides():
    # Solicita valores iniciais ao usuário
    distancia_segura = int(input("Digite a distância inicial segura (inteiro positivo): "))
    incremento = int(input("Digite o valor de incremento para afastamento (ex: 2): "))
    
    while True:
        distancia_asteroide = random.randint(1, 10)
        print(f"
Distância do asteroide: {distancia_asteroide}")  # quebra de linha para melhor visualização

        # Verifica perigo imediato
        if distancia_asteroide < 3:
            print("PERIGO! Asteroide muito próximo! Encerrando simulação.")
            break

        # Alerta de aproximação
        if distancia_asteroide < distancia_segura / 2:
            print("Aproximando-se de asteroide!")

        # Aumenta distância segura
        distancia_segura += incremento
        print(f"Distância segura agora é {distancia_segura}")

        # Pausa rápida para simular tempo de navegação
        time.sleep(1)
    
    print("
Navegação finalizada.")

# Loop principal para reiniciar a simulação
if __name__ == "__main__":
    while True:
        navegar_campo_asteroides()
        opcao = input("
Deseja reiniciar a simulação? (s/n): ").lower()
        if opcao != 's':
            print("Encerrando o programa. Até a próxima aventura!")
            break
```  

> **Como funciona:**
> 1. O programa pede ao usuário a **distância inicial segura** e o **incremento** para afastamento.
> 2. Em cada iteração, gera uma distância aleatória do asteroide e aplica as lógicas de perigo e alerta.
> 3. Ao final de cada execução, pergunta se o usuário deseja reiniciar a simulação.

---

## 🤝 Contribuição
Contribuições são bem-vindas! Sinta-se à vontade para abrir *issues* ou enviar *pull requests*.

Contribuições são bem-vindas! Sinta-se à vontade para abrir *issues* ou enviar *pull requests*.

---

## 📄 Licença
Este projeto está licenciado sob a [MIT License](LICENSE).
