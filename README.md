# Cle
Comparateur-prix
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Comparateur de Prix</title>
    <style>
        /* Style global pour la page */
        body {
            font-family: 'Arial', sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 0;
            color: #333;
        }

        /* Container central du site */
        .container {
            max-width: 1000px;
            margin: 0 auto;
            padding: 20px;
        }

        /* Header */
        header {
            text-align: center;
            margin-bottom: 40px;
        }

        header h1 {
            font-size: 2.5em;
            color: #3498db;
        }

        header p {
            font-size: 1.1em;
            color: #555;
        }

        /* Section de recherche */
        .search-section {
            text-align: center;
            margin-bottom: 30px;
        }

        input {
            width: 80%;
            padding: 12px;
            font-size: 1.1em;
            border: 2px solid #ccc;
            border-radius: 4px;
            margin-top: 10px;
            box-sizing: border-box;
        }

        input:focus {
            border-color: #3498db;
            outline: none;
        }

        /* Section des produits comparés */
        .product-section {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            justify-content: space-around;
        }

        .product {
            background-color: white;
            border-radius: 5px;
            padding: 20px;
            width: 280px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
            transition: transform 0.2s;
        }

        .product:hover {
            transform: scale(1.05);
        }

        .product h2 {
            font-size: 1.5em;
            color: #3498db;
        }

        .product p {
            font-size: 1em;
            color: #777;
        }

        .product ul {
            list-style-type: none;
            padding: 0;
        }

        .product li {
            padding: 8px 0;
        }

        .product a {
            color: #3498db;
            text-decoration: none;
        }

        .product a:hover {
            text-decoration: underline;
        }

        /* Section "Styles" */
        .styles-section {
            margin-top: 50px;
            padding: 20px;
            background-color: #f9f9f9;
            border-radius: 5px;
            text-align: center;
        }

        .styles-section h2 {
            font-size: 2em;
            color: #3498db;
        }

        .styles-section p {
            font-size: 1.1em;
            color: #555;
            max-width: 800px;
            margin: 0 auto;
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>Comparateur de Prix</h1>
            <p>Comparez les prix de différents produits en un seul endroit.</p>
        </header>

        <!-- Section de recherche de produit -->
        <section class="search-section">
            <input type="text" id="searchInput" placeholder="Rechercher un produit" oninput="filterProducts()">
        </section>

        <!-- Section des produits comparés -->
        <section class="product-section" id="productList">
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
        </section>

        <!-- Section Styles -->
        <section class="styles-section">
            <h2>Nos Styles</h2>
            <p>Nous avons conçu ce site pour qu'il soit facile à utiliser, avec une interface épurée et des couleurs modernes. Le design est responsive et s'adapte à toutes les tailles d'écran.</p>
        </section>

    </div>
    <script>
        function filterProducts() {
            const query = document.getElementById("searchInput").value.toLowerCase();
            const products = document.querySelectorAll(".product");

            products.forEach(product => {
                const name = product.getAttribute("data-name").toLowerCase();
                if (name.includes(query)) {
                    product.style.display = "";
                } else {
                    product.style.display = "none";
                }
            });
        }
    </script>
</body>
</html>
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Comparateur de Prix</title>
    <style>
        /* Style global pour la page */
        body {
            font-family: 'Arial', sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 0;
            color: #333;
        }

        /* Container central du site */
        .container {
            max-width: 1000px;
            margin: 0 auto;
            padding: 20px;
        }

        /* Header */
        header {
            text-align: center;
            margin-bottom: 40px;
        }

        header h1 {
            font-size: 2.5em;
            color: #3498db;
        }

        header p {
            font-size: 1.1em;
            color: #555;
        }

        /* Section de recherche */
        .search-section {
            text-align: center;
            margin-bottom: 30px;
        }

        input {
            width: 80%;
            padding: 12px;
            font-size: 1.1em;
            border: 2px solid #ccc;
            border-radius: 4px;
            margin-top: 10px;
            box-sizing: border-box;
        }

        input:focus {
            border-color: #3498db;
            outline: none;
        }

        /* Section des produits comparés */
        .product-section {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            justify-content: space-around;
        }

        .product {
            background-color: white;
            border-radius: 5px;
            padding: 20px;
            width: 280px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
            transition: transform 0.2s;
        }

        .product:hover {
            transform: scale(1.05);
        }

        .product h2 {
            font-size: 1.5em;
            color: #3498db;
        }

        .product p {
            font-size: 1em;
            color: #777;
        }

        .product ul {
            list-style-type: none;
            padding: 0;
        }

        .product li {
            padding: 8px 0;
        }

        .product a {
            color: #3498db;
            text-decoration: none;
        }

        .product a:hover {
            text-decoration: underline;
        }

        /* Section "Styles" */
        .styles-section {
            margin-top: 50px;
            padding: 20px;
            background-color: #f9f9f9;
            border-radius: 5px;
            text-align: center;
        }

        .styles-section h2 {
            font-size: 2em;
            color: #3498db;
        }

        .styles-section p {
            font-size: 1.1em;
            color: #555;
            max-width: 800px;
            margin: 0 auto;
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>Comparateur de Prix</h1>
            <p>Comparez les prix de différents produits en un seul endroit.</p>
        </header>

        <!-- Section de recherche de produit -->
        <section class="search-section">
            <input type="text" id="searchInput" placeholder="Rechercher un produit" oninput="filterProducts()">
        </section>

        <!-- Section des produits comparés -->
        <section class="product-section" id="productList">
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
        </section>

        <!-- Section Styles -->
        <section class="styles-section">
            <h2>Nos Styles</h2>
            <p>Nous avons conçu ce site pour qu'il soit facile à utiliser, avec une interface épurée et des couleurs modernes. Le design est responsive et s'adapte à toutes les tailles d'écran.</p>
        </section>

    </div>
    <script>
        function filterProducts() {
            const query = document.getElementById("searchInput").value.toLowerCase();
            const products = document.querySelectorAll(".product");

            products.forEach(product => {
                const name = product.getAttribute("data-name").toLowerCase();
                if (name.includes(query)) {
                    product.style.display = "";
                } else {
                    product.style.display = "none";
                }
            });
        }
    </script>
</body>
</html>
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Comparateur de Prix</title>
    <style>
        /* Style global pour la page */
        body {
            font-family: 'Arial', sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 0;
            color: #333;
        }

        /* Container central du site */
        .container {
            max-width: 1000px;
            margin: 0 auto;
            padding: 20px;
        }

        /* Header */
        header {
            text-align: center;
            margin-bottom: 40px;
        }

        header h1 {
            font-size: 2.5em;
            color: #3498db;
        }

        header p {
            font-size: 1.1em;
            color: #555;
        }

        /* Section de recherche */
        .search-section {
            text-align: center;
            margin-bottom: 30px;
        }

        input {
            width: 80%;
            padding: 12px;
            font-size: 1.1em;
            border: 2px solid #ccc;
            border-radius: 4px;
            margin-top: 10px;
            box-sizing: border-box;
        }

        input:focus {
            border-color: #3498db;
            outline: none;
        }

        /* Section des produits comparés */
        .product-section {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            justify-content: space-around;
        }

        .product {
            background-color: white;
            border-radius: 5px;
            padding: 20px;
            width: 280px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
            transition: transform 0.2s;
        }

        .product:hover {
            transform: scale(1.05);
        }

        .product h2 {
            font-size: 1.5em;
            color: #3498db;
        }

        .product p {
            font-size: 1em;
            color: #777;
        }

        .product ul {
            list-style-type: none;
            padding: 0;
        }

        .product li {
            padding: 8px 0;
        }

        .product a {
            color: #3498db;
            text-decoration: none;
        }

        .product a:hover {
            text-decoration: underline;
        }

        /* Section "Styles" */
        .styles-section {
            margin-top: 50px;
            padding: 20px;
            background-color: #f9f9f9;
            border-radius: 5px;
            text-align: center;
        }

        .styles-section h2 {
            font-size: 2em;
            color: #3498db;
        }

        .styles-section p {
            font-size: 1.1em;
            color: #555;
            max-width: 800px;
            margin: 0 auto;
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>Comparateur de Prix</h1>
            <p>Comparez les prix de différents produits en un seul endroit.</p>
        </header>

        <!-- Section de recherche de produit -->
        <section class="search-section">
            <input type="text" id="searchInput" placeholder="Rechercher un produit" oninput="filterProducts()">
        </section>

        <!-- Section des produits comparés -->
        <section class="product-section" id="productList">
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
        </section>

        <!-- Section Styles -->
        <section class="styles-section">
            <h2>Nos Styles</h2>
            <p>Nous avons conçu ce site pour qu'il soit facile à utiliser, avec une interface épurée et des couleurs modernes. Le design est responsive et s'adapte à toutes les tailles d'écran.</p>
        </section>

    </div>
    <script>
        function filterProducts() {
            const query = document.getElementById("searchInput").value.toLowerCase();
            const products = document.querySelectorAll(".product");

            products.forEach(product => {
                const name = product.getAttribute("data-name").toLowerCase();
                if (name.includes(query)) {
                    product.style.display = "";
                } else {
                    product.style.display = "none";
                }
            });
        }
    </script>
</body>
</html>

