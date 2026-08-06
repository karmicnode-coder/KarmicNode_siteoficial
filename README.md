# Karmic Node — Publicação na Vercel

Pacote pronto a publicar. Este é um site estático puro (HTML + CSS + JavaScript) — sem servidor, sem base de dados, sem build. É por isso que a Vercel é perfeita para este caso: publicação em segundos, HTTPS automático, gratuito.

---

## 🚀 Como publicar (5 minutos)

### 1. Criar conta gratuita na Vercel

Aceda a **[vercel.com](https://vercel.com)** e clique em "Sign Up". Recomendo criar conta com o **GitHub** ou com o **email `karmicnode@gmail.com`** — a escolha influencia o método de deploy no passo seguinte.

### 2. Publicar (escolha um dos dois métodos)

#### Opção A · Deploy por arrastar (mais fácil, sem GitHub)

1. No painel da Vercel, clique em **"Add New..."** → **"Project"**.
2. Escolha **"Deploy without Git"** (opção que aparece em baixo, se disponível). Se não aparecer, siga a Opção B.
3. Arraste toda a pasta `deploy_vercel/` para a área de upload.
4. Clique em **"Deploy"**.
5. Em ~30 segundos o site fica online num URL provisório do tipo `karmic-node.vercel.app`.

#### Opção B · Deploy via GitHub (recomendado a longo prazo)

Esta opção é ligeiramente mais trabalhosa mas **desbloqueia atualizações automáticas** — sempre que fizer uma alteração ao código, o site atualiza-se sozinho.

1. Crie um repositório no GitHub (privado): [github.com/new](https://github.com/new). Nome sugerido: `karmicnode-website`.
2. Faça upload dos ficheiros desta pasta para o repositório (pode arrastar diretamente no site do GitHub).
3. Na Vercel: **"Add New..."** → **"Project"** → **"Import Git Repository"** → escolha o repositório.
4. Nas definições de deploy, deixe **tudo por defeito** (não é preciso build command nem output directory — a Vercel deteta que é um site estático).
5. Clique em **"Deploy"**.

### 3. Ligar o domínio próprio (quando o tiverem)

1. Compre `karmicnode.pt` em [dns.pt](https://www.dns.pt) (~10€/ano) ou noutro registrador.
2. No painel da Vercel do projeto → **Settings** → **Domains** → **Add**.
3. Escreva `karmicnode.pt` e siga as instruções que aparecem — a Vercel diz-lhe exatamente que registos DNS deve criar no painel do seu registrador.
4. Em algumas horas (normalmente 15 minutos) o domínio fica ativo com HTTPS automático incluído.

---

## 🔄 Como fazer alterações depois de publicado

Continue a trabalhar aqui, no espaço onde criámos o site. Cada vez que quiser atualizar o site online:

### Se usou Opção A (deploy manual)
1. Peça-me para preparar uma nova versão do pacote.
2. Descarregue-o.
3. Na Vercel, entre no projeto → **Deployments** → **"Redeploy"** (ou volte a arrastar a pasta como fez da primeira vez).

### Se usou Opção B (GitHub)
1. Peça-me para preparar as alterações.
2. Faça upload dos ficheiros atualizados para o mesmo repositório GitHub.
3. **A Vercel deteta automaticamente e publica em segundos** — não precisa de fazer mais nada.

Esta é a grande vantagem da Opção B: cada alteração aqui = publicação automática lá.

---

## 📦 Estrutura da pasta

```
deploy_vercel/
├── index.html              ← página principal (todo o site num único ficheiro)
├── vercel.json             ← configuração da Vercel (cache, security headers)
├── README.md               ← este ficheiro
└── assets/
    ├── css/karmic.css      ← estilos
    ├── js/karmic.js        ← lógica principal
    ├── js/i18n.js          ← traduções PT/EN
    ├── logo-karmic-node-hd.jpg
    └── img/                ← 12 imagens (hero, serviços, portfólio, fundadores)
```

---

## ✅ Checklist antes de publicar

- [x] Formulário de contacto ligado ao Formspree → `karmicnode@gmail.com`
- [x] Botão "Loja" ligado a `karmicnode.com`
- [x] Foto e nomes reais dos fundadores (Rafael Dias · Rodrigo Romana)
- [x] Contactos oficiais (email, morada Cartaxo, horário)
- [x] Páginas legais RGPD (Privacidade, Termos, Cookies)
- [x] Cookie banner conforme RGPD
- [x] Multilingue PT/EN
- [x] Modo dark/light
- [ ] Preencher dados legais em `#privacidade` e `#termos` (marcados a dourado no site)
- [ ] Ligar redes sociais quando existirem
- [ ] (Opcional) Adicionar Google Analytics 4 quando quiserem tracking de visitas

---

## 🆘 Suporte

Se algum passo do deploy der problema, tire uma screenshot e envie por aqui — resolvemos em conjunto.
