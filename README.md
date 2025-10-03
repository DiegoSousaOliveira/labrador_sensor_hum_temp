# Datalogger

# Labrador Sensor Hum/Temp

Este projeto tem como objetivo o desenvolvimento de um **datalogger multifuncional** utilizando a plataforma **Labrador 32**, capaz de monitorar temperatura e umidade por meio do sensor **AHT10**. Os dados coletados são armazenados em um cartão microSD para posterior análise.

---

## 📌 Funcionalidades

* Leitura de **temperatura (°C)** e **umidade relativa (%)**.
* Registro periódico dos dados em um arquivo `.txt` no cartão **microSD**.
* Estruturação do armazenamento para fácil análise posterior.
* Projeto modular para futura expansão com novos sensores.

---

## 🛠️ Tecnologias e Componentes

* **Plataforma:** Labrador 32
* **Sensor:** AHT10 (temperatura e umidade)
* **Linguagem:** Python
* **Armazenamento:** Cartão microSD

---

## 📂 Estrutura do Projeto

```
labrador_sensor_hum_temp/
├── main.py            # Código principal de leitura e registro
├── lib/               # Bibliotecas auxiliares
├── data/              # Diretório de dados armazenados
└── README.md          # Documentação do projeto
```

---

## ⚙️ Instalação e Uso

1. Clone o repositório:

   ```bash
   git clone https://github.com/DiegoSousaOliveira/labrador_sensor_hum_temp.git
   cd labrador_sensor_hum_temp
   ```

2. Instale as dependências necessárias:

   ```bash
   pip install -r requirements.txt
   ```

3. Conecte o sensor **AHT10** à plataforma **Labrador 32**.

4. Execute o código:

   ```bash
   python main.py
   ```

5. Os dados serão salvos automaticamente no microSD.

---

## 📊 Exemplo de Funcionamento
<img width="605" height="831" alt="Captura de tela 2025-10-02 204156" src="https://github.com/user-attachments/assets/602c026c-ae65-4e30-a97d-a06c3aefa182" />
<img width="822" height="506" alt="Captura de tela 2025-10-02 204712" src="https://github.com/user-attachments/assets/c5843b3e-df74-417a-91d8-8d2e512766b7" />


Arquivo gerado no microSD (exemplo):

```
Data/Hora, Temperatura(°C), Umidade(%)
2025-10-02 14:32, 27.4, 61.2
2025-10-02 14:37, 27.6, 60.9
```

---

## 🚀 Melhorias Futuras

* Suporte para múltiplos sensores.
* Exportação dos dados para formatos `.csv` ou `.json`.
* Interface gráfica para visualização em tempo real.
* Integração com dashboards online.

---


## Instruções

1. Crie um ambiente virtual.

   ```bash
   python3 -m venv .venv
   ```

1. Ative o ambiente virtual.

   ```bash
   source .venv/bin/activate
   ```

1. Instale as dependências.

   ```bash
   pip install -r requirements.txt
   ```

1. Identifique e monte a unidade que deseja utilizar.

   ```bash
   lsblk
   ```

1. Altere os valores das variáveis se necessário.

   ```python
   SD_CARD = "/media/caninos/adata64"
   DATALOGGER = "/data.txt"
   ```

1. Execute o programa.
   Utiliza-se o superusuário para simplificar o uso das permissões.
   No entanto, não é recomendado.

   ```bash
   sudo $PWD/.venv/bin/python main.py
   ```
   
