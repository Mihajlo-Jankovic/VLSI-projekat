# Detekcija objekata pomocu PYNQ Z2 ploce (VLSI-projekat)

Ovaj repozitorijum sadrzi pip install paket za Quantized Neural Network (QNN) na PYNQ ploci koriscenjem Multi-Layer Offload (MO) arhitekture. Koriscena su dva razlicita "sloja", W1A2 (1 bit-na tezina, 2 bit-na aktivacija) i W1A3 (1 bit-na tezina, 3 bit-na aktivacija), izvrsavanjem programabilne logike jednog Convolutional sloja i jednog Max Pool sloja (opcionalno).

## Brzo pokretanje
Kako bi ste instalirali na PYNQ plocu, povezite plocu, otvorite terminal i upisite
```shell
# (on PYNQ v2.3 and later versions, tested up to v2.5)
sudo pip3 install git+https://github.com/Mihajlo-Jankovic/VLSI-projekat.git
```

NAPOMENA: Ploca mora biti konektovana na internet

