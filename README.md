# 🧠 MLP aplicada ao Problema Lógico XOR

Este projeto consiste na implementação e experimentação de uma **Rede Neural Multicamadas (MLP)** para resolver o clássico **problema lógico XOR**, utilizando a linguagem **Python** e a biblioteca **NumPy**.

## 🎯 Objetivo

Aplicar uma MLP simples para o problema não-linearmente separável **XOR**, testando diferentes combinações de **hiperparâmetros** (número de neurônios na camada oculta, taxa de aprendizado e número de épocas), com o objetivo de observar o comportamento da rede quanto à **convergência e acurácia**.

---

## 🔍 Problema XOR

O XOR (OU exclusivo) é uma função lógica que retorna `1` apenas quando as entradas são diferentes:

| Entrada A | Entrada B | XOR |
|-----------|-----------|-----|
|     0     |     0     |  0  |
|     0     |     1     |  1  |
|     1     |     0     |  1  |
|     1     |     1     |  0  |

Este problema **não pode ser resolvido por um perceptron simples**, exigindo uma arquitetura mais complexa — uma MLP com pelo menos uma camada oculta.

---

## ⚙️ Arquitetura da Rede Neural

- Rede Neural Multicamadas (MLP)
- Uma camada oculta
- Função de ativação: **Sigmoid**
- Treinamento via **backpropagation**
- Erro: **Mean Squared Error (MSE)**

---

## 🔬 Experimentos Realizados

Foram executadas 5 combinações de hiperparâmetros, variando:

- 🧮 **Número de neurônios na camada oculta**: 2, 4, 6
- 🚀 **Taxa de aprendizado**: 0.01, 0.1, 0.5
- 🕰️ **Número de épocas**: 1000, 5000, 10000

### 📋 Tabela de Configurações:

| Execução | Neurônios | Learning Rate | Épocas |
|----------|-----------|----------------|--------|
| 1        | 2         | 0.1            | 1000   |
| 2        | 4         | 0.01           | 5000   |
| 3        | 6         | 0.5            | 10000  |
| 4        | 4         | 0.1            | 10000  |
| 5        | 2         | 0.5            | 5000   |

---

## 📊 Resultados

Cada execução foi registrada com os erros ao longo das épocas e as saídas previstas pela rede. Gráficos de erro por época foram gerados para facilitar a análise.

### 📈 Gráficos (Erro por Época)

Os gráficos estão disponíveis no diretório `img/` e foram gerados com o [matplotlib](https://matplotlib.org/). Também foram exportados em `.csv` na pasta `files/` para uso no [Canva](https://www.canva.com/):

#### 📂 `files/` (dados em CSV para Canva)
- `execucao1.csv`  
- `execucao2.csv`  
- `execucao3.csv`  
- `execucao4.csv`  
- `execucao5.csv`  

#### 🖼️ `img/` (gráficos salvos em PNG)
- `execucao1.png`  
- `execucao2.png`  
- `execucao3.png`  
- `execucao4.png`  
- `execucao5.png`  

---

## 📺 Apresentação em Vídeo

📌 Assista à explicação completa da metodologia, experimentos e análise dos resultados:

🔗 [Clique aqui para assistir no YouTube](https://youtu.be/0SeB9W8n5cI)

---

## 💻 Como executar

1. Certifique-se de ter o **Python 3.8+** e **NumPy** instalado:
   ```bash
   pip install numpy
   ```

2. Execute o script:
   ```bash
   python mlp_xor.py
   ```

3. O console exibirá os resultados de cada experimento e as previsões da rede.

---

## 🧾 Estrutura do Projeto

```
├── mlp_simples.py            # Código principal da MLP
├── README.md
├── results/
│   ├── resultados.txt        # Saída resumida das execuções
│   ├── files/                # Dados em CSV para gráficos
│   │   ├── execucao1.csv
│   │   ├── ...
│   └── img/                  # Gráficos de erro por época (PNG)
│       ├── execucao1.png
│       ├── ...
```

---

## ✅ Conclusões

- A rede neural foi capaz de aprender o problema XOR nas execuções com **parâmetros bem ajustados**.
- A **melhor performance** foi observada na execução 3 (6 neurônios, LR=0.5, 10000 épocas).
- **Taxas muito baixas** ou **quantidade insuficiente de neurônios** dificultaram o aprendizado.

---

## 📚 Créditos

Este projeto foi desenvolvido como parte da avaliação prática da disciplina **Inteligência Artificial** (UNITINS), orientada pelo professor Marco Antônio.

Autor: Lucas Daniel Rodrigues dos Santos 
Curso: Sistemas de Informação – 6º Período  