# to-do-app
Desafio de criação de agenda de tarefas

<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Closet Chromatic | Gestão de Organização</title>
    <style>
        :root {
            /* Paleta de Cores com Contraste Acessível */
            --primary-dark: #1a252f;
            --accent-blue: #2980b9;
            --bg-light: #f8f9fa;
            --text-main: #212529;
            --border-color: #dee2e6;
        }

        body {
            font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
            background-color: var(--bg-light);
            color: var(--text-main);
            margin: 0;
            padding: 2rem;
            display: flex;
            justify-content: center;
        }

        .dashboard {
            max-width: 900px;
            width: 100%;
            background: #ffffff;
            padding: 2.5rem;
            border-radius: 16px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.08);
        }

        .header {
            text-align: center;
            margin-bottom: 2rem;
            border-bottom: 3px solid var(--accent-blue);
        }

        /* Melhoria na organização do Checklist */
        .checklist {
            border: none;
            padding: 0;
            margin: 2rem 0;
        }

        .checklist__legend {
            font-size: 1.5rem;
            font-weight: bold;
            margin-bottom: 1rem;
            color: var(--primary-dark);
        }

        .checklist__item {
            display: flex;
            align-items: center;
            padding: 0.8rem;
            border-radius: 8px;
            transition: background 0.3s;
        }

        .checklist__item:hover {
            background-color: #f1faff;
        }

        .checklist__input {
            width: 20px;
            height: 20px;
            cursor: pointer;
            margin-right: 12px;
        }

        .checklist__label {
            cursor: pointer;
            font-size: 1.1rem;
        }

        /* Tabela Acessível */
        .inventory-table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 1.5rem;
        }

        .inventory-table th {
            background-color: var(--primary-dark);
            color: white;
            padding: 15px;
            text-align: left;
        }

        .inventory-table td {
            padding: 12px;
            border-bottom: 1px solid var(--border-color);
        }

        /* Grid de Cores com foco em contraste */
        .color-guide {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 1rem;
            margin: 2rem 0;
        }

        .color-swatch {
            padding: 1rem;
            border-radius: 8px;
            text-align: center;
            font-weight: 600;
            /* Garante que o texto seja legível independente da cor de fundo */
            outline: 1px solid rgba(0,0,0,0.1);
        }

        .text--white { color: #fff; text-shadow: 0 1px 2px #000; }
        .text--dark { color: #000; }

        @media (max-width: 600px) {
            body { padding: 10px; }
            .dashboard { padding: 1.5rem; }
        }
    </style>
</head>
<body>

    <main class="dashboard" role="main">
        <header class="header">
            <h1>Agenda Closet Chromatic</h1>
            <p>Sistema de organização visual e rotina têxtil</p>
        </header>

        <section aria-labelledby="workflow-title">
            <fieldset class="checklist">
                <legend id="workflow-title" class="checklist__legend">🚀 Fluxo de Trabalho Operacional</legend>
                
                <div class="checklist__item">
                    <input type="checkbox" id="step1" class="checklist__input">
                    <label for="step1" class="checklist__label">Higienização e esvaziamento total do espaço.</label>
                </div>

                <div class="checklist__item">
                    <input type="checkbox" id="step2" class="checklist__input">
                    <label for="step2" class="checklist__label">Triagem: Manter, Doar ou Consertar.</label>
                </div>

                <div class="checklist__item">
                    <input type="checkbox" id="step3" class="checklist__input">
                    <label for="step3" class="checklist__label">Agrupamento por matiz (Círculo Cromático).</label>
                </div>
            </fieldset>
        </section>

        <section>
            <h3>🌈 Guia de Referência de Matizes</h3>
            <div class="color-guide">
                <div class="color-swatch text--white" style="background-color: #d32f2f;">Quentes / Intensos</div>
                <div class="color-swatch text--white" style="background-color: #1976d2;">Frios / Profundos</div>
                <div class="color-swatch text--dark" style="background-color: #f1c40f;">Alerta / Brilho</div>
                <div class="color-swatch text--dark" style="background-color: #ecf0f1;">Neutros Claros</div>
            </div>
        </section>

        <section>
            <h3>📊 Status do Inventário</h3>
            <table class="inventory-table">
                <caption>Resumo da organização atual por categoria de cor</caption>
                <thead>
                    <tr>
                        <th scope="col">Grupo Cromático</th>
                        <th scope="col">Progresso</th>
                        <th scope="col">Volume</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>Escala de Cinza & Preto</td>
                        <td>✅ Finalizado</td>
                        <td>25 itens</td>
                    </tr>
                    <tr>
                        <td>Tons de Terra & Bege</td>
                        <td>⏳ Organizando</td>
                        <td>10 itens</td>
                    </tr>
                </tbody>
            </table>
        </section>
    </main>

</body>
</html>
