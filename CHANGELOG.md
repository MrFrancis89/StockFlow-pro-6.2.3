# Changelog

Todas as alterações notáveis neste projeto serão documentadas neste arquivo.

O formato é baseado em [Keep a Changelog](https://keepachangelog.com/pt-BR/1.0.0/),
e este projeto adere ao [Versionamento Semântico](https://semver.org/lang/pt-BR/).

## [6.2.0] - 2025-04-08

### Adicionado
- **Nova aba "Adicionar"**: O formulário de adição de produtos foi movido para uma aba separada, ao lado de "Estoque" e "Compras", deixando a interface mais limpa.
- **Ícone ➕** na nova aba para indicar a ação de adicionar.

### Alterado
- **Botão "Ocultar" renomeado para "Apagar"** no formulário de adição, com tooltip "Remover item da lista padrão".
- Versão do projeto atualizada para **v6.2.0**.

### Corrigido
- Garantido que itens fixados com o botão "Fixar" permaneçam na lista após "Novo Dia".
- O botão "Apagar" agora remove permanentemente o item da lista padrão (não apenas o oculta).

---

## [6.1.1] - 2025-04-08

### Corrigido
- **Microfone no duplo toque da lupa**: Agora o microfone é ativado corretamente ao dar duplo toque na lupa. Ajustes no temporizador garantem que o overlay de busca abra antes da ativação do microfone.
- **Lista de compras**: Agora a lista de compras é atualizada imediatamente ao marcar/desmarcar itens, ao adicionar ou remover produtos, e ao editar via swipe.

---

## [6.1.0] - 2025-04-08

### Adicionado
- **Alternância entre calculadora e teclado nativo**: Na calculadora, um botão "⌨️ Usar teclado" permite sair para o teclado do dispositivo e digitar diretamente no campo de quantidade.
- **Ícone de retorno à calculadora**: Quando em modo teclado, um ícone 🧮 aparece dentro do campo; clicando nele, o campo volta a ser readonly e a calculadora reabre.
- **Parser avançado de frações**: Agora é possível digitar frações como `1/2`, `3/4`, `2 1/3` nos campos de quantidade (modo teclado). Ao sair do campo, a fração é convertida automaticamente para decimal (ex: `1/2` → `0,5`), garantindo compatibilidade com os alertas de estoque.

---

## [6.0.0] - 2025-04-08

### Adicionado
- **Navegação por abas**: Interface reorganizada com as abas "Estoque" e "Compras" no menu superior, seguindo o design dos prints.
- **Seções separadas**: O conteúdo foi dividido em duas seções (`#estoque-section` e `#compras-section`), controladas por classes CSS `.tab-content` e `.active`.
- **Estilo do menu de abas**: Botões com ícone e texto, arredondados, e o ativo destacado em vermelho (`var(--btn-danger)`).
- **Sistema de novidades automáticas**: Ao abrir o app após uma atualização, um modal exibe as principais mudanças da nova versão.
- **Versionamento dinâmico**: O título agora mostra "StockFlow Pro" seguido da versão atual (lida da constante `VERSAO_ATUAL`).

### Alterado
- **Nome do projeto**: Restaurado para "StockFlow Pro".

---

## [5.3.1] - 2025-04-08

### Adicionado
- **Dica de swipe na primeira execução**: Um toast informativo é exibido uma única vez após o carregamento da lista, explicando que é possível deslizar os itens para a esquerda para acessar as opções "Apagar" e "Configurar alerta". Essa dica é controlada por uma flag no `localStorage` para não se repetir.
- **Tooltips nos botões da área de adição**:
  - Botão "⭐ Fixar": agora possui o atributo `title="Adicionar item e fixar na lista padrão"`.
  - Botão "🗑️ Apagar" (anteriormente "Padrão"): agora possui `title="Remover item da lista padrão"`.
- **Atributos de acessibilidade (`aria-label`)** nos botões de swipe:
  - Botão "Apagar": `aria-label="Apagar item"`.
  - Botão "Alerta": `aria-label="Configurar alerta"`.

### Alterado
- **Renomeação do botão "Padrão" para "Apagar"** no formulário de adição de itens, com o objetivo de tornar sua função mais clara (remover da lista padrão).

---

## [5.3.0] - 2025-03-15

### Versão inicial com as seguintes funcionalidades principais:
- Lista de estoque categorizada automaticamente.
- Adição de itens com opção de fixar na lista padrão.
- Remoção de itens da lista padrão.
- Swipe em itens para apagar ou configurar alertas de estoque mínimo/máximo.
- Calculadora integrada para entrada de quantidades.
- Reconhecimento de voz para busca e adição de produtos.
- Tema claro/escuro.
- Exportação e importação de listas em JSON.
- Geração de lista de compras baseada em itens marcados.
- Compartilhamento via WhatsApp e cópia para área de transferência.
- Lupa flutuante com funcionalidade de busca e duplo toque para ativar microfone.
