# Detekcija objekata pomocu PYNQ Z2 ploce (VLSI-projekat)

Ovaj repozitorijum sadrzi pip install paket za Quantized Neural Network (QNN) na PYNQ ploci koriscenjem Multi-Layer Offload (MO) arhitekture. Koriscena su dva razlicita "sloja", W1A2 (1 bit-na tezina, 2 bit-na aktivacija) i W1A3 (1 bit-na tezina, 3 bit-na aktivacija), izvrsavanjem programabilne logike jednog Convolutional sloja i jednog Max Pool sloja (opcionalno).

## Brzo pokretanje
Kako bi ste instalirali na PYNQ plocu, povezite plocu, otvorite terminal i upisite
```shell
# (on PYNQ v2.3 and later versions, tested up to v2.5)
sudo pip3 install git+https://github.com/Mihajlo-Jankovic/VLSI-projekat.git
```

NAPOMENA: Ploca mora biti konektovana na internet

## Organizacija projekta

Projekat je organizovan na sledeci nacin:

- folder qnn: Sadrzi opis qnn klase, kao i klasa za testiranje mreze
  - src: Sadrzi izvor 2 overlay-a i biblioteke za rebuild-ovanje
    - library: FINN biblioteka za HLS QNN-MO opise, host kod, skripta za rebuild-ovanje i trajveri za PYNQ
    - Network: topologije W1A2 i W1A3 HLS top funkcije, host kod i skripta za build-ovanje HW-a i SW-a
  - bitstreams: Bit-streamovi za 2 overlay-a
  - libraries: pre-kompajlirani deljeni objekti za low-level drivere
  - params: skup treniranih parametara
- notebooks: lista skupova python-ovih biblioteka , koji ce tokom instalacije biti premesteni `/home/xilinx/jupyter_notebooks/qnn/` folder
- tests: testna skripta i testne slike
