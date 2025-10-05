# Álcool ou Gasolina - App Android ⛽

Um aplicativo Android simples e prático para ajudar motoristas a decidir qual combustível é mais vantajoso na hora de abastecer. Com base nos preços atuais do álcool e da gasolina, o app calcula e informa a opção mais econômica.

## 📸 Screenshot

<img width="366" height="786" alt="image" src="https://github.com/user-attachments/assets/b10c7133-6e31-40f8-ae5a-a52600b1983f" />


---

## ✨ Funcionalidades

* **Interface Intuitiva:** Uma única tela para entrada de dados e visualização do resultado.
* **Entrada de Preços:** Campos para o usuário digitar o preço por litro do álcool e da gasolina.
* **Cálculo Instantâneo:** Um botão "Calcular" que processa os valores e exibe o resultado imediatamente.
* **Recomendação Clara:** O resultado informa de forma direta qual combustível é a melhor escolha.

---

## 📐 A Lógica do Cálculo

A decisão é baseada na regra comumente aceita de que o rendimento de um motor a álcool é, em média, **70%** do rendimento de um motor a gasolina.

Portanto, o cálculo realizado pelo app é:

$$
\frac{\text{Preço do Álcool}}{\text{Preço da Gasolina}}
$$

* Se o resultado for **menor ou igual a 0.7**, é mais vantajoso abastecer com **Álcool**.
* Caso contrário, a **Gasolina** é a melhor opção.

---

## ⚙️ Estrutura do Código (Inferida)

O aplicativo é construído com uma única `MainActivity.kt`, que gerencia toda a lógica:

1.  **Captura de Dados:** Os valores dos preços são lidos dos componentes `TextInputEditText` (`edit_alcool` e `edit_gasolina`).
2.  **Validação:** Ao clicar no botão `btn_calcular`, uma função de validação (`validarCampos`) verifica se ambos os campos foram preenchidos pelo usuário.
3.  **Cálculo:** Se os campos forem válidos, uma função de cálculo (`calcularMelhorPreco`) executa a divisão dos preços.
4.  **Exibição do Resultado:** Com base no resultado da divisão, o `TextView` `text_resultado` é atualizado com a recomendação: "Melhor utilizar Álcool" ou "Melhor utilizar Gasolina".

---

## 🛠️ Tecnologias Utilizadas

* **Linguagem:** Kotlin
* **IDE:** Android Studio
* **Layout:** XML com `ConstraintLayout`
* **Componentes Visuais:** `Material Components` (como `TextInputLayout`)

---

## 🚀 Como Executar o Projeto

1.  **Clone o repositório:**
    ```bash
    git clone <URL_DO_SEU_REPOSITORIO>
    ```

2.  **Abra no Android Studio:**
    * Abra o Android Studio.
    * Selecione "Open an existing Project".
    * Navegue até o diretório onde você clonou o projeto e selecione-o.

3.  **Sincronize e Execute:**
    * Aguarde o Gradle sincronizar as dependências do projeto.
    * Clique no botão "Run 'app'" (ícone de play verde) para instalar e executar o aplicativo em um emulador ou dispositivo Android conectado.
