# RetoMasterSeman4
Nuestro servicio identifica trabajos informales, formales y temas relacionados a la contingencia COVID 19
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="style.css"
    <title>RETO MASTER</title>
</head>
<body>
    <h1 id="titulo" class="titulo-class">COVIDSOLUTIONS</h1>
    <p id="instrucciones" style="border: 2px solid blue;">
        Ingresa la URL de una imagen para identificarla
    </p>
    <form id="MyForm">
        <input id="url" type="url" placeholder="URL de la imagen" >
        <input type="button"onclick="senToApi()">Enviar</button>
    </form>
</body>
</html>

<script src="https://ajax.googleapis.com/ajax/libs/jquery/2.2.4/jquery.min.js"></script>

<script>
    function senToApi() {
            const url = document.getElementByIde("url").value;
            if (url !="") {
                $.ajax
                    async:true,
                    type:"POST",
                    dataType:"html",
                    contentType:"application/www-form-urlencoded",
                    headers: {
                        "PredictionKey":"xxxxxxxxxxxxxxxxxxxxxxxxxx"
                    }
                    data:"Url:https://lasillarotarm.blob.core.windows.net/images/2018/06/11/cdmxtrabajoinfantil.jpg"
                    url:"https://southcentralus.api.cognitive.microsoft.com/customvision/v3.0/Prediction/04cd3932-dd64-4131-b0d8-560168f78931/classify/iterations/COVIDSOLUTIONS/url",
                    success : function(data){
                        console.log(data):

                    }
                },
                    timeout:10000
                    )
    
            }
    }
</script>
