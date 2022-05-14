	<!DOCTYPE html>
	<html>
	<head>
		<meta charset="utf-8">
		<meta name="viewport" content="width=device-width, initial-scale=1">
		<meta author="Guilherme fernandes de souza, RA: 00228895">
		<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-1BmE4kWBq78iYhFldvKuhfTAU6auU8tT94WrHftjDbrCEXSU1oBoqyl2QvZ6jIW3" crossorigin="anonymous">

		<title>Contador de cliques</title>
		<style type="text/css">
			.quadro{
				background-color: #f2f2f2;
				width: 300px;
				height: 75px;
				margin-bottom: 25px;
				border-radius: 10px;
			}
		</style>	

		<body>
			<center>
					<h3>Contador de cliques</h3>
					<div class="quadro">
						<h3>Número de cliques: <h3 id="cliques">0</h3></h3>
					</div>

					<div class="quadro">
						<h3>Número de dezenas: <h3 id="dezena">0</h3></h3>
					</div>

					<div class="quadro"> 
						<h3>Número de resets: <h3 id="reset">0</h3></h3>
					</div>

					<div>
						<button class="btn btn-primary" onclick="contar_1()">Add</button>
						<button class="btn btn-danger" onclick="resetar_cont()">Reset</button>
					</div>
			</center>

			<script type="text/javascript">
				var contagem = 0;
				var	resetar = 0;
				var dezenas = 0;

				function contar_1() {
					atualizar(++contagem);
					if ((contagem % 10) == 0){
						atualizar_dezena(++dezenas)
						alert('O botão ja foi clicado mais 10 vezes')

					}
				}

				function resetar_cont() {
					if ((contagem)!= 0) {
						atualizar_reset(++resetar);
					}else{
						alert('o contador ja esta zerado')
					}
					contagem = 0;
					dezenas = 0;
					atualizar(contagem);
					atualizar_dezena(dezenas);
					
				}

				function atualizar(val) {
					document.getElementById("cliques").innerHTML = val;
				}

				function atualizar_reset(val) {
					document.getElementById("reset").innerHTML = val;
				}

				function atualizar_dezena(val) {
					document.getElementById("dezena").innerHTML = val;

				}
			</script>



		</body>
		</html>
