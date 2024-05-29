# **Calculadora Simples**

**Bibliotecas usadas:** 
- flet (*pip install flet*) - Essa biblioteca é a responsável pela criação da interface;
- Decimal(*for decimal import Decimal* isso no código) - Essa é usada para ter acesso aos números decimais do resultado e possibilitar mais configurações na calculadora;
- pyinstaller (*pip install pyinstaller*) -  Essa biblioteca é usada pela *flet* para converter o código em um aplicativo

## configuração da interface:
- **botoes[{  }]** se tratar de um 'dicionario' com todos os botões e suas especificações, para reduzir o tamanho do código;

- **def main(page: ft.page):** É a função que criar a Página/Janela, suas especificações e o que será adicionado a ela;
   - *page.bgcolor = '#000'* definir o fundo da Janela;
   - *page.window_resizable= False* Impedir a alteração do tamanho da Janela; 
   - *page.window_width = 300* definir a comprimento da página;
   - *page.window_height = 420* definir a altura da página;
   - *page.title = 'Calculadora'* título da página;
   - *page.window_always_on_top= True* Mantem a página aberto mesmo quando clicando fora da janela.

- **page.add( )** adicionar elementos a página

- **display= ft.Row()** Criar uma linha para adicionar informações;
   - *width= 250* definir a comprimento da linha;
   - *controls= [result]* o que será exibido na linha;
   - *alignment= 'end'* Aliamento da linha
   - *wrap= True* quebrar de linha quando chegar ao limite da linha.

- **ft.app(target= main)** Exibição da página(nesse caso, como um aplicativo).

## Conversão em aplicativo:
É necessário que a biblioteca pyinstaller esteja instalada.
No terminal:
- **flet pack *nome do arquivo.py*** - compilar o código e o converter em um executável no mesmo diretório do código de origem. *obs:* O executável será de acordo com o sistema operacional usado.
Outra forma que permite adicionar um ícone especifico ao executável é o:
- **flet pack *nome do arquivo.py* --icon "*Caminho da imagem*"**
