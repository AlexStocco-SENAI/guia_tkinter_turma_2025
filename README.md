# Guia Rápido de Tkinter para Iniciantes

Bem-vindo! Este é um guia de referência rápida para quem está começando a desenvolver interfaces gráficas (GUI) em Python com a biblioteca Tkinter. O objetivo é fornecer exemplos claros e diretos para os conceitos e widgets mais utilizados no dia a dia.

## 🚀 Estrutura Básica: Seu Primeiro "Olá, Mundo!"

Toda aplicação em Tkinter segue uma estrutura fundamental. Pense nela como a fundação de uma casa.

1.  **Importar a biblioteca:** Trazer as ferramentas do Tkinter para o nosso código.
2.  **Criar a janela principal:** A tela onde tudo irá acontecer.
3.  **Adicionar "widgets":** Os elementos visuais como textos e botões.
4.  **Iniciar o "loop" da aplicação:** Manter a janela aberta, esperando por interações do usuário.

```python
# 1. Importar a biblioteca tkinter
import tkinter as tk

# 2. Criar a janela principal
janela = tk.Tk()
janela.title("Minha Primeira Aplicação")

# 3. Adicionar um widget de texto (Label)
label = tk.Label(janela, text="Olá, Mundo!")
label.pack() # "Empacota" o widget na janela para que ele apareça

# 4. Iniciar o loop da aplicação
janela.mainloop()

## 🧩 Widgets Essenciais: As Peças do Quebra-Cabeça

Widgets são os componentes visuais da sua interface. Vamos conhecer os mais importantes.

### Label: Exibindo Textos
O `Label` é usado para mostrar informações estáticas, como títulos e mensagens.

- **Propósito:** Exibir um texto ou uma imagem.
- **Comando:** `tk.Label(container, text="Seu texto aqui")`

```python
import tkinter as tk

janela = tk.Tk()
janela.title("Exemplo de Label")

label_titulo = tk.Label(janela, text="Bem-vindo ao nosso sistema!", font=("Arial", 16))
label_titulo.pack(pady=10) # pady adiciona um espaço vertical

label_aviso = tk.Label(janela, text="Preencha os campos abaixo.")
label_aviso.pack()

janela.mainloop()
```

### Button: Ações e Interatividade
O `Button` permite que o usuário dispare uma ação ao clicar.

- **Propósito:** Executar uma função quando clicado.
- **Comando:** `tk.Button(container, text="Texto do Botão", command=nome_da_funcao)`

```python
import tkinter as tk

def acao_do_botao():
  print("O botão foi clicado!")

janela = tk.Tk()
janela.title("Exemplo de Botão")

botao = tk.Button(janela, text="Clique em Mim!", command=acao_do_botao)
botao.pack(pady=20, padx=20)

janela.mainloop()

### Entry: Coletando Informações
O `Entry` é um campo para o usuário digitar uma única linha de texto.

- **Propósito:** Permitir a entrada de texto.
- **Comando:** `tk.Entry(container)`
- **Obter valor:** Use o método `.get()` para capturar o texto digitado.

```python
import tkinter as tk

def mostrar_nome():
  nome_digitado = campo_nome.get()
  label_resultado.config(text=f"Olá, {nome_digitado}!")

janela = tk.Tk()
janela.title("Exemplo de Entry")

label_nome = tk.Label(janela, text="Digite seu nome:")
label_nome.pack()

campo_nome = tk.Entry(janela)
campo_nome.pack()

botao_enviar = tk.Button(janela, text="Enviar", command=mostrar_nome)
botao_enviar.pack(pady=5)

label_resultado = tk.Label(janela, text="")
label_resultado.pack()

janela.mainloop()

