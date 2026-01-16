# Classificação de Espécies de Pássaros do Cerrado com Deep Learning

Projeto desenvolvido no contexto da disciplina **Tópicos Especiais em Matemática Aplicada (Deep Learning)** da **FCTE/UnB**, com o objetivo de comparar diferentes abordagens de Deep Learning para a classificação de espécies de aves do Cerrado brasileiro.

---

##  Informações Gerais

- **Instituição:** Faculdade de Ciências e Tecnologias em Engenharia – FCTE/UnB  
- **Disciplina:** Tópicos Especiais em Matemática Aplicada (Deep Learning)  
- **Professor:** Vinicius Rispoli  

###  Alunos
- **Felipe Junior Duarte da Silva** – 231012192  
- **Rafael Welz Schadt** – 231011800  
- **Othavio Araujo Bolzan** – 231039150  

---

##  Objetivo do Projeto

Desenvolver e avaliar um sistema de **classificação automática de espécies de psitacídeos do Cerrado**, utilizando imagens e técnicas de **Deep Learning**, comparando três abordagens:

1. **CNN construída do zero**
2. **Transfer Learning** com EfficientNetV2-S
3. **Fine-Tuning** da EfficientNetV2-S

O objetivo final é identificar a metodologia com **maior capacidade de generalização**, utilizando métricas robustas e validação externa.

---

##  Metodologias Utilizadas

###  1. CNN do Zero
- Arquitetura customizada (CNNFromScratchV3)
- Batch Normalization, Dropout e Early Stopping
- Treinamento completo apenas com o dataset do projeto

###  2. Transfer Learning
- Modelo base: **EfficientNetV2-S (ImageNet)**
- Backbone congelado
- Treinamento apenas do classificador final

###  3. Fine-Tuning
- EfficientNetV2-S pré-treinada
- Descongelamento dos blocos finais da rede
- Taxas de aprendizado diferenciadas para backbone e head

---

## Dataset

- **Total de imagens:** 2879  
- **Total de classes:** 14 espécies de Psittacidae  
- **Formato:** Pastas organizadas por classe (ImageFolder)  

### Divisão dos Dados
- **Treinamento:** 70%
- **Validação:** 15%
- **Teste:** 15%
- **Validação Externa:** Dataset separado e não visto durante o treino

---

## Tecnologias e Ferramentas

###  Linguagem e Ambiente
- **Python 3**
- **Google Colab** (com suporte a GPU)

###  Principais Bibliotecas
- **Deep Learning:** PyTorch, Torchvision  
- **Manipulação de Dados:** NumPy, Pandas, OS, Pathlib  
- **Visualização:** Matplotlib, Seaborn  
- **Avaliação:** Scikit-learn  
- **Download de Dados:** gdown  

---

##  Instalação das Dependências

Execute o comando abaixo no terminal ou notebook:

```bash
pip install torch torchvision torchaudio seaborn scikit-learn matplotlib pandas numpy gdown
