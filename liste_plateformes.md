LoraWan TTN (The Thing Network)
----------------
Je regroupe ici mes connaissances sur The Thing Network.    
Auteur : Rémi Sarrailh    
Licence : CC-By    

# C'est quoi The Thing Network ?
The Thing Network (TTN) permet de connecter des objets à Internet à l'aide du Réseau LoRa.   
Tant qu'un objet LoRa est à portée d'une passerelle LoRaWan relié à TTN, ils pourront transmettre ses données sur Internet.    
Les messages sont chiffrés de bout en bout et seules les personnes ayant la clé de déchiffrement peuvent avoir accès aux données.    
Il est possible d'envoyer et de recevoir des messages par le biais des gateway (passerelle)    

http://www.electronicdesign.com/industrial-automation/11-myths-about-lorawan


# Gateway (passerelles)
Voici une liste des passerelles compatible avec The Thing Network    
Tutoriels : https://www.thethingsnetwork.org/labs/stories/gateway
# RHF0M301 
https://www.seeedstudio.com/Raspberry-Pi-LoRa/LoRa-LoRaWAN-Gateway-868MHz-Kit-with-Raspberry-Pi-3-p-2823.html


* Tutoriel : https://www.thethingsnetwork.org/labs/story/seedstudio-lorawan-gateway-built-on-risinghf/step/hardware-and-basic-sw-install



# IC880A
* https://wireless-solutions.de/products/radiomodules/ic880a.html
* Tutoriel : https://www.rs-online.com/designspark/building-a-raspberry-pi-powered-lorawan-gateway
* Installation : https://github.com/ttn-zh/ic880a-gateway/wiki


# Liste officielle: 
https://www.thethingsnetwork.org/docs/gateways/gateway/


# Devices (appareils)
Voici une liste de plateformes compatible avec The Thing Network. 
À l'aide de ces plateformes, on peut créer des capteurs / actionneurs qui à l'aide
d'une passerelle vont communiquer avec The Thing Network (sur internet)

## Atmega 32u4 / Atmega328
* Tutoriel TTN : https://www.thethingsnetwork.org/labs/story/using-adafruit-feather-32u4-rfm95-as-an-ttn-node
* Bibliothèque Arduino : https://github.com/matthijskooijman/arduino-lmic


### Arduino Mini Pro 3.3V / RFM95
* Testé : Oui
* Prix : 6,15€
* Microcontrolleur : Atmega328
* Radio : RFM95 (Module SX1276 LoRa®)
* Code de test : https://github.com/matthijskooijman/arduino-lmic/blob/master/examples/ttn-abp/ttn-abp.ino

### Lora32u4 -- Lora Lipo Atmega32u4
https://bsfrance.fr/lora-long-range/1345-LoRa32u4-II-Lora-LiPo-Atmega32u4-SX1276-HPD13-868MHZ-EU-Antenna.html 
* Prix : 13,12€
* Testé : non
* Microcontrôleur : Atmega32u4
* Radio : Semtech® SX1276
* Batterie : 100ma (par défaut) / 1000ma (Max)
* Consommation électrique : 
    * ~300uA en veille
    * 11ma en écoute (attente)
    * 1ma en réception + veille
* Datasheet: https://docs.bsfrance.fr/documentation/11355_LORA32U4II/Datasheet_LoRa32u4II_1.1.pdf

### Adafruit Feather 32u4 RFM95 LoRa Radio
https://www.adafruit.com/product/3078
* Testé : non
* Prix : 29,63€
* Microcontrôleur : ATmega32u4
* Radio : RFM95 (Module SX1276 LoRa®)
* Batterie : Chargeur intégré
* Consommation électrique :
    * ~300uA en veille
    * ~120mA pic pendant une transmission à +20dBM
    * ~40mA en écoute radio active
* Antenne : Câble / Connecteur uFL
* Documentation: 
    * Tutoriel : https://learn.adafruit.com/adafruit-feather-32u4-radio-with-lora-radio-module

## ARM Cortex M0
Programme envoi sur TTN (Cédric Goby) : https://github.com/CedricGoby/Arduino-MKR-WAN-1300/
https://www.adafruit.com/product/3178

### Adafruit Feather M0 with RFM95 LoRa Radio
* Testé : non
* Prix : 29,63€
* Microcontrôleur : ATSAMD21G18 ARM Cortex M0
* Radio : RFM95 (Module SX1276 LoRa®)
* Batterie : Chargeur intégré.
* Consommation électrique : 
    *  ~300uA en veille
    *  ~120mA pic pendant une transmission à +20dBM
    *  ~40mA en écoute radio active

### Arduino MKR WAN 1300
https://store.arduino.cc/usa/mkr-wan-1300
* Testé : oui
* Prix : 50€
* Microcontrolleur : SAMD21 Cortex-M0+ 32bit low power ARM MCU
* Radio : Murata CMWX1ZZABZ (IC: SX1276)
* Documentation:
    * Datasheet Radio : https://wireless.murata.com/RFM/data/type_abz.pdf
    * Programme envoi sur TTN (Cédric Goby) : https://github.com/CedricGoby/Arduino-MKR-WAN-1300/


