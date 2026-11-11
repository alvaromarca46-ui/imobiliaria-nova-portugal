# Painel administrativo — configuração pendente

O painel não foi incluído nesta versão porque os arquivos administrativos disponíveis usam uma tabela `imoveis` e um bucket `imoveis-fotos`, enquanto o projeto informado para a Nova Portugal contém `properties`, `property_images` e `admins`.

Adaptar o painel sem conhecer as colunas, chaves estrangeiras, políticas RLS e bucket corretos poderia causar falhas ou alterações indevidas.

Para concluir o painel:
- confirmar o Project Ref do Supabase;
- inspecionar as três tabelas e suas colunas;
- verificar políticas RLS e permissões do Storage;
- implementar autenticação e autorização administrativa;
- testar operações com uma conta de administrador autorizada.

Não colocar a chave `service_role` no navegador. Usar somente a chave pública/publishable com RLS corretamente configurado.
