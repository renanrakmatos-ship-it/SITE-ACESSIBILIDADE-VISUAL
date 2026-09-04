<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portal da Visão - Acessibilidade Visual</title>
    <style>
        :root {
            --bg-color: #121212;
            --surface-color: #1e1e1e;
            --text-color: #ffffff;
            --accent-color: #ffd700;
            --link-color: #82aaff;
            --font-scale: 1rem;
        }

        body.light-theme {
            --bg-color: #ffffff;
            --surface-color: #f4f4f4;
            --text-color: #000000;
            --accent-color: #000000;
            --link-color: #0000ee;
        }

        html {
            font-size: var(--font-scale);
        }

        body {
            font-family: Arial, sans-serif;
            font-size: 1.2rem;
            line-height: 1.6;
            background-color: var(--bg-color);
            color: var(--text-color);
            margin: 0;
            padding: 0;
            transition: background-color 0.3s, color 0.3s;
        }

        .skip-link {
            position: absolute;
            top: -40px;
            left: 0;
            background: var(--accent-color);
            color: #000;
            padding: 8px;
            z-index: 100;
        }

        .skip-link:focus {
            top: 0;
        }

        .accessibility-bar {
            background-color: #000;
            padding: 10px 2rem;
            display: flex;
            gap: 10px;
            align-items: center;
            border-bottom: 1px solid #333;
        }

        .accessibility-bar button {
            background-color: var(--accent-color);
            color: #000;
            border: 2px solid #fff;
            padding: 8px 12px;
            font-weight: bold;
            font-size: 1rem;
            cursor: pointer;
            border-radius: 4px;
        }

        .accessibility-bar button:focus, 
        .accessibility-bar button:hover {
            outline: 3px solid #ffffff;
            background-color: #fff;
            color: #000;
        }

        header {
            background-color: var(--surface-color);
            padding: 1rem 2rem;
            border-bottom: 3px solid var(--accent-color);
        }

        h1 {
            margin: 0;
            color: var(--accent-color);
        }

        nav ul {
            list-style: none;
            padding: 0;
            display: flex;
            gap: 15px;
            flex-wrap: wrap;
        }

        nav a {
            color: var(--link-color);
            text-decoration: underline;
            font-weight: bold;
        }

        nav a:focus, nav a:hover {
            outline: 3px solid var(--accent-color);
        }

        main {
            padding: 2rem;
            max-width: 900px;
            margin: 0 auto;
        }

        section {
            margin-bottom: 2rem;
        }

        h2 {
            border-bottom: 2px solid var(--accent-color);
            padding-bottom: 0.5rem;
        }

        h3 {
            color: var(--accent-color);
            margin-top: 1.5rem;
        }

        .img-container {
            margin: 1.5rem 0;
            text-align: center;
        }

        .responsive-img {
            max-width: 100%;
            height: auto;
            border-radius: 8px;
            border: 2px solid var(--accent-color);
        }

        figcaption {
            font-size: 0.95rem;
            margin-top: 8px;
            font-style: italic;
        }

        .qrcode-section {
            background-color: var(--surface-color);
            border: 2px solid var(--accent-color);
            border-radius: 8px;
            padding: 1.5rem;
            text-align: center;
            margin-top: 2rem;
        }

        .qrcode-box {
            display: inline-block;
            padding: 12px;
            background-color: #ffffff;
            border-radius: 4px;
            margin-top: 10px;
        }

        footer {
            background-color: var(--surface-color);
            text-align: center;
            padding: 1rem;
            border-top: 1px solid #333;
        }
    </style>
