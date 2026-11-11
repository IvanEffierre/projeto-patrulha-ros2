# Projeto de Patrulhamento Autônomo com ROS 2

## Sobre o projeto

Sistema de patrulhamento autônomo desenvolvido com ROS 2, Gazebo, Python e inteligência artificial.

O objetivo é controlar um robô móvel para executar uma trajetória quadrada, identificar indicações de obstáculos e registrar informações de odometria.

## Tecnologias utilizadas

- Ubuntu 24.04
- ROS 2 Jazzy
- Gazebo Harmonic
- Python 3
- Jupyter Notebook
- NumPy, Pandas e Matplotlib
- PyTorch
- Git e GitHub

## Funcionalidades

- Comunicação entre nós ROS 2.
- Controle de velocidade por parâmetros.
- Execução de trajetória quadrada.
- Painel interativo com Jupyter.
- Treinamento e inferência da rede neural ObstacleNet.
- Integração da rede neural com ROS 2.
- Máquina de estados para controle da patrulha.
- Simulação do robô no Gazebo.
- Gravação e análise de odometria com ROS Bag.

## Máquina de estados

O nó de patrulhamento utiliza quatro estados:

- `MOVING_FORWARD`: movimentação em linha reta.
- `TURNING`: execução de curvas.
- `AVOIDING`: parada diante de indicação de obstáculo.
- `DONE`: conclusão da patrulha.

## Inteligência artificial

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
