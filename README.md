# Cle
Comparateur-prix
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Comparateur de Prix</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="container">
        <h1>Comparateur de Prix</h1>
        <input type="text" id="searchInput" placeholder="Rechercher un produit" oninput="filterProducts()">
        <div id="productList">
            <!-- Liste des produits avec prix comparés -->
            <div class="product" data-name="Smartphone XYZ">
                <h2>Smartphone XYZ</h2>
                <p>Description du produit.</p>
                <ul>
                    <li>Amazon: 599€ <a href="https://www.amazon.com" target="_blank">Acheter</a></li>
                    <li>Cdiscount: 589€ <a href="https://www.cdiscount.com" target="_blank">Acheter</a></li>
                    <li>Fnac: 609€ <a href="https://www.fnac.com" target="_blank">Acheter</a></li>
                </ul>
            </div>
            <div class="product" data-name="Ordinateur ABC">
                <h2>Ordinateur ABC</h2>
                <p>Description du produit.</p>
                <ul>
                    <li>Amazon: 999€ <a href="https://www.amazon.com" target="_blank">Acheter</a></li>
                    <li>Cdiscount: 950€ <a href="https://www.cdiscount.com" target="_blank">Acheter</a></li>
                    <li>Fnac: 990€ <a href="https://www.fnac.com" target="_blank">Acheter</a></li>
                </ul>
            </div>
        </div>
    </div>
    <script src="script.js"></script>
</body>
</html>
