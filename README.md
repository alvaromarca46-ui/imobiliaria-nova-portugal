# Imobiliária Nova Portugal

Site institucional da Imobiliária Nova Portugal.

## Arquivos

- `index.html`: site público responsivo, com catálogo dinâmico conectado ao Supabase e fotos incorporadas como imagens de apoio para os quatro anúncios iniciais.
- `admin.html`: painel administrativo para login, cadastro, edição, exclusão e upload de fotos dos imóveis.

## Catálogo público e Supabase

O catálogo público consulta a tabela `public.imoveis` e atualiza os imóveis em destaque, filtros, contagem e páginas individuais. Se a consulta ao Supabase falhar, a página mantém os quatro anúncios iniciais como fallback.

Os quatro imóveis iniciais foram inseridos na tabela existente. Para esses registros, o site mantém as fotos que já estavam incorporadas no HTML; fotos enviadas pelo painel são exibidas a partir do bucket `imoveis-fotos`.

O site usa apenas a chave pública (publishable) do Supabase. Nenhuma chave `service_role` está no navegador.

## Painel administrativo

Após a publicação, acesse `/admin.html`.

- E-mail autorizado: `novaportugalimobiliaria@gmail.com`
- O usuário já existe no Supabase Auth. Use a senha definida para essa conta.
- O painel utiliza `public.imoveis` e o bucket `imoveis-fotos`.
- As políticas RLS e Storage restringem alterações e uploads ao e-mail administrativo autorizado.

## Banco Supabase

Projeto: `wjrrpuvfpufmdtqxblcj`

Tabela `public.imoveis`:
`id`, `titulo`, `descricao`, `preco`, `tipo`, `endereco`, `quartos`, `banheiros`, `vagas`, `fotos`, `created_at`.

Bucket de imagens: `imoveis-fotos` (público para exibição; operações de escrita restritas ao administrador).

## Dados institucionais

- Responsável: Joel Alves — CRECI 306196
- Endereço: Avenida Rodolfo Pirani, 805 — Jardim Rodolfo Pirani, São Paulo — SP
- WhatsApp: https://wa.me/5511950692911
- E-mail: novaportugalimobiliaria@gmail.com
- Instagram: https://www.instagram.com/novaportugal_.imobiliaria/

## Publicação

Repositório conectado à Vercel: `alvaromarca46-ui/imobiliaria-nova-portugal`, branch `main`. A Vercel cria implantações automaticamente a cada commit.
