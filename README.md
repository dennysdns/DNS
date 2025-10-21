# Simple Wi-Fi File Server (Servidor Simples de Arquivos via Wi-Fi)

Este repositório contém o código e as instruções para iniciar um servidor web **temporário e local** em seu computador (PC ou Mac) usando Python, permitindo o download de arquivos via Wi-Fi.

**ATENÇÃO:** Este servidor é **apenas para redes locais (Wi-Fi)** e é recomendado usá-lo apenas para compartilhar arquivos entre seus próprios dispositivos na mesma rede.

## 🚀 Como Usar (Requer Python 3 instalado)

1.  **Abra o Terminal** (ou Prompt de Comando).
2.  **Navegue até a Pasta** que contém os arquivos que você deseja compartilhar (ex: sua pasta de Downloads, ou a pasta que contém este `README.md`).
3.  **Inicie o Servidor:**
    ```bash
    python3 -m http.server 8080
    ```
    *Se `python3` não funcionar, tente apenas `python`.*
4.  **Verifique o Endereço IP:** O terminal exibirá uma mensagem como: `Serving HTTP on 0.0.0.0 port 8080 (http://0.0.0.0:8080/) ...`
5.  **Acesse no Outro Dispositivo (Celular/Outro PC):**
    * Descubra o **endereço IP local** do seu computador (o que está rodando o servidor). Geralmente é algo como `192.168.1.xxx` ou `10.0.0.xxx`.
    * No navegador do seu celular (ou outro dispositivo), digite o endereço completo:
        ```
        http://[SEU_IP_LOCAL]:8080
        ```
    * Exemplo: `http://192.168.1.10:8080`

Agora você verá uma lista de todos os arquivos na pasta e poderá baixá-los.

## 💡 Para uma Interface Web Bonita (Opcional)

Se você colocar o arquivo `index.html` (o código que criei antes) na mesma pasta, o servidor Python o exibirá em vez da lista simples de arquivos.

## 🛑 Como Parar

Para desligar o servidor, volte ao Terminal e pressione **`Ctrl + C`**.
