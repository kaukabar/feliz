<!DOCTYPE html> 
<html lang="pt"> 
<head> 
    <meta charset="UTF-8"> 
    <meta name="viewport" content="width=device-width, initial-scale=1.0"> 
    <title>29/10</title> 
    <style> 
        corpo { 
            família da fonte: "Times New Roman", serif; 
            margem: 0; 
            cor de fundo: #1e1e2f; 
            cor: #f0f0f0; 
            estouro: oculto; 
        } 
        .container { 
            alinhamento do texto: centralizado; 
            exibição: flex; 
            justificar o conteúdo: centralizado; 
            alinhar os itens: centralizado; 
            altura: 100vh; 
            direção flexível: coluna; 
        } 
        entrada[tipo="senha"] { 
            preenchimento: 10px; 
            margem superior: 10px; 
            tamanho da fonte: 16px; 
            borda: 1px sólido #555; 
            raio da borda: 5px; 
            cor de fundo: #3e3e4e; 
            cor: #fff; 
        } 
        botão { 
            preenchimento: 10px 20px; 
            margem superior: 10px; 
            tamanho da fonte: 16px; 
            cor de fundo: #007bff; 
            cor: #fff; 
            borda: nenhuma; 
            raio da borda: 5px; 
            cursor: ponteiro; 
        } 
        botão: pairar { 
            cor de fundo: #0056b3; 
        } 
        .erro { 
            cor: vermelho; 
            margem superior: 10px; 
        } 
        # recipiente-balão { 
            posição: absoluto; 
            topo: 0; 
            esquerda: 0; 
            largura: 100%; 
            altura: 100%; 
            estouro: oculto; 
            índice z: -1; 
        } 
        .balão { 
            posição: absoluto; 
            largura: 50px; 
            altura: 70px; 
            cor de fundo: vermelho; 
            raio da borda: 50%; 
            animação: flutuante 5s linear infinito; 
        } 
        .balão:: antes { 
            conteúdo: ''; 
            posição: absoluto; 
            largura: 2px; 
            altura: 20px; 
            fundo: #fff; 
            fundo: -20px; 
            esquerda: 50%; 
            transformar: traduzirX(-50%); 
        } 
        @keyframes float { 
            0% { 
                transformar: traduzirY(100vh); 
                opacidade: 0; 
            } 
            50% { 
                opacidade: 1; 
            } 
            100% { 
                transformar: traduzirY(-10vh); 
                opacidade: 0; 
            } 
        } 
        .content { 
            alinhamento do texto: justificar; 
            fundo: #2e2e3e; 
            preenchimento: 20px; 
            raio da borda: 10px; 
            sombra da caixa: 0 4px 6px rgba(0, 0, 0, 0.3); 
            largura máxima: 800px; 
            margem: 40px automático; 
            estouro-y: automático; 
            altura máxima: 80vh; 
        } 
        .content h1 { 
            alinhamento do texto: centralizar; 
            margem inferior: 20px; 
        } 
        .dedicação { 
            margem superior: 20px; 
            tamanho da fonte: 14px; 
            alinhamento do texto:centro; 
        } 
    </style> 
    <script> 
        função checkPassword() { 
            const senha = document.getElementById('senha').value; 
            const correctPassword = "the1"; 
            if (senha === correctPassword) { 
                document.body.innerHTML = `
                    <div id="balloon-container"></div> 
                    <div class="content"> 
                        <h1>FELIZ ANIVERSÁRIO MEU LINDO</h1>
                        <p>Eu era como um suicida jogando roleta russa em um parque de diversões abandonado...</p>
                        <p><b>feliz aniversário senhor lucas araujo fernandes...</b></p>
                    </div>`;
                startBalloons(); 
            } else { 
                alert("Senha incorreta. Tente novamente!"); 
            } 
        } 
        function startBalloons() { 
            const container = document.getElementById('balloon-container'); 
            for (let i = 0; i < 30; i++) { 
                const balloon = document.createElement('div'); 
                balloon.classList.add('balloon'); 
                balloon.style.backgroundColor = getRandomColor(); 
                balloon.style.left = Math.random() * 100 + 'vw'; 
                balloon.style.animationDuration = Math.random() * 2 + 3 + 's'; 
                container.appendChild(balloon); 
            } 
        } 
        function getRandomColor() { 
            const cores = ['#ff0000', '#ffa500', '#ffff00', '#00ff00', '#00ffff', '#0000ff', '#ff00ff']; 
            return cores[Math.floor(Math.random() * cores.length)]; 
        } 
    </script> 
</head> 
<body> 
    <div class="container"> 
        <h1>ALERTA</h1> 
        <p>Insira a senha para acessar o conteúdo:</p> 
        <p>Dica: a senha está na imagem que foi enviada</p> 
        <p>BOBAO, EU SEI A SENHA E VOCE NAO</p> 
        <input type="password" id="senha" placeholder="TENTE A SENHA"> 
        <button onclick="checkPassword()">Entrar</button> 
    </div> 

    <!-- Música adicionada diretamente ao carregar a página -->
    <iframe width="560" height="315" src="https://www.youtube.com/embed/cZb-ubdscvA?autoplay=1" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</body> 
