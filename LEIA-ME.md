# Página de venda — Ebook Ice Tube

**URL final:** `https://industrialcursos.com.br/ebook`

## O que está nesta pasta

```
site-ebook/
├── index.html          ← página completa (11 blocos do briefing)
├── style.css           ← estilos (paleta azul + laranja)
├── img/
│   ├── paraty.png      ← foto de Paraty (1º marco)
│   └── maquina-galpao.jpg  ← foto da construção da máquina
├── ebook-referencia/   ← seu .pdf/.docx pode ficar aqui (NÃO vai pro site)
└── LEIA-ME.md          ← este arquivo
```

## Para ver o site localmente AGORA (antes de publicar)

Clica duas vezes em `index.html`. Vai abrir no seu navegador com o visual completo. Assim você valida antes de colocar no ar.

---

## Passo 1 — Subir para GitHub Pages (grátis)

### 1.1 Criar repositório novo
1. Entra em https://github.com/new
2. Nome do repositório: `ebook-industrialcursos` (pode ser outro, mas use esse que combina)
3. Marca como **Public** (GitHub Pages grátis exige público)
4. Clica em **Create repository**

### 1.2 Subir os arquivos
**Jeito mais fácil (sem git, pelo navegador):**
1. Na página do repositório novo, clica em **"uploading an existing file"**
2. Arrasta **TODO O CONTEÚDO** da pasta `site-ebook/` (menos a subpasta `ebook-referencia/`)
   - ✅ `index.html`
   - ✅ `style.css`
   - ✅ pasta `img/` inteira
   - ✅ `LEIA-ME.md` (opcional)
   - ❌ NÃO sobe a pasta `ebook-referencia/` (contém material privado)
3. Clica **Commit changes**

### 1.3 Ativar GitHub Pages
1. No repositório, clica em **Settings** (menu superior)
2. No menu lateral esquerdo, clica em **Pages**
3. Em "Source", escolha **Deploy from a branch**
4. Em "Branch", selecione **main** e pasta **/ (root)**
5. Clica **Save**
6. Aguarde 1-2 minutos. O GitHub vai te dar uma URL tipo:
   `https://seu-usuario.github.io/ebook-industrialcursos/`

**🎉 Neste ponto o site já está no ar** nessa URL do GitHub. O próximo passo é fazer ele responder em `industrialcursos.com.br/ebook`.

---

## Passo 2 — Conectar ao seu domínio industrialcursos.com.br

Como você quer `industrialcursos.com.br/ebook` (caminho `/ebook`, não raiz), **há dois caminhos:**

### CAMINHO A (recomendado, mais simples) — usar subdomínio
Usa `ebook.industrialcursos.com.br` em vez de `industrialcursos.com.br/ebook`. Funciona igual, mais fácil de configurar.

#### A.1 No GitHub
1. No repositório → Settings → Pages
2. Em **Custom domain**, digite: `ebook.industrialcursos.com.br`
3. Clica Save
4. Marca a caixa **Enforce HTTPS** (após alguns minutos fica disponível)

#### A.2 No seu registrador de domínio (registro.br / HostGator / onde comprou)
Adiciona um registro **CNAME**:
- **Nome/Host:** `ebook`
- **Tipo:** `CNAME`
- **Valor/Destino:** `seu-usuario.github.io.` (com o ponto final!)
- **TTL:** 3600 (ou deixa automático)

Espera 15 min a 2h para propagar. Depois acessa `https://ebook.industrialcursos.com.br` — deve funcionar.

---

### CAMINHO B (mais complexo) — exatamente `industrialcursos.com.br/ebook`
Isso **exige** que você tenha outro site na raiz (`industrialcursos.com.br`) que funcione como "gateway" para `/ebook`. Se a raiz do domínio ainda não tem um site, esse caminho não funciona bem com GitHub Pages.

