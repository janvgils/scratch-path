# My Scratch Path

## SatNOGS IQ data.
raw data recorded by a SatNOGS groundstation, files are 48000Hz, 16 bit complex.
To convert the IQ files to WAV or use them in other software, here are some example commands:

```
sox -t raw -b 16 -e signed-integer -r 48000 -c 2 iq_5293127.raw iq_5293127.wav
inspectrum -f c16 -r 48000 iq_5293127.raw
rffft -i iq_5293127.raw -f 436650000 -s 48000 -F int -T "2022-01-14T10:20:46"
```

[source](https://charon.camras.nl/public/satnogs/)
