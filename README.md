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
