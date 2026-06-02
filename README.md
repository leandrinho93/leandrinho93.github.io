# 🌐 leandrinho93.github.io

Este é o repositório raiz e servidor estático principal do ecossistema **LMTR**, hospedado via **GitHub Pages**. Ele atua como a central de autenticação criptográfica para os aplicativos móveis e como o validador oficial de segurança perante as redes de anúncios do Google.

---

## 🔐 1. Autenticação de Links (Android App Links)

A pasta oculta `.well-known` abriga o arquivo `assetlinks.json`. Este arquivo é a peça fundamental que viabiliza o sistema de **Deep Linking Seguro** (compartilhamento e importação automática de bolões entre usuários do aplicativo *Estratégia Loteria*).

Como funciona esta camada:
Segurança Nativa: Quando um link de bolão é clicado no WhatsApp, o sistema operacional Android consulta este repositório em milissegundos para verificar se a assinatura digital (sha256_cert_fingerprints) bate com o aplicativo instalado.

Prevenção de Fraudes: Por ser uma validação baseada em criptografia assimétrica na raiz do domínio, é impossível que aplicativos terceiros ou maliciosos interceptem ou simulem os links gerados pelos nossos usuários.

💰 2. Monetização e Inventário (Google AdMob)
O arquivo app-ads.txt na raiz deste repositório serve como a declaração pública de Vendedor Autorizado (Authorized Digital Sellers) exigida pelo Google AdMob para os aplicativos da marca.

Proteção de Receita: Ele lista os IDs de distribuidor autorizados a comercializar espaços publicitários dentro dos nossos aplicativos.

Prevenção de Ad Fraud: Garante que marcas e anunciantes comprem mídia com total transparência, blindando o ecossistema contra fraudes de inventário e garantindo a correta entrega e remuneração dos blocos de anúncios (Banners, Intersticiais e Premiados).

🛠️ Infraestrutura Técnica
Provedor: GitHub Pages (Serverless)

Bypass de Compilação: O arquivo .nojekyll na raiz força o servidor a ignorar as travas do motor Jekyll, permitindo a leitura pública de diretórios que começam com ponto (como a .well-known).

Protocolo Forçado: HTTPS ativo com TLS de ponta a ponta para conformidade estrita com os requisitos de rede do Android 10+.

📲 Projetos Relacionados
A infraestrutura de dados que consome e distribui as APIs de sorteios das loterias e os scripts das páginas de captura finais podem ser encontrados no repositório irmão:
🔗 api-loterias

Mantido e gerenciado por Leandro Silva da Costa.
