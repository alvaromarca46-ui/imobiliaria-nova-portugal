# Imobiliária Nova Portugal

Site institucional da Imobiliária Nova Portugal.

## Arquivos

- `index.html`: site público estático, responsivo, com catálogo e fotos incorporadas.
- `admin.html`: painel administrativo conectado ao Supabase para login, cadastro, edição, exclusão e upload de fotos dos imóveis.

## Painel administrativo

Após a publicação na Vercel, acesse `/admin.html`.

- Login autorizado: `novaportugalimobiliaria@gmail.com`
- O usuário já existe no Supabase Auth. A senha não é armazenada neste repositório; entre com a senha configurada no Supabase.
- O painel utiliza a tabela `public.imoveis` e o bucket `imoveis-fotos`.
- O painel usa apenas a chave pública (publishable) do Supabase. Não contém chave `service_role`.
- O acesso administrativo é validado no cliente e reforçado por políticas RLS no banco e no Storage.

## Banco Supabase

Projeto: `wjrrpuvfpufmdtqxblcj`

Tabela `public.imoveis`:
`id`, `titulo`, `descricao`, `preco`, `tipo`, `endereco`, `quartos`, `banheiros`, `vagas`, `fotos`, `created_at`.

Bucket de imagens: `imoveis-fotos` (público para exibição das fotos). Upload, atualização e exclusão via Storage são permitidos apenas para o e-mail administrativo autorizado.

## Limitação atual

O catálogo da página inicial `index.html` ainda é estático e não consulta automaticamente a tabela `imoveis`. O painel grava no Supabase, mas a sincronização automática do catálogo público com o banco ainda precisa ser implementada e testada.

## Dados institucionais

- Responsável: Joel Alves — CRECI 306196
- Endereço: Avenida Rodolfo Pirani, 805 — Jardim Rodolfo Pirani, São Paulo — SP
- WhatsApp: https://wa.me/5511950692911
- E-mail: novaportugalimobiliaria@gmail.com
- Instagram: https://www.instagram.com/novaportugal_.imobiliaria/

## Publicação

A Vercel está conectada ao repositório `alvaromarca46-ui/imobiliaria-nova-portugal`. Cada commit na branch `main` pode iniciar uma nova implantação. Para um site HTML estático, não é necessário comando de build.
