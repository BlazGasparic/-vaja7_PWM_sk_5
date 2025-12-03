# vaja7_PWM_sk_5

Odgovori na vprašanja:


__V levem Pinout oknu razširite nabor možnosti za Timers ter za časovnik TIM1. Clock Source nastavite kot Internal Clock. Prvi kanal aktivirajte kot PWM Generation CH1. Kateri pin ste omogočili? Kaj se izpiše poleg pina?__ 
Omogočili smo pin 8 (PA8), izpiše se pa «TIM1_CH1«

__V Oknu Configuration kliknemo za TIM1 Vrednost Prescaler (Parameter settings) v zavihku Counter Settinngs določite tako, da bo časovnik delal s frekvenco 1 MHz. Koliko je vrednost Perscaler?__
16.

__Parameter Counter Period nastavimo na 100 in s tem še dodatno znižamo takt časovnika. Koliko znaša sedaj? kHz__
//

__V PWM Generation Chanel nastavite Pulse (16 bits value) na 50. Kaj pomeni ta parameter?__
To pomeni 16-bitno vrednost, ki določa dolžino visokega nivoja signala (duty cycle) znotraj ene PWM periode.

__Poiščite prenastavljeni parameter ..Pulse (vrednosti je nastavljena na 50) v vaši kodi in prepišite ukaz, ki ga je generiral CubeMX__
sConfigOC.Pulse = 50;

__Iz osciloskopa določite čas ene periode T in čas aktivnega pulza TON__
T = 26 us     TON = 13 us

__V kodi spremenite vrednost širine pulza na 25 %. Zapišite popravljeni ukaz v kodi__
sConfigOC.Pulse = 25;

__Zapišite kaj počnejo ukazi v 1.,2. in 3. vrstici (v user code begin 3):__
1. S tem ukazom spremeniš širino PWM impulza na TIM1 Channel
2. Poveča vrednost spremenljivke dutyCycle za 10 
3. Preveri, če je dutyCycle večji od 90, če je, potem nastavi spremenljivko na 10.

__Komentar:__
Vse deluje tako kot mora.
