# VETORES
Estrutura de um ARRAY
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <h1>Aula de Arrays</h1>
    <hr>
    <h3>Lista de batatas</h3>
    <label for="txt">Digite o produto</label>
    <input type="text" id="txt" placeholder="Ex: Ruffles">
    <button onclick="add()">Adicionar</button>
    <button onclick="remove()">Remover</button>

    <P id="lista"></P>

    <script src="scritpt.js"></script>
</body>
</html>



//////////////////////////////////////////////////////////


let batatas = [];
function add(){
    let produto = document.getElementById("txt").value;
    let posicao = batatas.indexOf(produto);
    if (posicao == -1){
    batatas.push (produto);
    document.getElementById("lista").innerHTML = batatas;
} else {
    alert ("Este produto já está cadastrado!");
}
}
function remove(){
    let produto = document.getElementById("txt").value;
    let posicao = batatas.indexOf(produto);
    if (posicao == -1){
    alert ("Não foi encontrado produto com o nome: " + produto);
    } 
    else{
    batatas.splice(posicao, 1);
    document.getElementById("lista").innerHTML = batatas;
    }
}
