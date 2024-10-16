## Installation

Use an environement with either Python 3.8 or 3.9 or 3.10 . Then :

```shell
pip install -r requirements.txt
```

Install and activate solc 0.8.19 :

```
solc-select install 0.8.19
solc-select use 0.8.19
```

Install the [foundry framework](https://github.com/foundry-rs/foundry.git), in order to get anvil, 

```
curl -L https://foundry.paradigm.xyz | bash
```

Then, in a new terminal (to update `PATH`), run the following command :

```
foundryup
```

## Usage


Example :

```shell
python3 lysmata.py -r 1000 -s 100 -c tests/invariant_breaker.sol
```

## DA FARE
    - Supporta il pagamento di ether durante le transazioni che coinvolgono funzioni pagabili o fallback pagabili.

    - Supporta l'invio di transazioni da diversi account durante la campagna fuzzing, invece di un singolo EOA.

    - Attualmente la generazione di costanti (ovvero l'estrazione di costanti hardcoded dal codice per usarle come argomenti durante i test basati sulle proprietà) è supportato solo per i parametri string, uint, int e address. constants_minings dovrebbe supportare anche altri tipi di input: bytes, array e struct.
    
    - Alcuni casi limite sono ancora problematici: se un contratto contiene più funzioni con lo stesso nome o se più contratti condividono lo stesso nome.
