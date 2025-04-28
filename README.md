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

## 💻 Código Principal
```python
import random

distancia_segura = 5  # distância inicial segura

distancia_asteroide = random.randint(1, 10)

while distancia_asteroide < distancia_segura:
    print(f"Distância do asteroide: {distancia_asteroide}")
    if distancia_asteroide < 3:
        print("PERIGO! Asteroide muito próximo! Encerrando simulação.")
        break
    if distancia_asteroide < distancia_segura / 2:
        print("Aproximando-se de asteroide!")
    distancia_segura += 2
    print(f"Distância segura agora é {distancia_segura}
")
    distancia_asteroide = random.randint(1, 10)
else:
    print("Navegação concluída com segurança!")
```

---

## 🤝 Contribuição
Contribuições são bem-vindas! Sinta-se à vontade para abrir *issues* ou enviar *pull requests*.

---

## 📄 Licença
Este projeto está licenciado sob a [MIT License](LICENSE).

