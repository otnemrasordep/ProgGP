# ProgGP

ProgGP is:

* a dataset of 173 GuitarPro songs from the progressive metal genre, converted to a token sequence format introduced on [DadaGP](https://github.com/dada-bots/dadaGP).

*Please contact Jack Loth or Pedro Sarmento via email or twitter, [@jackjamesloth](https://twitter.com/jackjamesloth) / [@umpedronosapato](https://twitter.com/umpedronosapato), to request access to the dataset for research purposes.*

Number of songs per artist in the dataset comprise:



## Usage as per [DadaGP](https://github.com/dada-bots/dadaGP)

#### Requirements

* python3
* PyGuitarPro 0.6 *(it ONLY works with 0.6 -- if you're using a newer version, install 0.6 in a virtual environment to run dadagp.py)*
```
pip install 'PyGuitarPro==0.6'
```

#### ENCODE (guitar pro --> tokens)
```
python dadagp.py encode input.gp3 output.txt [artist_name]
python dadagp.py encode examples/progmetal.gp3 progmetal.tokens.txt unknown
```

#### DECODE (tokens --> guitar pro)
```
python dadagp.py decode input.txt output.gp5
python dadagp.py decode progmetal.tokens.txt progmetal.decoded.gp5
```

Note:
* only gp3, gp4, gp5 files are supported by the encoder;
* rare combinations of instruments and tunings may not be supported;
* banjo is not supported;
* instrument-change events are not supported;



