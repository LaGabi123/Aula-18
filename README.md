# Aula-18
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script type="text/javascript">
        function verifica() {
            if (document.forms[0].email.value.length == 0) {
                alert('Por favor, informe o seu EMAIL.');
                //document.frmEnvia.email.focus();
                return false;
            }

        }

        function checarEmail() {
            if (document.forms[0].email.value == ""
                || document.forms[0].email.value.indexOf('@') == -1
                || document.forms[0].email.value.indexOf('.') == -1) {
                alert("Por favor, informe um E-MAIL válido!");
                return false;
            }
        }

        verifica()
        checarEmail()
    </script>
</head>

<body>
    <form method="post" action="" onSubmit="return ( verifica() )" name="frmEnvia">
        <label for="email">E-mail: </label>
        <input name="email" type="text" class="input" id="email" onblur="checarEmail();" />
        <input name="submit" type="submit" value=" ENVIAR " />
    </form>
</body>

</html>
