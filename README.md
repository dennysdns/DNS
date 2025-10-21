# 📡 Solução Simples de Transferência de Arquivos via Wi-Fi (Web)

Este projeto oferece uma maneira super rápida de compartilhar arquivos da sua pasta atual (PC/Mac) para qualquer dispositivo na mesma rede Wi-Fi (como seu celular), usando apenas o seu navegador web.

A funcionalidade de servidor é criada usando um comando nativo do Python, transformando a pasta onde você estiver em um servidor HTTP temporário.

## 🚀 Como Usar (Requer Python 3 instalado)

1.  **Baixe ou Clone** este repositório para uma pasta no seu computador (PC ou Mac).
2.  **Mova/Copie** todos os arquivos que deseja compartilhar (fotos, vídeos, documentos) para dentro desta mesma pasta.
3.  **Abra o Terminal** (ou Prompt de Comando/PowerShell) no seu computador.
4.  **Navegue** até a pasta que você criou/clonou (onde estão os arquivos).
    ```bash
    # Exemplo: Se a pasta estiver na Área de Trabalho
    cd ~/Desktop/NomeDaPasta
    ```
5.  **Inicie o Servidor:**
    Execute o seguinte comando para ativar o servidor na porta 8080:
    ```bash
    python3 -m http.server 8080
    ```
    *Se `python3` não funcionar, tente apenas `python`.*

6.  **Acesse no Outro Dispositivo (Celular/Outro PC):**
    * O terminal irá mostrar que o servidor está rodando em um endereço.
    * **Descubra o endereço IP local** do seu computador (o que está rodando o servidor).
    * No navegador do seu celular (ou outro dispositivo na mesma rede Wi-Fi), digite:
        ```
        http://[SEU_IP_LOCAL]:8080
        ```
    * Exemplo: Se o IP do seu computador for `192.168.1.10`, digite **`http://192.168.1.10:8080`**.

    Você verá a interface HTML para download dos seus arquivos!

## 💡 Para Encerrar

Para desligar o servidor e interromper o compartilhamento, volte ao Terminal e pressione **`Ctrl + C`**.

---

## 💻 Arquivo 2: `index.html` (Interface Web)

Este arquivo é a interface que aparecerá no navegador do seu celular quando você acessar o endereço IP.

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Servidor Wi-Fi Local de Arquivos</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 20px;
            background-color: #f4f4f9;
            color: #333;
            text-align: center;
        }
        .container {
            max-width: 600px;
            margin: 0 auto;
            background-color: #ffffff;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        }
        h1 {
            color: #4a90e2;
            border-bottom: 2px solid #4a90e2;
            padding-bottom: 10px;
            margin-bottom: 20px;
        }
        .info-box {
            background-color: #e6f0ff;
            border: 1px solid #cce0ff;
            padding: 15px;
            border-radius: 8px;
            margin-bottom: 25px;
        }
        .info-box p {
            margin: 5px 0;
            font-size: 1.1em;
            font-weight: bold;
        }
        /* Estilização para a lista de arquivos padrão do Python */
        pre {
            text-align: left;
            padding: 15px;
            border: 1px solid #ddd;
            background-color: #f9f9f9;
            border-radius: 5px;
        }
        pre a {
            color: #4a90e2;
            text-decoration: none;
            display: block;
            padding: 5px 0;
        }
        pre a:hover {
            text-decoration: underline;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Servidor de Arquivos Wi-Fi Local</h1>
        
        <div class="info-box">
            <p>Seu Computador está Ativo como Servidor de Download.</p>
            <p>Acesse pelo seu navegador:</p>
            <p style="color: #d9534f; font-size: 1.5em; margin-top: 10px;">http://[SEU IP LOCAL]:8080</p>
        </div>

        <h2>Arquivos Disponíveis para Download</h2>
        <p>Abaixo estão os arquivos da pasta atual do seu computador. Clique para baixar.</p>
        
        <p>*(Esta mensagem é uma simulação. O servidor Python exibirá a lista real de arquivos.)*</p>

    </div>
</body>
</html>
