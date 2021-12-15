# No-Skull Patch for Molden

Simple and dirty patch for [Molden](https://www.theochem.ru.nl/molden/), the ancient chemical/molecular viewer. Allows to close Molden without the need to click the annoying *Skull Icon*.

![Molden Closing](./closing.gif)

Tested on Molden 6.9 & gcc 9.3 @ a Linux machine.  
No warranty at all, although it is so simple that should not break anything.


## Usage

1. Download the [source code](https://ftp.science.ru.nl/Molden/) of Molden and untar it.
2. Apply the patch. `curl https://raw.githubusercontent.com/boneta/no-skull-patch/master/noskull.diff | patch src/xwin.c`
3. Compile Molden
4. Run Molden.
5. Close Molden without the skull icon!!!


## Full compilation example
```
wget https://ftp.science.ru.nl/Molden/molden6.9.tar.gz --no-check-certificate
tar -xzf molden6.9.tar.gz
cd molden6.9
curl https://raw.githubusercontent.com/boneta/molden-noskull-patch/main/noskull.diff | patch src/xwin.c
make
./bin/molden
```
