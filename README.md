# frases-e-frases
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Frases e Frases</title>
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/tailwindcss/dist/tailwind.min.css">
  <style>
    body {
      background: url('https://images.unsplash.com/photo-1506744038136-46273834b3fb?auto=format&fit=crop&w=1600&q=80') no-repeat center center fixed;
      background-size: cover;
      transition: background 0.5s ease;
    }
    .conteudo {
      display: none;
      background: rgba(255, 255, 255, 0.85);
      padding: 2rem;
      border-radius: 1rem;
      box-shadow: 0 0 15px rgba(0,0,0,0.2);
    }
    .ativo {display: block;}
    .texto-poema {font-size: 1.5rem; line-height: 2.2rem; font-weight: 500; color: #222;}
    .dark .conteudo {background: rgba(30, 30, 30, 0.85); color: #eee; box-shadow: 0 0 15px rgba(255,255,255,0.1);}
    header, footer {backdrop-filter: saturate(180%) blur(20px);}
  </style>
</head>
<body class="bg-white/90 dark:bg-gray-900/90 text-gray-900 dark:text-white transition-colors">
  <header class="p-5 flex flex-wrap justify-between items-center border-b bg-white/80 dark:bg-gray-800/80 shadow-md">
    <h1 class="text-3xl font-bold">Frases e Frases</h1>
    <nav class="space-x-4 mt-2 md:mt-0">
      <button onclick="mostrar('amor')" class="hover:underline text-lg">Amor</button>
      <button onclick="mostrar('reflexao')" class="hover:underline text-lg">Reflexão</button>
      <button onclick="mostrar('natureza')" class="hover:underline text-lg">Natureza</button>
      <button onclick="mostrar('home')" class="hover:underline text-lg">Início</button>
    </nav>
    <div class="space-x-2 mt-2 md:mt-0">
      <button id="temaBtn" class="px-4 py-2 bg-blue-500 text-white rounded-lg hover:scale-105 transition-transform">Alternar Tema</button>
      <button id="fundoBtn" class="px-4 py-2 bg-green-500 text-white rounded-lg hover:scale-105 transition-transform">Trocar Fundo</button>
      <button id="galeriaBtn" class="px-4 py-2 bg-purple-500 text-white rounded-lg hover:scale-105 transition-transform">Escolher Paisagem</button>
    </div>
  </header>

  <main id="home" class="conteudo mt-5 max-w-4xl mx-auto">
    <h2 class="text-2xl font-bold mb-4">Bem-vindo ao site de frases</h2>
    <p class="text-xl">Escolha uma categoria no menu acima para visualizar os poemas completos com letras maiores e mais fáceis de ler.</p>
  </main>

  <main id="amor" class="conteudo mt-5 max-w-4xl mx-auto">
    <article class="mb-8">
      <h3 class="text-3xl font-bold mb-4">Ecos do Coração</h3>
      <p class="texto-poema">Quando teu sorriso encontra o meu olhar,<br>o mundo silencia em um instante de paz.<br>Cada toque teu é verso que não sei rimar,<br>mas que escreve na alma o mais belo dos sinais.<br><br>E quando a noite cai, fria e sem luar,<br>lembro do calor dos teus abraços.<br>Pois amar-te é mais do que apenas estar,<br>é viver contigo todos os espaços.</p>
    </article>
  </main>

  <main id="reflexao" class="conteudo mt-5 max-w-4xl mx-auto">
    <article class="mb-8">
      <h3 class="text-3xl font-bold mb-4">Caminhos da Vida</h3>
      <p class="texto-poema">Nem sempre o caminho mais fácil é o mais certo.<br>A estrada longa ensina a paciência,<br>os tropeços ensinam humildade,<br>e cada curva nos mostra quem realmente somos.<br><br>Olhe para trás com gratidão,<br>para frente com esperança,<br>e viva o agora com plenitude,<br>pois é nele que mora a verdadeira transformação.</p>
    </article>
  </main>

  <main id="natureza" class="conteudo mt-5 max-w-4xl mx-auto">
    <article class="mb-8">
      <h3 class="text-3xl font-bold mb-4">Canção da Floresta</h3>
      <p class="texto-poema">O vento dança com as folhas,<br>o rio canta com seu próprio tom.<br>Cada flor exala poesia,<br>cada raiz conta uma história antiga.<br><br>A natureza é mestra silenciosa,<br>guia dos passos apressados.<br>Basta parar, ouvir e sentir:<br>a Terra também respira em nós.</p>
    </article>
  </main>

  <footer class="p-5 text-center text-gray-500 border-t bg-white/80 dark:bg-gray-800/80 mt-10 text-lg">
    © 2025 Frases e Frases - Feito por Cassio
  </footer>

  <script>
    const imagensGaleria = [
      'https://images.unsplash.com/photo-1506744038136-46273834b3fb?auto=format&fit=crop&w=1600&q=80',
      'https://images.unsplash.com/photo-1470770841072-f978cf4d019e?auto=format&fit=crop&w=1600&q=80',
      'https://images.unsplash.com/photo-1500530855697-b586d89ba3ee?auto=format&fit=crop&w=1600&q=80',
      'https://images.unsplash.com/photo-1518458028785-8fbcd101ebb9?auto=format&fit=crop&w=1600&q=80',
      'https://images.unsplash.com/photo-1526778548025-fa2f459cd5c1?auto=format&fit=crop&w=1600&q=80',
      'https://images.unsplash.com/photo-1504384308090-c894fdcc538d?auto=format&fit=crop&w=1600&q=80',
      'https://images.unsplash.com/photo-1524504388940-b1c1722653e1?auto=format&fit=crop&w=1600&q=80'
    ];

    function mostrar(secao){
      document.querySelectorAll('.conteudo').forEach(s=>s.classList.remove('ativo'));
      document.getElementById(secao).classList.add('ativo');
      window.scrollTo(0,0);
    }

    document.getElementById('temaBtn').addEventListener('click', ()=>{
      document.documentElement.classList.toggle('dark');
    });

    document.getElementById('fundoBtn').addEventListener('click', ()=>{
      const url = prompt('Digite a URL da imagem de fundo:');
      if(url){
        document.body.style.background = `url('${url}') no-repeat center center fixed`;
        document.body.style.backgroundSize = 'cover';
      }
    });

    document.getElementById('galeriaBtn').addEventListener('click', ()=>{
      const escolha = Math.floor(Math.random() * imagensGaleria.length);
      document.body.style.background = `url('${imagensGaleria[escolha]}') no-repeat center center fixed`;
      document.body.style.backgroundSize = 'cover';
    });

    window.onload = ()=>mostrar('home');
  </script>
</body>
</html>

