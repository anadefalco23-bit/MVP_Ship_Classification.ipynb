# Ship Classification using Deep Learning and Transfer Learning

Projeto desenvolvido como MVP da disciplina de Machine Learning & Analytics, com o objetivo de aplicar técnicas de Visão Computacional e Deep Learning para classificação automática de embarcações a partir de imagens.

---

## Objetivo

Desenvolver e avaliar modelos de Deep Learning capazes de identificar automaticamente diferentes categorias de embarcações com base em suas características visuais, contribuindo para aplicações de monitoramento marítimo, consciência situacional, vigilância costeira e automação de processos de classificação de alvos.

---

## Problema

A identificação manual de embarcações em grandes volumes de imagens é uma tarefa trabalhosa, sujeita a erros e pouco escalável. O uso de técnicas de Inteligência Artificial permite automatizar esse processo por meio da extração de padrões visuais diretamente das imagens.

Neste projeto foi desenvolvido um sistema de classificação multiclasse capaz de reconhecer diferentes tipos de embarcações utilizando Redes Neurais Convolucionais (CNNs) e modelos pré-treinados baseados em Transfer Learning.

---

## Dataset

**Maritime Vessel Classification Dataset**

Fonte:

https://www.kaggle.com/datasets/arpitjain007/game-of-deep-learning-ship-datasets

### Características do conjunto de dados

- 6.252 imagens de embarcações;
- 5 categorias distintas;
- Imagens RGB;
- Classificação multiclasse supervisionada;
- Redimensionamento para 224 × 224 pixels.

---

## Metodologia

O projeto seguiu as principais etapas de um pipeline de Machine Learning:

1. Análise exploratória dos dados (EDA);
2. Verificação da integridade das imagens;
3. Pré-processamento e normalização;
4. Divisão estratificada em treino, validação e teste;
5. Treinamento de modelos candidatos;
6. Avaliação comparativa;
7. Otimização de hiperparâmetros;
8. Avaliação final em conjunto de teste.

---

## Modelos Avaliados

### CNN Baseline

Rede Neural Convolucional construída do zero para servir como referência inicial de desempenho.

### MobileNetV2

Modelo pré-treinado utilizando Transfer Learning baseado no dataset ImageNet.

### ResNet50

Arquitetura profunda baseada em conexões residuais, também utilizando pesos pré-treinados do ImageNet.

---

## Otimização

Foram realizados experimentos envolvendo:

- ajuste da taxa de aprendizado (*learning rate*);
- Data Augmentation;
- Fine Tuning parcial da MobileNetV2.

Os resultados mostraram que a configuração original da MobileNetV2 permaneceu como a melhor solução para o conjunto de dados estudado.

---

## Resultados

### Melhor modelo: MobileNetV2

| Métrica | Resultado |
|----------|-----------:|
| Accuracy (Validação) | 86,67% |
| Accuracy (Teste) | 86,25% |
| F1-Score Macro | 0,874 |
| Precision Macro | 0,88 |
| Recall Macro | 0,87 |

### Comparação entre modelos

| Modelo | Accuracy de Validação |
|----------|---------------------:|
| CNN Baseline | 71,1% |
| MobileNetV2 | 86,7% |
| ResNet50 | 34,0% |

---

## Principais Conclusões

- O Transfer Learning apresentou desempenho significativamente superior ao treinamento de uma CNN do zero;
- A MobileNetV2 demonstrou excelente capacidade de generalização;
- A diferença entre validação e teste foi inferior a 1%, indicando baixa ocorrência de overfitting;
- Data Augmentation e Fine Tuning não produziram ganhos relevantes para o conjunto de dados utilizado;
- Arquiteturas mais complexas nem sempre resultam em melhor desempenho quando comparadas experimentalmente.

---

## Tecnologias Utilizadas

- Python
- TensorFlow
- Keras
- Scikit-Learn
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Pillow
- Google Colab

---

## Reprodutibilidade

O projeto foi desenvolvido em ambiente Google Colab com aceleração por GPU.

Para reproduzir os experimentos é necessário:

1. Baixar o dataset original;
2. Configurar as dependências do notebook;
3. Executar as células na ordem apresentada.

---

## Estrutura do Repositório

```text
.
├── README.md
├── Visual_MVP_ML_Analytics_20261.ipynb
└── resultados/
```

---

## Autora

**Ana Paula Santiago de Falco**

Doutora em Ciência e Tecnologia de Polímeros (UFRJ)

Pesquisadora nas áreas de Inteligência Artificial, Machine Learning, Defesa, Biossegurança e Tecnologias Estratégicas.

---

## Licença

Projeto desenvolvido exclusivamente para fins acadêmicos e educacionais.
