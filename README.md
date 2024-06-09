<!DOCTYPE html>
<html lang="en">
<head>
    
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <script>
        //karol romero caballero, karla fuentes blanca
        var minuscula=false, mayuscula=false, numero=false, password;

        while(true){
            password=prompt("Ingresa una contraseña");

            if(password.split(" ").length < 3){
                alert("Tu password debe contener 3 palabras :)");
                continue;
            }
            if(password.length < 10 || password.length > 20){
                alert("Tu password debe tener entre 10 y 20 caracteres");
                continue;
            }

            for(var k=0;k<password.length;k++) {
                if(password[k]>='a'&&password[k]<='z'){
                    minuscula=true;
                }
                if(password[k]>='A'&& password[k]<='Z'){
                    mayuscula=true;
                }
                if(password[k]>='0'&&password[k]<='9') {
                    numero=true;
                }
            }
            if(!minuscula){
                alert("Tu contraseña debe tener una letra minuscula");
                continue;
            }
            if(!mayuscula){
                alert("Tu contraseña debe tener una letra mayuscula");
                continue;
            }
            if(!numero){
                alert("Tu contraseña debe tener un numero");
                continue;
            }
            if(!/[!@#$%^&*()_+\-=\[\]{};':"\\|,.<>\/?]+/.test(password)){
                alert("Tu contraseña debe contener al menos un caracter especial");
                continue;
            }
            if(/(.)\1+/.test(password)){
                alert("Tu contraseña no debe contener caracteres repetidos");
                continue;
            }
            alert("Tu contraseña es valida!!! :)");
            break;
        }
    </script>
</body>
</html>

