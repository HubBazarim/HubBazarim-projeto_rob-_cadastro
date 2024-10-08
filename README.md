## Robô de Cadastro com Python e PyAutoGUI

Este projeto foi desenvolvido durante um **Intensivão de Python da Hashtag**, onde aprendi a utilizar a biblioteca **PyAutoGUI** para automação de tarefas no computador. A ferramenta permite simular ações como **escrever textos**, **pressionar teclas**, **clicar** e realizar **combinações de teclas**. No projeto, automatizamos o cadastro de produtos em um sistema online.

### Passo a Passo do Projeto:

**PASSO 1: ENTRAR NO SISTEMA DA EMPRESA**

Na aula, foi ensinado a abrir o **Windows Explorer** e, em seguida, o **Google Chrome**. No entanto, achei mais eficiente abrir o **navegador padrão diretamente**, independente de qual seja, utilizando a função `subprocess.run()` para isso. Outra alternativa seria o uso da biblioteca `webbrowser`, que também pode abrir um link no navegador padrão:

```python ``import webbrowser``
**PASSO 2: FAZER LOGIN NO SISTEMA**

Utilizei o **PyAutoGUI** para simular o preenchimento dos campos de **e-mail** e **senha** no formulário de login e, em seguida, clicar no botão de login.

**PASSO 3: IMPORTAR A BASE DE PRODUTOS**

A base de produtos a ser cadastrada foi carregada a partir de um arquivo **CSV** usando a biblioteca **Pandas**. Isso permite a manipulação dos dados de forma eficiente.

**PASSO 4: CADASTRO AUTOMÁTICO DE PRODUTOS**

O robô percorre cada linha da tabela de produtos e preenche os campos correspondentes no sistema, como **código**, **marca**, **tipo**, **categoria**, **preço unitário**, **custo** e observações. Após o preenchimento, ele envia o formulário e repete o processo até o final da lista.

**PASSO 5: REPETIÇÃO DO PROCESSO ATÉ O FIM DA LISTA**

O robô é programado para rolar a página para cima após cada envio, preparando a tela para o próximo cadastro.

### OBSERVAÇÕES IMPORTANTES:

- **Posições de "clicks" do mouse**: As coordenadas usadas para clicar nos campos da tela podem variar conforme a resolução do monitor e a interface do sistema. Caso necessário, é importante ajustar os valores de **x** e **y** nas funções `pyautogui.click()`.
- **Parar o programa**: Caso o robô precise ser interrompido durante a execução, basta mover o mouse para o canto superior esquerdo da tela, uma função de segurança embutida no **PyAutoGUI** chamada `FAILSAFE`.

### FERRAMENTAS UTILIZADAS:

- **PyAutoGUI**: Para automação das interações com a interface gráfica do sistema.
- **Pandas**: Para manipulação e leitura dos dados do CSV.

Essa aula foi fundamental para meu aprendizado no uso do **PyAutoGUI**, que se mostrou uma ferramenta muito interessante para automação de tarefas repetitivas.

