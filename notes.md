# termos/ferramentas para estudar e entender

* Dalvik
* HAL
* RIL - driver do android em espaço de usuário
* ofono - https://01.org/ofono - framework para desenvolvimento de aplicações
  que usem telefonia móvel (GSM/UMTS)

* Das U-Boot - bootloader open source


* parei em https://cascardo.eti.br/blog/GNU_on_Smartphones_part_II/ (ROOT)

# boot

* bootloader: fica no chip, dentro do celular, não são livres. Existem pedaços
  que são difíceis de serem removidos pois precisa modificar parte da ROM

* das u-boot é uma das melhores opções, pois é livre e é compatível com vários
  equipamentos, sistemas de arquivos, boot via rede, usb e serial. Mas portá-lo
  não é uma tarefa fácil

* usar o bootloader que vem com o equipamento é um caminho, para utilizar
  outras partes livres

* desafio é construir uma única imagem que possa fazer boot em qualquer
  equipamento. ARM não possuí um único ambiente de boot 


