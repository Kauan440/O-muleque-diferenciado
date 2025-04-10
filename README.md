<!DOCTYPE html>
2<html lang="pt-BR">
3<head>
4    <meta charset="UTF-8">
5    <meta name="viewport" content="width=device-width, initial-scale=1.0">
6    <title>Navegador Favela</title>
7    <style>
8        body {
9            font-family: Arial, sans-serif;
10            background-color: #2c3e50; /* Cor de fundo urbana */
11            color: white;
12            text-align: center;
13            padding: 20px;
14        }
15        button {
16            padding: 10px 20px;
17            font-size: 16px;
18            cursor: pointer;
19            background-color: #e74c3c; /* Cor vibrante */
20            border: none;
21            color: white;
22            border-radius: 5px;
23        }
24        .hidden {
25            display: none;
26        }
27    </style>
28</head>
29<body>
30    <h1>Bem-vindo ao Navegador Favela</h1>
31    <audio controls autoplay loop>
32        <source src="caminho/para/sua/musica/baile_do_panta.mp3" type="audio/mpeg">
33        Seu navegador não suporta o elemento de áudio.
34    </audio>
35    
36    <button onclick="window.location.href='https://www.instagram.com/moraees_inwl/'">Meu Instagram</button>
37    
38    <div id="publico">
39        <h2>Página Pública</h2>
40        <p>Aqui você pode ver conteúdos públicos.</p>
41        <!-- Área de postagem pública -->
42    </div>
43    
44    <div id="vip" class="hidden">
45        <h2>Página VIP</h2>
46        <p>Acesso restrito a conteúdos VIP.</p>
47        <!-- Área de postagem VIP -->
48    </div>
49    
50    <div id="painelSaque" class="hidden">
51        <h2>Painel de Saque Privado</h2>
52        <p>Área privada para gerenciamento de saques.</p>
53        <!-- Conteúdo do painel de saque -->
54    </div>
55    
56    <script>
57        // Função para alternar entre público e VIP
58        function toggleVIP() {
59            const publico = document.getElementById('publico');
60            const vip = document.getElementById('vip');
61            if (vip.classList.contains('hidden')) {
62                publico.classList.add('hidden');
63                vip.classList.remove('hidden');
64            } else {
65                vip.classList.add('hidden');
66                publico.classList.remove('hidden');
67            }
68        }
69
70        // Modo desenvolvedor (exemplo simples)
71        const isDevMode = false; // Mude para true no seu celular
72        if (isDevMode) {
73            document.getElementById('painelSaque').classList.remove('hidden');
74        }
75    </script>
76</body>
77</html>
