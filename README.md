# python-notfy
System to display notifications on the Windows Linux and Mac screen,With sound icon

<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
        }
        h1, h2, h3 {
            color: #333;
        }
        pre {
            background-color: #f4f4f4;
            padding: 10px;
            border-left: 5px solid #2E2E2E;
            overflow: auto;
        }
        .code {
            color: #005cbf;
            font-weight: bold;
        }
        .description {
            margin-bottom: 20px;
        }
        .function {
            background-color: #f0f0f0;
            padding: 15px;
            border-radius: 5px;
            margin-bottom: 20px;
        }
    </style>
</head>
<body>

    <h1>Documentação da Biblioteca de Notificações</h1>
    <p>Esta biblioteca fornece funcionalidades para exibir notificações visuais no canto da tela com um ícone, uma mensagem e um som opcional.</p>

    <h2>Variáveis Globais</h2>
    <div class="description">
        <p>As variáveis globais configuram as propriedades da notificação:</p>
        <ul>
            <li><span class="code">time</span>: Tempo em milissegundos antes de a notificação ser fechada automaticamente. Valor padrão: 4444.</li>
            <li><span class="code">posicao</span>: Define a posição da notificação na tela. Valor padrão: <code>"topo_esquerda"</code>.</li>
            <li><span class="code">back_color</span>: Cor de fundo da notificação. Valor padrão: <code>"#2E2E2E"</code>.</li>
            <li><span class="code">text_color</span>: Cor do texto da notificação. Valor padrão: <code>"white"</code>.</li>
        </ul>
    </div>

    <h2>Funções</h2>

    <div class="function">
        <h3>sets</h3>
        <p><strong>Descrição:</strong> Função para configurar as variáveis globais da biblioteca.</p>
        <p><strong>Parâmetros:</strong></p>
        <ul>
            <li><span class="code">novo_time</span> (opcional): Novo valor para o tempo de exibição em milissegundos (padrão: 3000).</li>
            <li><span class="code">nova_posicao</span> (opcional): Nova posição para a notificação. Opções: <code>"topo_esquerda"</code>, <code>"topo_direita"</code>, <code>"base_esquerda"</code>, <code>"base_direita"</code>, ou <code>"centro"</code>.</li>
            <li><span class="code">nova_back_color</span> (opcional): Cor de fundo da notificação (padrão: "#2E2E2E").</li>
            <li><span class="code">nova_text_color</span> (opcional): Cor do texto da notificação (padrão: "white").</li>
        </ul>
        <p><strong>Exemplo de uso:</strong></p>
        <pre>sets(novo_time=5000, nova_posicao="topo_direita", nova_back_color="#000000", nova_text_color="yellow")</pre>
    </div>

    <div class="function">
        <h3>notfy</h3>
        <p><strong>Descrição:</strong> Exibe uma notificação com uma mensagem, ícone e, opcionalmente, um som.</p>
        <p><strong>Parâmetros:</strong></p>
        <ul>
            <li><span class="code">mensagem</span>: Texto a ser exibido na notificação.</li>
            <li><span class="code">icona</span>: Caminho para a imagem do ícone a ser exibido.</li>
            <li><span class="code">sond</span> (opcional): Caminho para o arquivo de som a ser reproduzido durante a notificação.</li>
        </ul>
        <p><strong>Descrição adicional:</strong> A função exibe uma janela personalizada no canto da tela conforme a posição definida na variável <code>posicao</code>. Caso um som seja fornecido, ele será reproduzido se o arquivo estiver disponível.</p>
        <p><strong>Exemplo de uso:</strong></p>
        <pre>notfy("Bem-vindo!", "icone.png", "som.mp3")</pre>
    </div>

    <h2>Dependências</h2>
    <p>A biblioteca requer os seguintes pacotes:</p>
    <ul>
        <li><span class="code">tkinter</span>: Biblioteca padrão do Python para criar interfaces gráficas.</li>
        <li><span class="code">PIL (Pillow)</span>: Usada para carregar e manipular imagens.</li>
        <li><span class="code">pygame</span>: Usada para reproduzir o som na notificação.</li>
    </ul>

    <h2>Exemplo de Uso Completo</h2>
    <pre>
from PIL import Image, ImageTk
import tkinter as tk
import pygame

# Configurações da notificação
sets(novo_time=5000, nova_posicao="topo_direita", nova_back_color="#4E4E4E", nova_text_color="yellow")

# Exibe a notificação
notfy("Sua operação foi bem-sucedida!", "caminho/para/icone.png", "caminho/para/som.mp3")
    </pre>
</body>
</html>
