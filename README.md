# ODrive DFU

README.md in english: [README.en-us.md](https://github.com/achavevirou/odrive_dfu/blob/main/README.en-us.md)

A aplicação **ODrive DFU** é um simples utilitário que tem como objetivo **colocar a placa em MODO DFU (STM32 BOOTLOADER)**.  
Esta aplicação é gratuita e **não possui qualquer vínculo com a ODrive Robotics**.

![odrive_dfu_interface](https://github.com/achavevirou/odrive_dfu/blob/main/img/odrive_dfu_interface.png)

---

## ✅ Requisitos

Para se conectar à **ODrive | XDrive | Odesc**, é necessário que:

- A placa esteja com o firmware nativo (**ODrive 3.6 CDC Interface**);
- O driver da controladora seja o **WinUSB**.

---

## 🛠 Instalação do Driver com Zadig

1. Baixe o Zadig: [https://zadig.akeo.ie](https://zadig.akeo.ie)
2. Abra o Zadig e vá em `Options > List All Devices`.
3. Na lista de dispositivos, selecione `ODrive 3.6 CDC Interface (Interface 0)`.
4. Em `Driver`, verifique se o atual é **WinUSB**.
5. Se não for, selecione **WinUSB** e clique em **Install Driver** ou **Reinstall Driver**.
6. Repita para o dispositivo `ODrive 3.6 Native Interface (Interface 2)`.

---

## ▶️ Usando a aplicação

1. Faça o download do [ODrive DFU 1.0](https://github.com/achavevirou/odrive_dfu/releases) e execute.
2. Clique no botão **Conectar**.
3. Em seguida, clique no botão **Modo DFU**.
4. Se tudo estiver correto, a placa será desconectada e irá aparecer no Windows como **STM32 BOOTLOADER**, indicando que está pronta para carregamento de firmware.

---

## 🧩 Caso a placa não seja detectada como STM32 BOOTLOADER

- Acesse o **Gerenciador de Dispositivos**.
- Vá em `Exibir > Mostrar dispositivos ocultos`.
- Verifique em `Dispositivos de Barramento Serial Universal` se há dispositivos **STM32 BOOTLOADER** desconectados.
- **Se sim, desinstale todos eles**.
- Desconecte e reconecte a placa.
- Tente novamente o modo DFU via aplicação.

---

## ⚠️ Conflito com drivers Thrustmaster

Se você já instalou drivers de algum dispositivo **Thrustmaster**, pode haver conflitos.  
Siga o tutorial abaixo para **desinstalar os drivers Guillemot STM DFU**:

👉 [Desinstalar Guillemot STM DFU](https://support.pimax.com/en/support/solutions/articles/60000812307-failure-upgrade-blinking-led-)

---

## 💡 Erro com o driver do STM32 BOOTLOADER?

Basta instalar o **WinUSB** usando novamente o Zadig como descrito acima.

---

## 🔌 Último recurso: ST Link

Se nenhum método funcionar, utilize um **ST Link** para carregar o firmware na **ODrive | XDrive | Odesc**.

> ⚠️ Cuidado: nem todos os ST Links vendidos funcionam corretamente.  
> Dê preferência aos que usam **chip original**.

### Esquema de ligação:

> A alimentação da placa XDrive Mini deve ser feita com fonte **DC entre 12V e 56V**. Se a placa for Odesc, fique atento a tensão limite (**24V ou 56V a depender da versão**).

![Esquema ST Link e XDrive](https://github.com/achavevirou/odrive_dfu/blob/main/img/stlink_xdrive_odrive_odesc.jpg)

### Programação:

- Use o **STM32 ST-LINK Utility** para carregar arquivos `.bin` ou `.hex`.
- Use o **STM32CubeProgrammer** para carregar arquivos `.elf`, `.bin` ou `.hex`.

---

## 🙏 Um pedido

Se a aplicação ODrive DFU ou as dicas foram úteis, considere **se inscrever no canal**:

🔗 [Canal A Chave Virou no YouTube](https://www.youtube.com/@achavevirou)

---

## 🌐 Outros Links

- 📸 [Instagram A Chave Virou](https://www.instagram.com/achavevirou)  
- 📘 [Facebook A Chave Virou](https://www.facebook.com/share/g/1ArMr9tooj/?mibextid=wwXIfr)  
- 🛍️ [Loja Virtual A Chave Virou](https://www.achavevirou.com.br/)

---
