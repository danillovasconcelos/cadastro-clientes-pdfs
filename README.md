# Exemplo Cadastro Clientes · Empresas + PDFs (MVP Supabase)

Sistema simples (apenas `index.html`) para:
- Autenticação (Supabase Auth)
- Seleção/Criação de **empresa** (multiempresa)
- Cadastro de **clientes** por empresa
- **Upload de PDFs** por cliente (Storage Supabase, caminho `company_id/cliente_id/...`)
- **RLS** e políticas garantindo segregação por empresa

## 1) Preparar o Supabase
1. Crie um projeto no Supabase.
2. Em **Storage**, crie o bucket **`pdfs`** (privado).
3. Em **SQL Editor**, cole o bloco SQL que está dentro do `index.html` (há um `<details>` com todo o script).

## 2) Executar
Abra o `index.html` no navegador e:
1. Cole `SUPABASE_URL` e `ANON KEY`.
2. Faça **Sign up / Login**.
3. Crie ou selecione uma **Empresa**.
4. Cadastre **Clientes** e faça **Upload** de PDFs.

## 3) Deploy Grátis (Netlify)
1. Crie um repositório no GitHub e envie este `index.html`.
2. Acesse https://app.netlify.com/start → **Import from Git** → selecione seu repo.
3. **Build command**: (deixe em branco)
4. **Publish directory**: `./`
5. Clique **Deploy site** → você ganhará um domínio `https://seusite.netlify.app`.

---

> **Atenção**: Este MVP não remove o arquivo do Storage ao excluir o registro. Para produção, implemente deleção no Storage e auditoria (quem apagou, quando, etc.).
