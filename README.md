# Deploy no Render

Este site é automaticamente publicado no **Render** a cada push na branch `main`.

**Passo 1: Criar conta no Render**
1. Acesse https://render.com (crie uma conta gratuita)
2. Clique em **"New → Web Service"**

**Passo 2: Conectar repositório GitHub**
1. Escolha **"Build and deploy from a Git repository"**
2. Conecte sua conta GitHub e selecione o repositório `site-malucao`
3. Preencha os campos:
   - **Name:** `site-malucao`
   - **Environment:** `Static Site`
   - **Publish directory:** `.` (ponto, para servir raiz)
   - **Build Command:** deixe vazio (ou `echo "Build complete"`)

**Passo 3: Configurar domínio customizado (opcional)**
1. No dashboard do Render, vá em **Settings → Domain**
2. Clique em **"Add Custom Domain"**
3. Adicione: `malucaopromos.com`
4. O Render fornecerá registros **CNAME** para apontar no seu registrador de domínios

**Passo 4: Deploy automático**
- Após conectar, todo push na branch `main` dispara deployment automático ✅
- Site fica online em: `https://site-malucao.onrender.com`

**Deploy manual (se necessário):**
```powershell
$env:PATH = "C:\Program Files\Git\bin;$env:PATH"
git push origin main
```

Render = Simples, gratuito e sem configuração de FTP! 🚀
