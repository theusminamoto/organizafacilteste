<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>OrganizaFácil - Protótipo</title>
    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background-color: #F5F5F5;
        }
        .screen {
            width: 375px;
            height: 812px;
            margin: 20px auto;
            background-color: #F5F5F5;
            border: 1px solid #CCCCCC;
            overflow: hidden;
            position: relative;
            display: none;
        }
        .screen.active {
            display: block;
        }
        .header {
            height: 50px;
            background-color: #333333;
            color: #FFFFFF;
            display: flex;
            align-items: center;
            padding: 0 10px;
        }
        .header .icon {
            width: 24px;
            height: 24px;
            background-color: #FFFFFF;
            margin-right: 10px;
        }
        .header .title {
            font-size: 18px;
        }
        .content {
            padding: 20px;
        }
        #login .content {
            padding-top: 50px;
        }
        .input {
            width: 300px;
            height: 40px;
            border: 1px solid #CCCCCC;
            padding: 10px;
            margin-bottom: 20px;
            font-size: 16px;
            color: #333333;
        }
        .textarea {
            height: 100px;
        }
        .button {
            width: 300px;
            height: 50px;
            background-color: #666666;
            color: #FFFFFF;
            border: none;
            font-size: 16px;
            cursor: pointer;
            display: block;
            margin: 20px auto;
            text-align: center;
            line-height: 50px;
            text-decoration: none;
        }
        .small-button {
            width: 150px;
            height: 40px;
            background-color: transparent;
            border: 1px solid #CCCCCC;
            color: #333333;
            line-height: 40px;
        }
        .task {
            width: 350px;
            height: 70px;
            border: 1px solid #CCCCCC;
            padding: 10px;
            margin-bottom: 10px;
            font-size: 16px;
            color: #333333;
        }
        .calendar {
            display: grid;
            grid-template-columns: repeat(7, 50px);
            gap: 5px;
        }
        .calendar div {
            width: 50px;
            height: 50px;
            border: 1px solid #CCCCCC;
            text-align: center;
            line-height: 50px;
            font-size: 14px;
            color: #333333;
        }
        .calendar .today {
            background-color: #999999;
        }
        .nav-bar {
            position: absolute;
            bottom: 0;
            width: 375px;
            height: 50px;
            background-color: #333333;
            display: flex;
            justify-content: space-around;
            align-items: center;
        }
        .nav-bar .icon {
            width: 24px;
            height: 24px;
            background-color: #FFFFFF;
        }
        .menu {
            position: fixed;
            top: 0;
            width: 100%;
            background-color: #333333;
            padding: 10px;
            text-align: center;
        }
        .menu a {
            color: #FFFFFF;
            margin: 0 10px;
            text-decoration: none;
            font-size: 14px;
        }
        .logo {
            font-size: 24px;
            color: #333333;
            text-align: center;
            margin: 50px 0;
        }
        .link {
            font-size: 14px;
            color: #666666;
            text-decoration: underline;
            text-align: center;
            display: block;
            margin-top: 20px;
        }
        .profile-pic {
            width: 100px;
            height: 100px;
            border-radius: 50%;
            border: 1px solid #CCCCCC;
            background-color: #CCCCCC;
            margin: 20px auto;
            display: block;
        }
    </style>
