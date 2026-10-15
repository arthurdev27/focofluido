# FOCO FLUIDO

Site estático (sem build). Arquivos:
- `index.html`: página de vendas
- `membros.html`: área de membros (Essencial e Completo)

## Publicar (GitHub + Vercel)
1. Crie um repositório no GitHub e envie os arquivos desta pasta.
2. Na Vercel: Add New > Project > importe o repositório > Framework "Other" > Deploy.

## Configurar
- Preços e links de checkout: objeto `CONFIG` no topo do script do `index.html`.
- Link do plano Completo (upgrade): objeto `CONFIG` do `membros.html`.
- Respostas do FAQ sobre acesso, pagamento e reembolso, e links de Privacidade e Contato (`CONFIG.faq` e `CONFIG.links`).

## Liberar acesso após o pagamento (no painel do checkout)
- Essencial: `https://SEU-SITE.vercel.app/membros.html`
- Completo: `https://SEU-SITE.vercel.app/membros.html?plano=completo`

Atenção: esse esquema não impede o compartilhamento de links. Para proteção real, use login ou
link único gerado por webhook de pagamento aprovado (função no servidor), com chaves em variáveis de ambiente.
Nunca coloque chaves secretas no HTML.
