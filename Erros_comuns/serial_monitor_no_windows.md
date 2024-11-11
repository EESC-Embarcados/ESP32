# Corrigindo Caracteres Aleatórios no Monitor Serial da ESP32

Se você está enfrentando problemas com caracteres aleatórios e desconhecidos sendo exibidos no monitor serial da ESP32 no Windows, isso pode estar relacionado à configuração da velocidade de comunicação (baud rate) e ao modo de flash utilizado. Para corrigir esse problema, adicione as seguintes linhas no arquivo `platformio.ini` do seu projeto:

## Passos

1. **Abra o arquivo `platformio.ini`**: Este arquivo está localizado no diretório raiz do seu projeto.

2. **Adicione as seguintes linhas** ao arquivo `platformio.ini`:

   ```ini
   board_build.flash_mode = qio
   upload_speed = 115200
   monitor_speed = 115200
