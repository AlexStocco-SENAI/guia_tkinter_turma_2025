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
```