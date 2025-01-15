
# **ESP32 LED Control with OLED Display**

Este projeto utiliza o **ESP32** para controlar barras LED de 12V com ajuste de intensidade via PWM, exibindo os valores de brilho em um **display OLED**. O sistema é ideal para aplicações como iluminação ambiente, decoração ou aprendizado em IoT.

---

## **Características**
- Controle de até **3 barras LED de 12V** individualmente usando **MOSFETs**.
- Ajuste de intensidade de brilho com **PWM**.
- Monitoramento em tempo real do nível de brilho no **display OLED** (128x64, I2C).
- Código modular para fácil expansão e personalização.

---

## **Hardware Necessário**
1. **ESP32 Dev Module**
2. **Display OLED 128x64** (I2C, endereço padrão 0x3C)
3. **MOSFETs** (exemplo: IRLZ44N ou similar)
4. **Fonte de Alimentação 12V, 3A** (ou superior, conforme os LEDs utilizados)
5. **Barras LED de 12V**
6. **Resistores:**
   - 220Ω para o Gate do MOSFET
   - 10kΩ como pull-down
7. **Protoboard e Fios**

---

## **Esquema de Ligação**
### **Conexões do OLED:**
| OLED Pin | ESP32 Pin      |
|----------|----------------|
| VCC      | 3.3V           |
| GND      | GND            |
| SDA      | GPIO 21 (SDA)  |
| SCL      | GPIO 22 (SCL)  |

### **Conexões das Barras LED:**
- O **positivo das barras LED** conecta diretamente à fonte de 12V.
- O **negativo das barras LED** conecta ao **Drain** do MOSFET.
- O **Source do MOSFET** conecta ao GND.
- O **Gate do MOSFET** conecta a um GPIO do ESP32 (ex.: GPIO 18).

---

## **Software Necessário**
1. **Arduino IDE** (versão mais recente)
2. **Bibliotecas Arduino:**
   - [Adafruit SSD1306](https://github.com/adafruit/Adafruit_SSD1306)
   - [Adafruit GFX Library](https://github.com/adafruit/Adafruit-GFX-Library)

### **Instalando as Bibliotecas**
- Abra a Arduino IDE.
- Vá em **Ferramentas > Gerenciar Bibliotecas**.
- Pesquise por "Adafruit SSD1306" e "Adafruit GFX Library" e clique em **Instalar**.

---

## **Código**
### Exemplo Básico de Controle:
O código do projeto está disponível no arquivo principal do repositório. Ele inclui:
1. Inicialização do display OLED.
2. Controle de brilho com PWM.
3. Exibição do nível de brilho no display OLED.

---

## **Uso**
1. Monte o circuito conforme o esquema de ligação.
2. Carregue o código para o ESP32 usando a Arduino IDE.
3. Monitore o comportamento do LED e as informações no display OLED.
4. Use o Monitor Serial (115200) para depuração, se necessário.

---

## **Contribuições**
Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou enviar pull requests.

---

## **Licença**
Este projeto está licenciado sob a licença **MIT**. Consulte o arquivo [LICENSE](LICENSE) para mais detalhes.
