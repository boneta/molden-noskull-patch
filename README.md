# No-Skull Patch for Molden

Simple and dirty patch for [Molden](https://www.theochem.ru.nl/molden/), the ancient chemical/molecular viewer. Allows to close Molden without the need to click the annoying *Skull Icon*.

![Molden Closing](./closing.gif)

Tested on Molden 7.1 & gcc 9.4 in a Linux machine.  
No warranty at all, although it is so simple that it should not break anything.


## Usage
1. Download the [source code](https://ftp.science.ru.nl/Molden/) of Molden and untar it
2. Apply the patch: `patch src/xwin.c noskull.diff`
3. Compile Molden
4. Run Molden
5. Close Molden without the skull icon!!!


## Full compilation example
```
wget https://ftp.science.ru.nl/Molden/molden7.1.tar.gz --no-check-certificate
tar -xzf molden7.1.tar.gz
cd molden7.1
curl https://raw.githubusercontent.com/boneta/molden-noskull-patch/master/noskull.diff | patch src/xwin.c
make
./bin/molden
```
