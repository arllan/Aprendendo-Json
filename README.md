# Aprendendo-Json
Estruturas básicas de como criar arquivos .json



# Introdução

O json e um formato de arquivo de padrão aberto. A sigla ```JSON``` vem do JSON (JavaScript Object Notation), o json e uma alternativa ao antigo XML. Veja a seguir uma breve introdução a sua estrutura de dados.



# Estrutura base do json. 

```{"name":"value" }``` 

Para cada valor representado, atribui-se um nome (ou rótulo) que descreve o seu significado.

```name``` = rótulo

```value``` = valor representado



# Tipos de dados

Numérico: ```{"name":31}```

Lógico: ```{"name":true} ```

String: ``` "nome": "arllan"```

Null: ```{"name":null}```



# Criando primeira estrutura
  ```
  { 
		"nome": "arllan",
		"sobreNome": "pablo",
		"idade": 21,
		"status":true,
		"faculdade": "Faculdade São Miguel",
		"rua": "800",
		"bairro": "maranguape",
		"cidade": "Paulista"
 }
```


# Valores em um objeto JSON pode ser outro objeto JSON

```
   {
		  "nome": "arllan",
		  "sobreNome": "pablo",
		  "idade": "21",
		  "faculdade": "faculdade são miguel",
		  "rua": "800",
		  "bairro": "maranguape",
		  "cidade": "paulista",
		  "cursos": {
		    "cursoA": "HTML",
		    "cursoB": "JAVASCRIPT",
		    "cursoC": "PHP",
		    "cursoD": "BOOTSTRAP"
		  }
		}
```



# Criando vários objetos

```
  {
		  "Aula01": {	// objeto Aula01 com seus elementos 
		    "senha": "12345",
		    "explorar": "4",
		    "criar": "45",
		    "compartilhar": "24",
		    "desafio": "3"
		  },
		  "Aula02": {	// objeto Aula02 com seus elementos 
		    "senha": "12345",
		    "explorar": "2",
		    "criar": "6",
		    "compartilhar": "32",
		    "desafio": "6"
		  },
		  "Aula03": {	// objeto Aula03 com seus elementos 
		    "senha": "12345",
		    "explorar": "2",
		    "criar": "6",
		    "compartilhar": "32",
		    "desafio": "6"
		  }
		}
```



# Criando objeto com array
```
[

		  { "Aula01":"ok", 
		    "senha": "12345",
		    "explorar": "4",
		    "criar": "45",
		    "compartilhar": "24",
		    "desafio": "3"
		  },

		  { "Aula02": "ok",
		    "senha": "12345",
		    "explorar": "2",
		    "criar": "6",
		    "compartilhar": "32",
		    "desafio": "6"
		  },

		  { "Aula03": "ok",
		    "senha": "12345",
		    "explorar": "2",
		    "criar": "6",
		    "compartilhar": "32",
		    "desafio": "6"
		  }
		]
```



# Testando json com javascript (exemplo)

```
var testeArray =
		[

		  { "Aula01":"ok", 
		    "senha": "12345",
		    "explorar": "4",
		    "criar": "45",
		    "compartilhar": "24",
		    "desafio": "3"
		  },

		  { "Aula02": "ok",
		    "senha": "12345",
		    "explorar": "2",
		    "criar": "6",
		    "compartilhar": "32",
		    "desafio": "6"
		  },

		  { "Aula03": "ok",
		    "senha": "12345",
		    "explorar": "2",
		    "criar": "6",
		    "compartilhar": "32",
		    "desafio": "6"
		  }
		]

		console.log(testeArray); // mostra todos elementos do objeto
		console.log(testeArray[2]); // acessa apenas o indice 2 
   
   ```
   # acessando json via jquery (de forma local com o $.each)
   ```
   <!doctype html>
<html>
    <head>
        <meta charset="utf-8">
        <title>PHP com AJAX</title>
    </head>

    <body>
        <div id="listagem">-</div>
        <script src="jquery.js"></script>
        <script>
			$.getJSON('_json/produtos.json', function(data){ // chama
            $.each(data, function(i,valor){

                console.log(valor.nomeproduto); // chamando todos os elementos nomeproduto

                console.log(valor); // chamando todos os elementos do json
            });

            });
		</script>
    </body>
</html>
   ```
   
   
   # acessando json via jquery (de forma local)
   
   
   obs: arquivos externos json e jquery 
   ```
   <!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
	<meta http-equiv="X-UA-Compatible" content="IE=edge">
	<title></title>
	<link rel="stylesheet" href="">
	<style type="text/css" media="screen">
		.texto {font-size: 30px}
	</style>
</head>
<body>
	<center> <p class="texto"> Neste mini tutorial vamos aprender as formas de trabalhar com o ajax utilizando jquery</p></center>
	<h1 id="h1ElementAdd"></h1> <!--elemento que recebe o texto-->
	<button id="ViaLoad">Carregar via load</button> <!--botao que acionar a requisição-->

	<script src="jquery.js"></script>
	<script type="text/javascript">
		$.getJSON('local.json',function(data) {
			console.log(data); // mostrar todas as informações
			console.log(data[0]); // chama apenas os campos do indice 0
			console.log(data[0].senha); // chama apenas o campo do indice 0 senha
		});
	</script>
</body>
</html>
   ```
   
   
   
   # Apredendo ajax com jquery (utilizando o método LOAD() do jquery)
   
   obs: arquivos extras são o jquery e o texto.txt
   
   ```
   <!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
	<meta http-equiv="X-UA-Compatible" content="IE=edge">
	<title></title>
	<link rel="stylesheet" href="">
	<style type="text/css" media="screen">
		.texto {font-size: 30px}
	</style>
</head>
<body>
	<center> <p class="texto"> Neste mini tutorial vamos aprender as formas de trabalhar com o ajax utilizando jquery</p></center>
	<h1 id="h1ElementAdd"></h1> <!--elemento que recebe o texto-->
	<button id="ViaLoad">Carregar via load</button> <!--botao que acionar a requisição-->

	<script src="jquery.js"></script>
	<script type="text/javascript">
		$('#ViaLoad').on('click',carregarAjax); // seleciona o elemento e evento

		function carregarAjax() // função a ser chamada pelo evento
		{
			$("#h1ElementAdd").load('texto.txt'); // forma via ajax pelo jquery
		}
	</script>
</body>
</html>
   ```
   
   
