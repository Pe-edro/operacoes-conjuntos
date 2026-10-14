# 🧮 Trabalho Prático: Matemática para Computação

Repositório acadêmico oficial desenvolvido para a disciplina de **Matemática para Computação** do curso de **Tecnologia em Desenvolvimento de Software Multiplataforma (DSM)** da **Faculdade de Tecnologia de Osasco - Prefeito Hirant Sanazar (FATEC Osasco)**.

---

## 👥 Integrantes e Divisão de Camadas

O projeto foi estruturado em três camadas modulares distintas, combinando implementações nativas e manuais de estruturas discretas, teoria dos números e uma aplicação prática em sistemas de recomendação.

| Camada / Módulo | Arquivos | Responsável | Descrição Detalhada |
| :--- | :--- | :--- | :--- |
| **Camada 1** | `conjuntos.py` | **Fabiano Barbir** | Implementação manual e algorítmica de operações da teoria dos conjuntos utilizando laços e condicionais (sem recorrer a classes prontas como `set`), realizando validações automáticas contra os métodos nativos da linguagem Python. |
| **Camada 2** | `conjunto_numericos.py` | **Pedro Senhor Monte** | Módulo avançado de Teoria dos Números contendo um classificador numérico completo ($\mathbb{N}, \mathbb{Z}, \mathbb{Q}, \mathbb{I}, \mathbb{R}$), gerador de divisores otimizado por raiz quadrada e o Crivo de Eratóstenes para busca de números primos. |
| **Camada 3** | `SistemaRecomendacaoPuro.java`<br>`Main.java` | **Rafael Magno da Sena** | Sistema de recomendação interativo desenvolvido em Java puramente estruturado, aplicando conceitos de conjuntos, cardinalidade e o cálculo do **Índice de Jaccard** para mensurar a afinidade de interesses entre os usuários. |

---

## 📂 Detalhes Técnicos dos Módulos

### 1. Operações com Conjuntos (`conjuntos.py`)
Implementa do zero as seguintes operações discretas fundamentais:
* **Pertinência ($x \in A$)**: Varredura sequencial para verificar a existência de um elemento.
* **União ($A \cup B$)**: Combinação de elementos sem repetição.
* **Interseção ($A \cap B$)**: Identificação de elementos comuns estritos.
* **Diferença ($A - B$ e $B - A$)**: Filtro de elementos presentes apenas no conjunto de origem.
* **Diferença Simétrica ($A \triangle B$)**: União das diferenças assimétricas.
* **Inclusão/Subconjunto ($A \subseteq B$ e $A \supseteq B$)**: Validação de subconjuntos.
* **Cardinalidade ($\|A\|$)**: Contagem de elementos únicos.
* **Complemento ($\complement_U A$)**: Subtração de $A$ em relação ao universo $U$.

### 2. Classificador Numérico e Teoria dos Números (`conjunto_numericos.py`)
Fornece um menu interativo completo capaz de:
* **Classificar Números**: Identifica e valida inteiros, frações (com simplificação automática via Máximo Divisor Comum - MDC pelo Algoritmo de Euclides), decimais exatos e dízimas periódicas simples/compostas (com conversão algorítmica para fração geratriz), além de tratar raízes quadradas exatas e irracionais.
* **Listar Divisores**: Algoritmo de alta eficiência baseado na raiz quadrada do número alvo.
* **Crivo de Eratóstenes**: Determinação em lote de números primos até um limite $n$.

### 3. Sistema de Recomendação por Teoria dos Conjuntos (`SistemaRecomendacaoPuro.java` & `Main.java`)
Desenvolvido em Java sem bibliotecas de coleção avançadas para demonstrar a manipulação de arrays e lógica pura:
* Modela perfis de usuários (Ana, Bia, Caio) e suas preferências como conjuntos de dados.
* Calcula interseções e uniões para extrair o **Índice de Jaccard** $J(A, B) = \frac{\|A \cap B\|}{\|A \cup B\|}$.
* Apresenta um relatório tabular no terminal indicando o grau de afinidade e recomendando o perfil mais compatível.

---

## 🛠️ Guia de Instalação dos Pré-requisitos

Para executar os códigos contidos neste repositório, certifique-se de possuir o **Python** e o **Java Development Kit (JDK)** instalados em seu ambiente.

### Passo A: Instalando o Python
1. Acesse o site oficial: [python.org](https://www.python.org/)
2. Baixe o instalador mais recente do Python 3.
3. *Importante (Windows):* Marque a opção **"Add Python to PATH"** na primeira tela do instalador.
4. Valide a instalação no terminal:
   ```bash
   python --version
   ```

### Passo B: Instalando o Java Development Kit (JDK)
1. Baixe uma distribuição atual do JDK (como *Eclipse Temurin OpenJDK* ou *Oracle JDK* versão 11 ou superior).
2. Execute o instalador seguindo as etapas padrão.
3. Configure as variáveis de ambiente do sistema operacional, adicionando o diretório `bin` da sua instalação do Java à variável `PATH`.
4. Valide a instalação abrindo um novo terminal:
   ```bash
   java -version
   javac -version
   ```

---

## 🚀 Como Clonar e Executar o Projeto

1. Clone o repositório em sua máquina local utilizando o Git:
   ```bash
   git clone https://github.com/SEU-USUARIO/SEU-REPOSITORIO.git
   cd SEU-REPOSITORIO
   ```

### Executando os Módulos em Python (Camadas 1 e 2)
Para interagir com as operações de conjuntos desenvolvidas por Fabiano:
```bash
python conjuntos.py
```

Para interagir com o classificador numérico e teoria dos números desenvolvido por Pedro:
```bash
python conjunto_numericos.py
```

### Compilando e Executando o Módulo em Java (Camada 3)
Para compilar e executar o sistema de recomendação desenvolvido por Rafael:
1. Navegue até o diretório dos arquivos `.java`.
2. Compile os códigos-fonte para gerar os bytecodes:
   ```bash
   javac SistemaRecomendacaoPuro.java Main.java
   ```
3. Execute a aplicação principal:
   ```bash
   java Main
   ```

---

## 📄 Licença
Trabalho acadêmico desenvolvido para fins educacionais na FATEC Osasco. Uso livre para consulta e estudos.