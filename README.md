# Imobiliária Nova Portugal

Site institucional da Imobiliária Nova Portugal.

## O que está neste repositório

- `index.html`: site estático, responsivo, com catálogo e fotos incorporadas no próprio HTML.
- As fotos dos quatro imóveis estão incorporadas no arquivo para que não dependam de uma pasta externa.

## Publicação na Vercel

1. Acesse https://vercel.com/ e entre com sua conta.
2. Escolha **Add New → Project**.
3. Importe o repositório `alvaromarca46-ui/imobiliaria-nova-portugal`.
4. Como é um site HTML estático, selecione **Other** (ou deixe a detecção automática sem framework).
5. Deixe Build Command e Output Directory vazios, se a Vercel permitir.
6. Clique em **Deploy**.

O arquivo `index.html` fica na raiz do repositório, então a Vercel o utiliza como página inicial.

## Dados institucionais

- Responsável: Joel Alves — CRECI 306196
- Endereço: Avenida Rodolfo Pirani, 805 — Jardim Rodolfo Pirani, São Paulo — SP
- WhatsApp: https://wa.me/5511950692911
- E-mail: novaportugalimobiliaria@gmail.com
- Instagram: https://www.instagram.com/novaportugal_.imobiliaria/

## Importante: Supabase e painel administrativo

A página atual é uma versão estática. Ela não está conectada ao Supabase e não possui painel administrativo funcional neste repositório.

O projeto Supabase que precisa ser conectado tem tabelas chamadas `properties`, `property_images` e `admins`. Os arquivos administrativos encontrados em versões anteriores usam uma estrutura diferente (`imoveis` e bucket `imoveis-fotos`). Não foram copiados para evitar consultas e alterações incompatíveis com o banco existente.

Antes de criar ou alterar tabelas, políticas RLS, autenticação ou Storage, é necessário confirmar o Project Ref e inspecionar as colunas e políticas reais do projeto correto. Nenhuma chave secreta deve ser colocada no código do navegador.

## Próximas etapas

1. Confirmar o Project Ref do Supabase correto.
2. Conferir as estruturas de `properties`, `property_images` e `admins`, além das políticas RLS e buckets.
3. Adaptar o site e construir o painel administrativo para esse esquema.
4. Configurar as URLs de autenticação depois que a Vercel fornecer o domínio de implantação.
5. Testar cadastro, edição, publicação, upload de fotos e permissões.
