<!DOCTYPE html>
<html lang="hu">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="feladat2.css">
    <script src="feladat2.js"></script>
    <title>Form</title>
</head>
<body>
    <h2>Megadható adatok</h2>

    <form id="forma">
        <label for="vnev">Vezetéknév</label>
        <input type="text" id="veznev" name="vezetéknév" size="40" placeholder="vezetéknév" > <br>

        <label for="knev">Keresztknév</label>
        <input type="text" id="knev" name="keresztknév" size="40" placeholder="keresztnévnév" ><br>

        <label for="szam">Kedvenc szám</label>
        <input type="text" id="szam" name="kedvenc_szám" size="40" placeholder="Kedvenc szám" > <br>
    </form>

    <label for="jogositvany">Van jogosítványod?</label>
    <input type="checkbox" id="jogositvany" name="jogositvany"><br>

    <label for="van">Jogosítvánnyal rendelkező ember</label>
    <button type="button" id="van" onclick="vanjogsi()">Mutasd</button><br>

    <label for="van">Jogosítvánnyal nem rendelkező ember</label>
    <button type="button" id="nincs" onclick="nincsjogsi()">Mutasd</button><br>

</body>
</html>

let adatok = [];

const adat = {
    vezetek : veznev,
    kereszt : knev,
    szamod : szam,
    jogosit : jogsi
}

function hozzaadAdat() {
    const vezetek = document.getElementById("veznev").value;
    const kereszt = document.getElementById("knev").value;
    const szamod = document.getElementById("szam").value;
    const jogosit = document.getElementById("jogositvany").checked;

    let adatok1 = [vezetek,kereszt,szamod,jogosit];
    console.log(adatok1);
}

adatok.push(adat);
console.log(adatok);

function vanjogsi(){
    var elso = document.getElementById('van').value;
    let egy= [elso];
    console.log(egy);
}

function nincsjogsi(){
    var masodik = document.getElementById('nincs').value;
    let ketto = [masodik];
    console.log(ketto);
}
