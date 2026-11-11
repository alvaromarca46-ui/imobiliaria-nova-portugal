# Integração Supabase — concluída

A integração inicial da Imobiliária Nova Portugal foi configurada no projeto Supabase `wjrrpuvfpufmdtqxblcj`.

- Catálogo público conectado à tabela `public.imoveis`.
- Os quatro imóveis iniciais foram inseridos no banco.
- Painel administrativo em `/admin.html`.
- Bucket de fotos: `imoveis-fotos`.
- Políticas RLS e Storage limitam operações administrativas ao e-mail `novaportugalimobiliaria@gmail.com`.
- O navegador utiliza somente a chave pública/publishable; a chave `service_role` não está no código.

Para conferir o esquema, consulte o README. O catálogo mantém os anúncios incorporados como fallback se o Supabase estiver indisponível.
