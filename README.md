# flexible-lay-out
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Flexbox Demo</title>
    <style>
        :root {
            --primary-color: #2a9d8f;
            --secondary-color: #e9c46a;
            --accent-color: #f4a261;
            --dark-color: #264653;
            --light-color: #f8f9fa;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', sans-serif;
            line-height: 1.6;
            background-color: var(--light-color);
        }

        .header {
            background-color: var(--dark-color);
            color: white;
            padding: 2rem;
            text-align: center;
        }

        .flex-container {
            display: flex;
            flex-wrap: wrap;
            gap: 1.5rem;
            padding: 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .flex-item {
            flex: 1 1 300px;
            background: white;
            padding: 1.5rem;
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            transition: transform 0.3s ease;
        }

        .flex-item:hover {
            transform: translateY(-5px);
        }

        .showcase-section {
            margin: 2rem 0;
            padding: 2rem;
            background: white;
        }

        .flex-row {
            display: flex;
            gap: 1rem;
            margin-bottom: 1rem;
        }

        .flex-column {
            display: flex;
            flex-direction: column;
            gap: 1rem;
        }

        .demo-item {
            padding: 1rem;
            background: var(--primary-color);
            color: white;
            border-radius: 4px;
            text-align: center;
            flex: 1;
        }

        .space-between {
            justify-content: space-between;
        }

        .center {
            justify-content: center;
            align-items: center;
        }

        .grow-2 {
            flex-grow: 2;
            background: var(--secondary-color);
        }

        .grow-3 {
            flex-grow: 3;
            background: var(--accent-color);
        }

        @media (max-width: 768px) {
            .flex-row {
                flex-direction: column;
            }

            .flex-item {
                flex: 1 1 100%;
            }
        }

        .section-title {
            color: var(--dark-color);
            margin-bottom: 1rem;
            font-size: 1.5rem;
        }

        .description {
            color: #666;
            margin-bottom: 1rem;
        }
    </style>
</head>
<body>
    <header class="header">
        <h1>CSS Flexbox Showcase</h1>
        <p>Exploring flexible box layout system</p>
    </header>

    <main>
        <div class="flex-container">
            <div class="flex-item">
                <h2 class="section-title">Basic Flex Container</h2>
                <p class="description">Default flex behavior with equal width items</p>
                <div class="flex-row">
                    <div class="demo-item">1</div>
                    <div class="demo-item">2</div>
                    <div class="demo-item">3</div>
                </div>
            </div>

            <div class="flex-item">
                <h2 class="section-title">Flex Grow</h2>
                <p class="description">Items with different flex-grow values</p>
                <div class="flex-row">
                    <div class="demo-item">1</div>
                    <div class="demo-item grow-2">2</div>
                    <div class="demo-item grow-3">3</div>
                </div>
            </div>

            <div class="flex-item">
                <h2 class="section-title">Space Between</h2>
                <p class="description">Using justify-content: space-between</p>
                <div class="flex-row space-between">
                    <div class="demo-item">Left</div>
                    <div class="demo-item">Center</div>
                    <div class="demo-item">Right</div>
                </div>
            </div>

            <div class="flex-item">
                <h2 class="section-title">Flex Column</h2>
                <p class="description">Vertical flex layout</p>
                <div class="flex-column">
                    <div class="demo-item">Top</div>
                    <div class="demo-item">Middle</div>
                    <div class="demo-item">Bottom</div>
                </div>
            </div>
        </div>
    </main>
</body>
</html>
