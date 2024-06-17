<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Coffee Shop Menu</title>
    <style>
        body {
    font-family: Arial, sans-serif;
    background-color: #f4f4f4;
    margin: 0;
    padding: 0;
}

header {
    background-color: #333;
    color: #fff;
    padding: 1em 0;
    text-align: center;
}

main {
    padding: 2em;
}

#menu {
    margin-bottom: 2em;
}

.menu-item {
    background-color: #fff;
    border: 1px solid #ddd;
    padding: 1em;
    margin-bottom: 1em;
    border-radius: 5px;
}

.menu-item h3 {
    margin-top: 0;
}

button {
    background-color: #333;
    color: #fff;
    border: none;
    padding: 0.5em 1em;
    cursor: pointer;
    border-radius: 5px;
}

button:hover {
    background-color: #555;
}

#order {
    background-color: #fff;
    padding: 1em;
    border: 1px solid #ddd;
    border-radius: 5px;
}

#order h2 {
    margin-top: 0;
}

    </style>
    <script>
        function customizeOrder(item) {
    let customization = prompt(`Customize your ${item}. Please specify any additions or changes:`);
    addToOrder(item, customization);
}

function addToOrder(item, customization) {
    let orderDetails = document.getElementById('order-details');
    let orderItem = document.createElement('div');
    orderItem.className = 'order-item';
    orderItem.innerHTML = `<strong>${item}</strong>: ${customization}`;
    orderDetails.appendChild(orderItem);
}

    </script>
</head>
<body>
    <header>
        <h1>Welcome to Our Coffee Shop</h1>
    </header>
    <main>
        <section id="menu">
            <h2>Menu</h2>
            <div class="menu-item">
                <h3>Espresso</h3>
                <p>A strong and bold coffee, perfect for a quick boost.</p>
                <button onclick="customizeOrder('Espresso')">Customize</button>
            </div>
            <div class="menu-item">
                <h3>Latte</h3>
                <p>A smooth blend of espresso and steamed milk.</p>
                <button onclick="customizeOrder('Latte')">Customize</button>
            </div>
            <div class="menu-item">
                <h3>Cappuccino</h3>
                <p>A rich and creamy coffee with a frothy top.</p>
                <button onclick="customizeOrder('Cappuccino')">Customize</button>
            </div>
            <div class="menu-item">
                <h3>Mocha</h3>
                <p>A delightful mix of espresso, chocolate, and steamed milk.</p>
                <button onclick="customizeOrder('Mocha')">Customize</button>
            </div>
        </section>
        <section id="order">
            <h2>Your Order</h2>
            <div id="order-details"></div>
        </section>
    </main>
    <script src="script.js"></script>
</body>
</html>
