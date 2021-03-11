# Calcular media
 
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Números com JS</title>
    <style>
        body { font: 12pt Arial; }
        button { font-size: 12pt; padding: 30px; }
    </style>
</head>
<body>
    <h1>Média do aluno v1.0</h1>
    <button onclick="media()">Calcular média</button>
    <section id="situacao">
        <p>O resultado vai aparecer aqui...</p>
    </section>

    <script>
    
        function media() {
            let nom = window.prompt('Qual é o nome do aluno?') // Já que o nome não é um número e sim letras, não é preciso colocar Number() para fazer a covnersão
            let n1 = Number(window.prompt(`Qual foi a primeira nota de ${nom}?`))
            let n2 = Number(window.prompt(`Além de ${n1}, qual foi a outra nota de ${nom}?`))
            med = (n1 + n2)/2 // Se você não colocar os parênteses para forçar a precedência, seu cálculo vai dar um resultado errado, já que a divisão será feita antes.

            let res = document.getElementById('situacao')
            res.innerHTML = `<p>Calculando a média final de <mark>${nom}</mark>.</p>`
            res.innerHTML += `<p>As notas obtidas foram <mark>${n1} e ${n2}</mark>.</p>` // O += é necessário, pois indica um pedido de "mantenha a frase anterior, adicionando essa outra frase". Se não fosse ele, a linha anterior seria apagada.
            res.innerHTML += `<p>A média final será <mark>${med}</mark>.</p>`
        }
    </script>
</body>
</html>