**Alternativa prática:** Coloca `industrialcursos.com.br` apontando para este site direto (subdomínio vazio):
1. GitHub Pages → Custom domain: `industrialcursos.com.br`
2. Registro DNS tipo **A** apontando para os IPs do GitHub:
   ```
   185.199.108.153
   185.199.109.153
   185.199.110.153
   185.199.111.153
   ```
3. E um CNAME `www` → `seu-usuario.github.io.`

Assim `https://industrialcursos.com.br` abre direto a página do ebook.

---

## Passo 3 — Testar tudo

Depois que o DNS propagar, testa:
- [ ] Site abre em `https://ebook.industrialcursos.com.br` (ou `industrialcursos.com.br`)
- [ ] HTTPS funcionando (cadeado verde)
- [ ] Todos os CTAs levam ao Kiwify (`https://pay.kiwify.com.br/1yebiRk`)
- [ ] WhatsApp abre conversa
- [ ] Vídeo do YouTube toca
- [ ] Foto de Paraty clicando abre o Instagram
- [ ] FAQ abre e fecha ao clicar
- [ ] Responsivo no celular (abre no seu celular e testa)

---

## Passo 4 — (Opcional) Desligar o GreatPages

Quando tudo estiver funcionando no novo site:
1. Entra no GreatPages → `app.greatpages.com.br`
2. Na página `Industrialcursos.com.br` → **Despublicar Página**
3. Se aparecer "Domínio" vinculado a `industrialcursos.com.br`, remova.

⚠️ **NÃO apague o backup** que criamos (`Industrialcursos.com.br - BACKUP 2026-04-19`) — fica lá como segurança histórica dos seus 186 mil acessos.

---

## Editar a página depois

Para mudar QUALQUER coisa (preço, texto, foto):
1. Abre `index.html` ou `style.css` com Bloco de Notas, VS Code ou qualquer editor
2. Mexe no que quiser
3. Sobe o arquivo atualizado no GitHub (arrastar e soltar, substitui automaticamente)
4. Em 1-2 minutos a alteração está no ar

Se não se sentir confortável mexendo, me chama que eu edito para você.

---

## O que está configurado no site

**Conteúdo (do briefing):**
- ✅ Headline: "Como eu montei minha máquina por menos de R$ 35 mil"
- ✅ Subheadline com promessa clara (2 ton/dia, R$ 250 mil no mercado)
- ✅ Vídeo do YouTube: `Rjv4FGYEjmA`
- ✅ História de Paraty completa (Bloco 3) + link do Instagram
- ✅ 7 partes do livro com descrição de cada uma
- ✅ Para quem é / NÃO é (Bloco 6)
- ✅ Investimento honesto (R$ 35 mil meu / R$ 40-60 mil realista)
- ✅ Suporte: e-mail + WhatsApp unidirecional
- ✅ Garantia 7 dias Kiwify
- ✅ CTA com preço R$ 139,90 (parcelável)
- ✅ FAQ com 7 perguntas do briefing
- ✅ Barra flutuante com CTA persistente
- ✅ Foto de Paraty + foto da máquina no galpão

**Técnico:**
- ✅ Responsivo (desktop + mobile)
- ✅ SEO (title, description, Open Graph para WhatsApp/Facebook)
- ✅ HTTPS compatível (só funciona com HTTPS, ativa no GitHub)
- ✅ Fonte Inter carregada do Google Fonts
- ✅ Paleta do briefing: #1E3A5F + #E76F51
- ✅ Vídeo com domínio `youtube-nocookie` (LGPD-friendly)

**O que você precisa trocar no código se quiser:**
- E-mail de suporte: procure no `index.html` por `marcos@industrialmaquinas.com.br` e troque pelo seu real
- Telefone WhatsApp: procure por `5561982302350` e troque se for outro
- Preço: procure por `139` e `139,90` e `242,71` e ajuste

---

## Dúvidas durante o processo

Se travar em qualquer passo (especialmente DNS), me chama de volta aqui com o erro exato ou print da tela. DNS é onde 90% das pessoas trava na primeira vez, é normal.

**Boa sorte!** 🚀
