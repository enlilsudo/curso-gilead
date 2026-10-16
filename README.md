# Curso Gilead — Escola Virtual 

## Conteúdo
- `index.html`: site responsivo em HTML, CSS e JavaScript, sem dependências externas.
- Catálogo pesquisável e filtrável com 12 áreas de estudo.
- Área do aluno demonstrativa, progresso guardado no navegador e conteúdo gratuito/membros identificado.
- Calculadora de Guematria hebraica (mispar hechrechi padrão).
- Links iniciais para Google Drive e Telegram.
- Identidade: `CURSO GILEAD / בית מדרש גלעד` e `Torah • Qabbalah • Linguagem • Tradição • Sabedoria`.

## Testar localmente
Abra `index.html` num navegador moderno. Para um teste via servidor local, dentro desta pasta execute:
```bash
python -m http.server 8000
```
Acesse `http://localhost:8000`.

## Publicar no domínio próprio
1. Registre um domínio no registrador escolhido.
2. Escolha uma hospedagem estática com HTTPS (por exemplo, um serviço de hospedagem estática ou hospedagem web tradicional).
3. Envie `index.html` como arquivo de entrada da raiz do site.
4. Configure os registros DNS informados pela hospedagem e habilite HTTPS.
5. Substitua o link provisório `https://t.me/` pelo canal/grupo oficial do Curso Gilead.
6. Confirme se a pasta do Drive deve ser pública ou acessível apenas a membros.

## Importante: o que ainda não é produção
Esta versão é um protótipo front-end. O modo de entrada é apenas uma demonstração local, não autentica pessoas, não valida pagamentos e não protege conteúdo privado. O progresso fica no `localStorage` do navegador e não sincroniza entre dispositivos. Não use esta versão para guardar dados sensíveis nem para vender acesso ainda.

## Arquitetura recomendada para a versão real
- Front-end: pode evoluir para React/Next.js ou continuar como HTML para um lançamento simples.
- Autenticação: serviço seguro com e-mail, recuperação de senha e controle de sessão.
- Banco de dados: perfis, matrículas, cursos, aulas, progresso e permissões.
- Pagamentos: provedor compatível com o Brasil, usando checkout hospedado e webhooks verificados no servidor.
- Controle de acesso: o servidor deve conferir a matrícula antes de entregar aulas e arquivos exclusivos. Ocultar um botão no navegador não protege conteúdo.
- Materiais: links privados ou URLs temporárias assinadas; evitar links públicos para arquivos pagos.
- Telegram: bot `Madrich Gilead`, com token somente no servidor, para boas-vindas, direcionamento de alunos e comunicação.
- LGPD: política de privacidade, termos de uso, minimização de dados, consentimento e processo de exclusão.

## Antes do lançamento
- Inserir domínio e contatos oficiais.
- Inserir links oficiais do Telegram e regras da comunidade.
- Revisar conteúdos, fontes e direitos de uso dos materiais.
- Definir planos, preços, política de cancelamento e acesso pós-cancelamento.
- Implantar autenticação, banco de dados, pagamentos e controle de acesso antes de oferecer cursos pagos.
