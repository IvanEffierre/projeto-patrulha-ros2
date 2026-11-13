# Projeto de Patrulhamento Autônomo com ROS 2

## 🎯 Objetivo  

Sistema de patrulhamento autônomo desenvolvido com ROS 2, Gazebo, Python e inteligência artificial.

O objetivo é controlar um robô móvel para executar uma trajetória quadrada, identificar indicações de obstáculos e registrar informações de odometria. Foram confeccionados 02 (dois) notebooks: ESP004_NB04_Atividade_Avaliativa.ipynb e Valdivan_Notebook.ipynb. 

O notebook "Valdivan_Notebook.ipynb" contém os testes e métricas da atividade e as evidências aplicadas na atividade e carrega o ambiente do Gazebo Sim.
Já  o notebook "SP004_NB04_Atividade_Avaliativa.ipynb" contém os dados da rúbrica pedida pelo professor da disciplina.

## 🧪  Tecnologias utilizadas

- Ubuntu 24.04
- ROS 2 Jazzy
- Gazebo Harmonic
- Python 3
- Jupyter Notebook
- NumPy, Pandas e Matplotlib
- PyTorch
- Git e GitHub

## 🧪  Funcionalidades

- Comunicação entre nós ROS 2.
- Controle de velocidade por parâmetros.
- Execução de trajetória quadrada.
- Painel interativo com Jupyter.
- Treinamento e inferência da rede neural ObstacleNet.
- Integração da rede neural com ROS 2.
- Máquina de estados para controle da patrulha.
- Simulação do robô no Gazebo.
- Gravação e análise de odometria com ROS Bag.

## 🧪  Máquina de estados

O nó de patrulhamento utiliza quatro estados:

- `MOVING_FORWARD`: movimentação em linha reta.
- `TURNING`: execução de curvas.
- `AVOIDING`: parada diante de indicação de obstáculo.
- `DONE`: conclusão da patrulha.

## 🧪  Inteligência artificial

A ObstacleNet foi desenvolvida com PyTorch. O modelo utiliza dados de velocidade, distância e velocidade angular para estimar a probabilidade de presença de obstáculos.

O treinamento local com dados sintéticos obteve 84% de acurácia na validação.

A distância utilizada nos testes foi fornecida por mensagens ROS 2 simuladas, não por um sensor físico do veículo.

## Resultados da odometria

| Métrica | Resultado |
|---|---:|
| Registros | 620 |
| Duração | 619,01 segundos |
| Distância acumulada | 8,07 metros |
| Deslocamento final | 0,448 metros |
| Velocidade linear máxima | 0,30 m/s |
| Velocidade média em movimento | 0,223 m/s |
| Velocidade angular máxima | 0,785 rad/s |

## Estrutura do projeto

```text
ros2_ws/
├── .gitignore
├── README.md
├── Untitled.ipynb
├── src/
│   └── patrol_node/
├── models/
└── patrol_odom_movimento/

```

## 🧩 Perfil e Propósito Profissional

### 🎓 Autor  
**Valdivan F. Ramos** – 📌Analista de Sistemas Multidisciplinar | Mestrando em Eng. de Sistemas e Produtos | Docência/Pesquisa/Gestão | Eng. de Requisitos/CC | Ciência de Dados/Big Data | Dir. Digital/Compliance/LGPD | Redes/IoT/IIoT. Atuação com foco em análise de dados aplicada à educação, desenvolvimento técnico-científico e construção de ferramentas interativas que orientam a tomada de decisão.


### 📚 Educação com Propósito  
> “Ensinar linguagens de programação é mais do que ensinar algoritmos e códigos.  
> É educar mentes capazes de resolver problemas complexos da realidade, unindo teoria e prática, sem desprezar os valores humanos.  
> Mas educação e valores só fazem sentido quando estão a serviço da sociedade.”  
> — Valdivan F. Ramos

---

### 📄 Referência para Currículo Lattes  
**Título:** Projeto de Patrulhamento Autônomo com ROS 2.  
**Tipo de produção técnica:** Desenvolvimento de Software / Robótica Terrestre 
**Ano:** 2026  
**Descrição:** Esta atividade faz parte das atividades acadêmicas desenvolvidas no âmbito do curso de Mestrado Profissional em Engenharia de Sistemas e Produtos - PPGESP/IFBA, tendo sido proposta e solicitada pelo professor responsável pela disciplina como parte do processo de aprendizagem e avaliação. O trabalho tem como objetivo aplicar, na prática, os conhecimentos teóricos e técnicos abordados ao longo da disciplina "Sistemas Autonomos Robóticos", proporcionando a oportunidade de desenvolver, implementar e avaliar uma solução utilizando os conceitos e ferramentas estudados.
**Disponível em:** [https://github.com/IvanEffierre/projeto-patrulha-ros2](https://github.com/IvanEffierre/projeto-patrulha-ros2)
