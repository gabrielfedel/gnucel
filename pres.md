% Gnu/Linux em Celular Android
% Gabriel Fedel
% Julho/2018


# O que não vou fazer

## O que não vou fazer

* Rodar gnu/linux "dentro" do Android
    * https://www.xda-developers.com/guide-installing-and-running-a-gnulinux-environment-on-any-android-device/
    * Soluções que criam "sandbox" e permitem instalar debian/ubuntu
    * Algumas soluções não exigem "dar root" no celular
    * Aplicações que promovem essa funcionalidade: GNURoot Debian e XServer XSDL (esse último para prover o X)

## O que não vou fazer

* "Liberar o Android"
    * https://replicant.us/
    * parte do esforço poderá ser utilizado (engenharia reversa em drivers de
      modens e bootloaders livres)

* Instalar uma ROM
    * https://lineageos.org/ (antigamente cyanogen)

* Construir um telefone para rodar gnu/linux
    * https://puri.sm/shop/librem-5/

# Qual é a ideia?

## Qual é a ideia?

* Rodar gnu/linux em celulares "populares", substituindo o android
* Rodar debian com kernel stable
* Depois rodar kernel upstream
* Documentar processo e fazer eventuais patches necessários

## Desafios

* Diferença entre os dispositivos
* Possibilidade de perder dados e o dispositivo (brick)
* Fazer boot (aparentemente uma das partes mais complexas)
* Drivers
* ...

## Desafios - boot

* bootloader: fica no chip, dentro do celular, não são livres. Existem pedaços
  que são difíceis de serem removidos pois precisa modificar parte da ROM

* das u-boot é uma das melhores opções, pois é livre e é compatível com vários
  equipamentos, sistemas de arquivos, boot via rede, usb e serial. Mas portá-lo
  não é uma tarefa fácil

* usar o bootloader que vem com o equipamento é um caminho, para utilizar
  outras partes livres

* desafio é construir uma única imagem que possa fazer boot em qualquer
  equipamento. ARM não possuí um único ambiente de boot 

## Desafios - drivers

* Rodar drivers em espaço de usuário (o android provê isso através de seu
  framework)

* Modem(RIL) : alternativas RIL livre e ofono (intel)

* Graphic: mesa, wayland, X.org ou framebuffer driver.

## Por que fazer isso

* Controle sobre o aparelho
* Abrir caminho para mais aparelhos rodando gnu/linux

## Alguns dos primeiros passos

* root no celular - ganhar acesso para modificar todas as partes

## Modelo escolhido

* Moto E condor 
* Diversos modelos da motorola são similiares
* Celulares motorola tem suporte para desbloquear bootloader

# Referência

## Materiais de referência

* https://wiki.debian.org/Mobile
* https://cascardo.eti.br/blog/GNU_on_a_Smartphone/
* https://cascardo.eti.br/blog/GNU_on_Smartphones_part_II/
* https://cascardo.eti.br/blog/mdc2017/
* https://wiki.postmarketos.org/wiki/Main_Page
