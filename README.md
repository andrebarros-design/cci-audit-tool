# CCI Audit Tool

Uma ferramenta mobile-first simples e eficiente para auditoria de **Higiene das Mãos** e **Uso de Luvas** em contexto clínico.

## Funcionalidades

*   **Design Responsivo**: Otimizado para dispositivos móveis, funcionando como uma app nativa.
*   **Dois Modos de Auditoria**:
    *   👋 **Higiene das Mãos**: Registo de indicações e ações (fricção, lavagem, etc.).
    *   🧤 **Uso de Luvas**: Checklist detalhada de critérios de seleção, uso e remoção.
*   **Fluxo de Trabalho Simplificado**:
    *   Seleção rápida de categoria profissional (Enfermeiro, Médico, Assist. Oper.).
    *   Validação imediata de dados.
    *   Relatórios de sessão instantâneos.
*   **Persistência Local**: Histórico de auditorias salvo no navegador (LocalStorage).
*   **Exportação**: Impressão de relatórios ou guardar como PDF.

## Como Usar

1.  Abra o ficheiro `index.html` em qualquer navegador moderno.
2.  Selecione o tipo de auditoria e a categoria profissional.
3.  Preencha a auditoria (clique nos itens para selecionar/responder).
4.  Clique em "Salvar e Fechar Sessão" para gerar o relatório.

## Tecnologias

*   **HTML5 / JavaScript (Vanilla)**: Sem dependências de build complexas, apenas um ficheiro.
*   **Tailwind CSS**: Estilo moderno via CDN.
*   **Phosphor Icons / Heroicons**: Ícones SVG inline.

## Instalação / Desenvolvimento

Não é necessária instalação. Basta clonar o repositório e abrir o `index.html`.

```bash
git clone https://github.com/andrebarros-design/cci-audit-tool.git
cd cci-audit-tool
# Abra index.html no seu browser
```
