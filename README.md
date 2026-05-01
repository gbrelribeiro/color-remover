<h1 align="center">
  Removedor de Cor
</h1>

## ⬇️ Download

| Versão | Download |
|---|---|
| v1.0.0 (Windows) | [**color_remove.exe**](https://github.com/gbrelribeiro/color-remover/releases/tag/v1.0.0) |

> Não precisa ter Python instalado — só baixar e executar.

Aplicação desktop com interface gráfica que remove uma cor específica de imagens, tornando os pixels correspondentes transparentes e salvando o resultado em PNG.

## Descrição

O **Removedor de Cor** é uma ferramenta visual construída com Python e Tkinter que permite selecionar uma cor por código HEX (ou clicando diretamente na imagem) e apagá-la com controle de tolerância. Os pixels que correspondem à cor escolhida ficam completamente transparentes no arquivo final.

**Funcionalidades:**

- Interface gráfica escura e moderna
- Seleção de imagem via explorador de arquivos
- Entrada de cor em formato HEX com prévia em tempo real
- Captura de cor clicando diretamente sobre a imagem
- Controle de tolerância de 0 a 120
- Preview lado a lado (original × resultado) com fundo xadrez para transparência
- Processamento em thread separada (sem travar a UI)
- Exportação em PNG com canal alpha preservado

**Formatos de imagem suportados:** PNG, JPG, JPEG, BMP, WEBP, TIFF

## Pré-requisitos

- Python 3.10+
- Bibliotecas:

```bash
pip install Pillow numpy
```

> `tkinter` já vem incluído na instalação padrão do Python.

## Como usar

### 1. Execute o script

```bash
python color_remove.py
```

### 2. Selecione uma imagem

Clique em **Procurar arquivo…** e escolha a imagem desejada. O preview original aparecerá à direita.

### 3. Defina a cor a remover

Digite o código HEX no campo (ex: `FF0000` para vermelho) — a prévia de cor atualiza em tempo real.

Ou clique em **Capturar da imagem** para abrir a janela de captura e clicar diretamente sobre o pixel desejado.

### 4. Ajuste a tolerância

Use o slider para controlar a sensibilidade da remoção:

| Valor | Comportamento |
|---|---|
| `0` | Remove apenas pixels exatamente iguais à cor |
| `30` | Padrão — remove tons próximos |
| `120` | Remove uma faixa ampla de cores similares |

### 5. Processe e salve

Clique em **Remover Cor**. Após o processamento, o resultado aparecerá no preview e o botão **Salvar PNG** ficará ativo.

O arquivo é salvo com o nome `<original>_sem_<HEX>.png` no local que desejar.