</head>
<body>

    <a class="skip-link" href="#conteudo-principal">Ir para o conteúdo principal</a>

    <div class="accessibility-bar" role="region" aria-label="Ferramentas de Acessibilidade">
        <button id="btn-increase" aria-label="Aumentar o tamanho do texto">A+</button>
        <button id="btn-decrease" aria-label="Diminuir o tamanho do texto">A-</button>
        <button id="btn-reset" aria-label="Redefinir o tamanho do texto">A (Normal)</button>
        <button id="btn-theme" aria-label="Alternar contraste da página">Alternar Contraste</button>
    </div>

    <header>
        <h1>Portal da Visão</h1>
        <nav aria-label="Navegação Principal">
            <ul>
                <li><a href="#sobre">Sobre</a></li>
                <li><a href="#deficiencias">Deficiências</a></li>
                <li><a href="#sintomas-tratamentos">Sintomas e Tratamentos</a></li>
                <li><a href="#recursos">Recursos</a></li>
                <li><a href="#dicas">Dicas</a></li>
            </ul>
        </nav>
    </header>

    <main id="conteudo-principal">
        <section id="sobre">
            <h2>Sobre o Portal</h2>
            <p>O <strong>Portal da Visão</strong> é um espaço dedicado a promover a inclusão digital e a conscientização sobre acessibilidade visual na web.</p>
            
            <figure class="img-container">
                <img class="responsive-img" src="https://equalweb.com.br/wp-content/uploads/2025/07/ew-2025-04-16-blog-leitor-de-tela_06.png" alt="Pessoa utilizando um computador desktop com opções de acessibilidade visual na tela.">
                <figcaption>Exemplo de interface web acessível sendo utilizada no computador.</figcaption>
            </figure>
        </section>

        <section id="deficiencias">
            <h2>Principais Deficiências Visuais</h2>
            <ul>
                <li><strong>Cegueira:</strong> Perda total da visão ou capacidade de percepção de luz extremamente reduzida.</li>
                <li><strong>Baixa Visão (Visão Subnormal):</strong> Alteração grave na acuidade visual que não pode ser totalmente corrigida com óculos comuns ou cirurgias.</li>
                <li><strong>Catarata:</strong> Opacificação do cristalino que torna a visão embaçada ou nublada.</li>
                <li><strong>Glaucoma:</strong> Dano ao nervo óptico que costuma afetar inicialmente a visão periférica.</li>
                <li><strong>Degeneração Macular (DMRI):</strong> Afeta a parte central da retina, dificultando a leitura e a identificação de rostos.</li>
                <li><strong>Daltonismo:</strong> Dificuldade na percepção de cores ou na distinção entre certos tons.</li>
            </ul>

            <figure class="img-container">
                <img class="responsive-img" src="https://images.unsplash.com/photo-1576091160399-112ba8d25d1d?q=80&w=800&auto=format&fit=crop" alt="Exame Oftalmológico mostrando os olhos de um paciente sendo examinados por um médico especialista em saúde ocular.">
                <figcaption>Exames oftálmicos periódicos são fundamentais para a detecção precoce de deficiências visuais.</figcaption>
            </figure>
        </section>

        <section id="sintomas-tratamentos">
            <h2>Sintomas e Tratamentos</h2>
            <p>Conhecer os sintomas é essencial para o diagnóstico precoce, e o tratamento varia conforme a causa e a severidade de cada condição:</p>

            <h3>1. Cegueira</h3>
            <ul>
                <li><strong>Sintomas:</strong> Incapacidade total de enxergar ou percepção mínima apenas de estímulos luminosos.</li>
                <li><strong>Tratamento e Reabilitação:</strong> Quando irreversível, o foco é a reabilitação visual com uso de bengala longa, aprendizagem do sistema Braille e uso de tecnologias assistivas.</li>
            </ul>

            <h3>2. Baixa Visão</h3>
            <ul>
                <li><strong>Sintomas:</strong> Visão bastante embaçada, manchas no campo visual ou perda de visão periférica.</li>
                <li><strong>Tratamento e Reabilitação:</strong> Recursos ópticos (lupas, telescópios e óculos especiais), iluminação adequada e softwares com recursos de ampliação.</li>
            </ul>

            <h3>3. Catarata</h3>
            <ul>
                <li><strong>Sintomas:</strong> Visão nublada ou opaca, sensibilidade ao brilho de luzes e desbotamento das cores.</li>
                <li><strong>Tratamento:</strong> Cirurgia para substituição do cristalino por uma lente intraocular artificial.</li>
            </ul>

            <h3>4. Glaucoma</h3>
            <ul>
                <li><strong>Sintomas:</strong> Perda progressiva da visão periférica ("visão em túnel").</li>
                <li><strong>Tratamento:</strong> Colírios específicos, laserterapia ou procedimentos cirúrgicos para controle da pressão intraocular.</li>
            </ul>

            <h3>5. Degeneração Macular Relacionada à Idade (DMRI)</h3>
            <ul>
                <li><strong>Sintomas:</strong> Ponto cego ou mancha escura no centro do campo visual.</li>
                <li><strong>Tratamento:</strong> Suplementação vitamínica específica ou injeções de medicamentos anti-VEGF.</li>
            </ul>

            <h3>6. Daltonismo</h3>
            <ul>
                <li><strong>Sintomas:</strong> Dificuldade para diferenciar cores específicas (verde e vermelho).</li>
                <li><strong>Tratamento:</strong> Óculos com lentes de filtros de cor especiais e aplicativos mobile de identificação de cores.</li>
            </ul>

            <figure class="img-container">
                <img class="responsive-img" src="https://images.unsplash.com/photo-1591076482161-42ce6da69f67?q=80&w=800&auto=format&fit=crop" alt="Lupa médica de aumento posicionada sobre um texto impresso para facilitar a leitura.">
                <figcaption>Lupas de aumento e lentes especiais são recursos de auxílio óptico para pessoas com baixa visão.</figcaption>
            </figure>
        </section>

        <section id="recursos">
            <h2>Recursos para Acessibilidade Visual</h2>
            <ul>
                <li><strong>Leitores de Tela:</strong> Softwares que convertem texto em áudio para usuários cegos ou com baixa visão.</li>
                <li><strong>Linhas Braille:</strong> Dispositivos que convertem o texto da tela em pontos de Braille em tempo real.</li>
                <li><strong>Alto Contraste:</strong> Opções de temas para facilitar a leitura.</li>
            </ul>

            <figure class="img-container">
                <img class="responsive-img" src="https://encrypted-tbn2.gstatic.com/licensed-image?q=tbn:ANd9GcTYgtw9aAPJZYsRMUAriJ3oWkLtUZrCu_o9TPx-JnwLDFGQnrpNmwoOoD7pV9750JWv9vq_WgDEchpd9qs" alt="Mãos de uma pessoa utilizando um teclado com linha Braille conectado a um computador.">
                <figcaption>Dispositivo de linha Braille utilizado para leitura tátil de conteúdos digitais.</figcaption>
            </figure>
        </section>

        <section id="dicas">
            <h2>Como Criar Conteúdo Acessível</h2>
            <ol>
                <li>Use tags semânticas do HTML.</li>
                <li>Sempre adicione o atributo <code>alt</code> descritivo nas imagens.</li>
                <li>Garanta contraste de cor adequado entre texto e fundo.</li>
            </ol>
        </section>

        <section class="qrcode-section" aria-labelledby="titulo-qrcode">
            <h2 id="titulo-qrcode">QR Code: Saiba Mais Sobre Saúde Ocular</h2>
            <p>Escaneie o QR Code abaixo para acessar o relatório oficial da OMS (Organização Mundial da Saúde) sobre cegueira e deficiências visuais:</p>
            <div class="qrcode-box">
                <div id="qrcode"></div>
            </div>
        </section>
    </main>

    <footer>
        <p>&copy; 2026 Portal da Visão - Promovendo a inclusão digital.</p>
    </footer>

    <script src="https://cdnjs.cloudflare.com/ajax/libs/qrcodejs/1.0.0/qrcode.min.js"></script>

    <script>
        let fontScale = 1;
        const root = document.documentElement;
        const btnIncrease = document.getElementById('btn-increase');
        const btnDecrease = document.getElementById('btn-decrease');
        const btnReset = document.getElementById('btn-reset');
        const btnTheme = document.getElementById('btn-theme');

        btnIncrease.addEventListener('click', () => {
            if (fontScale < 1.5) {
                fontScale += 0.1;
                root.style.setProperty('--font-scale', `${fontScale}rem`);
            }
        });

        btnDecrease.addEventListener('click', () => {
            if (fontScale > 0.8) {
                fontScale -= 0.1;
                root.style.setProperty('--font-scale', `${fontScale}rem`);
            }
        });

        btnReset.addEventListener('click', () => {
            fontScale = 1;
            root.style.setProperty('--font-scale', '1rem');
        });

        btnTheme.addEventListener('click', () => {
            document.body.classList.toggle('light-theme');
        });

        const urlDeficiencias = "https://www.who.int/news-room/fact-sheets/detail/blindness-and-visual-impairment";

        new QRCode(document.getElementById("qrcode"), {
            text: urlDeficiencias,
            width: 150,
            height: 150,
            colorDark : "#000000",
            colorLight : "#ffffff",
            correctLevel : QRCode.CorrectLevel.H
        });
    </script>
</body>
</html>
