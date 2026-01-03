# Auditoria CCI (Controlo de Infeção)

Ferramenta de auditoria móvel para registo de práticas de Higiene das Mãos e Uso de Luvas em ambiente hospitalar.

## Funcionalidades
- **Modo Offline/Standalone**: Funciona como um único ficheiro HTML (`index.html`), sem necessidade de servidor.
- **Auditoria Híbrida**: Suporta registo de Higiene das Mãos e Uso de Luvas na mesma sessão.
- **Interface Mobile-First**: Design otimizado para telemóveis com botões grandes e navegação fluida.
- **Relatório Automático**: Gera um resumo da sessão com:
  - Total de observações.
  - Detalhe de cada observação (Indicações vs Ação, Respostas do Checklist de Luvas).
  - Data e Hora formatadas (PT-PT).
- **Sticky Footer**: Botões de ação rápida ("Salvar", "Finalizar") sempre visíveis.
- **Histórico Local**: As sessões são guardadas no `localStorage` do navegador.

## Estrutura do Projeto
- `index.html`: **[Versão Principal]** Aplicação completa em um só ficheiro. Contém todo o HTML, CSS (Tailwind via CDN) e JavaScript. Basta abrir este ficheiro no browser para usar.
- `src/`: Código fonte da versão React (em desenvolvimento/alternativa).

## Como Usar
1. Abra o ficheiro `index.html` no seu navegador (Chrome, Safari, etc.).
2. Selecione o Tipo de Auditoria (Higiene, Luvas ou Ambos).
3. Selecione a Categoria Profissional.
4. Inicie a Sessão.
5. Registe as observações e clique em "Salvar Observação".
6. Ao terminar, clique em "Finalizar Sessão" para ver o relatório.