</head>
<body>
    <div class="menu">
        <a href="#login">Login</a>
        <a href="#dashboard">Dashboard</a>
        <a href="#task-list">Lista de Tarefas</a>
        <a href="#add-task">Adicionar Tarefa</a>
        <a href="#task-details">Detalhes da Tarefa</a>
        <a href="#profile">Perfil</a>
    </div>

    <div id="login" class="screen active">
        <div class="logo">OrganizaFácil</div>
        <div class="content">
            <input type="text" class="input" placeholder="E-mail">
            <input type="password" class="input" placeholder="Senha">
            <a href="#dashboard" class="button">Entrar</a>
            <a href="#" class="link">Esqueceu a senha?</a>
        </div>
    </div>

    <div id="dashboard" class="screen">
        <div class="header">
            <div class="icon"></div>
            <span class="title">OrganizaFácil</span>
        </div>
        <div class="content">
            <h3>Tarefas Hoje</h3>
            <div class="task">Tarefa 1 - 23/06/2025</div>
            <div class="task">Tarefa 2 - 24/06/2025</div>
            <h3>Calendário</h3>
            <div class="calendar">
                <div>1</div><div>2</div><div>3</div><div>4</div><div>5</div><div>6</div><div>7</div>
                <div>8</div><div>9</div><div>10</div><div>11</div><div>12</div><div>13</div><div>14</div>
                <div>15</div><div>16</div><div>17</div><div>18</div><div>19</div><div>20</div><div>21</div>
                <div>22</div><div class="today">23</div><div>24</div><div>25</div><div>26</div><div>27</div><div>28</div>
                <div>29</div><div>30</div><div></div><div></div><div></div><div></div><div></div>
            </div>
        </div>
        <div class="nav-bar">
            <a href="#profile"><div class="icon"></div></a>
            <a href="#task-list"><div class="icon"></div></a>
            <a href="#add-task"><div class="icon"></div></a>
        </div>
    </div>

    <div id="task-list" class="screen">
        <div class="header">
            <div class="icon"></div>
            <span class="title">OrganizaFácil</span>
        </div>
        <div class="content">
            <div style="display: flex; gap: 10px;">
                <a href="#" class="small-button">Por Disciplina</a>
                <a href="#" class="small-button">Por Prioridade</a>
            </div>
            <div class="task"><a href="#task-details" style="text-decoration: none; color: #333333;">Tarefa 1 - 23/06/2025 - Alta</a></div>
            <div class="task"><a href="#task-details" style="text-decoration: none; color: #333333;">Tarefa 2 - 24/06/2025 - Média</a></div>
            <div class="task"><a href="#task-details" style="text-decoration: none; color: #333333;">Tarefa 3 - 25/06/2025 - Baixa</a></div>
            <div class="task"><a href="#task-details" style="text-decoration: none; color: #333333;">Tarefa 4 - 26/06/2025 - Alta</a></div>
            <div class="task"><a href="#task-details" style="text-decoration: none; color: #333333;">Tarefa 5 - 27/06/2025 - Média</a></div>
        </div>
        <div class="nav-bar">
            <a href="#profile"><div class="icon"></div></a>
            <a href="#task-list"><div class="icon"></div></a>
            <a href="#add-task"><div class="icon"></div></a>
        </div>
    </div>

    <div id="add-task" class="screen">
        <div class="header">
            <a href="#dashboard"><div class="icon"></div></a>
            <span class="title">Nova Tarefa</span>
        </div>
        <div class="content">
            <input type="text" class="input" placeholder="Título">
            <textarea class="input textarea" placeholder="Descrição"></textarea>
            <input type="text" class="input" placeholder="Data (ex.: 23/06/2025)">
            <select class="input">
                <option>Alta</option>
                <option>Média</option>
                <option>Baixa</option>
            </select>
            <a href="#task-list" class="button">Salvar</a>
        </div>
    </div>

    <div id="task-details" class="screen">
        <div class="header">
            <a href="#task-list"><div class="icon"></div></a>
            <span class="title">Detalhes</span>
        </div>
        <div class="content">
            <h3>Tarefa 1</h3>
            <p style="font-size: 16px; color: #333333;">Descrição: Estudar para prova de UX Design.</p>
            <p style="font-size: 16px; color: #333333;">Data: 23/06/2025</p>
            <p style="font-size: 16px; color: #333333;">Prioridade: Alta</p>
            <a href="#add-task" class="small-button">Editar</a>
            <a href="#task-list" class="small-button">Excluir</a>
        </div>
        <div class="nav-bar">
            <a href="#profile"><div class="icon"></div></a>
            <a href="#task-list"><div class="icon"></div></a>
            <a href="#add-task"><div class="icon"></div></a>
        </div>
    </div>

    <div id="profile" class="screen">
        <div class="header">
            <div class="icon"></div>
            <span class="title">OrganizaFácil</span>
        </div>
        <div class="content">
            <div class="profile-pic"></div>
            <p style="font-size: 18px; color: #333333; text-align: center;">Matheus Minamoto</p>
            <p style="font-size: 16px; color: #333333; text-align: center;">matheus@example.com</p>
            <a href="#" class="button" style="background-color: transparent; border: 1px solid #CCCCCC; color: #333333;">Editar Perfil</a>
            <a href="#login" class="button" style="background-color: transparent; border: 1px solid #CCCCCC; color: #333333;">Sair</a>
        </div>
        <div class="nav-bar">
            <a href="#profile"><div class="icon"></div></a>
            <a href="#task-list"><div class="icon"></div></a>
            <a href="#add-task"><div class="icon"></div></a>
        </div>
    </div>

    <script>
        document.querySelectorAll('.menu a').forEach(link => {
            link.addEventListener('click', (e) => {
                document.querySelectorAll('.screen').forEach(screen => screen.classList.remove('active'));
                const target = e.target.getAttribute('href').substring(1);
                document.getElementById(target).classList.add('active');
            });
        });
    </script>
</body>
</html>
