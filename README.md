<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Painel de Controle</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: Arial, sans-serif;
        }

        body {
            display: grid;
            grid-template-columns: 250px 1fr;
            grid-template-rows: 60px 1fr;
            grid-template-areas: "sidebar header" "sidebar main";
            height: 100vh;
            background: #f4f4f4;
        }

        .sidebar {
            grid-area: sidebar;
            background: #333;
            color: white;
            padding: 20px;
            display: flex;
            flex-direction: column;
        }

        .sidebar h2 {
            margin-bottom: 20px;
        }

        .sidebar a {
            color: white;
            text-decoration: none;
            margin: 10px 0;
            padding: 10px;
            display: block;
            border-radius: 5px;
            transition: background 0.3s;
        }

        .sidebar a:hover {
            background: #555;
        }

        .header {
            grid-area: header;
            background: #222;
            color: white;
            display: flex;
            align-items: center;
            padding: 0 20px;
        }

        .main-content {
            grid-area: main;
            padding: 20px;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
        }

        .card {
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s;
        }

        .card:hover {
            transform: scale(1.05);
        }

        @media (max-width: 768px) {
            body {
                grid-template-columns: 1fr;
                grid-template-rows: 60px auto 1fr;
                grid-template-areas: "header" "sidebar" "main";
            }
            .sidebar {
                flex-direction: row;
                overflow-x: auto;
                white-space: nowrap;
            }
            .sidebar a {
                display: inline-block;
                margin-right: 10px;
            }
        }
    </style>
</head>
<body>
    <div class="sidebar">
        <h2>Painel</h2>
        <a href="#">Dashboard</a>
        <a href="#">Relatórios</a>
        <a href="#">Usuários</a>
        <a href="#">Configurações</a>
    </div>
    <div class="header">
        <h1>Painel de Controle</h1>
    </div>
    <div class="main-content">
        <div class="card">Métricas 1</div>
        <div class="card">Métricas 2</div>
        <div class="card">Métricas 3</div>
        <div class="card">Métricas 4</div>
    </div>
</body>
</html>
