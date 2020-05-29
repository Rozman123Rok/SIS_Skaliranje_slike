# Skaliranje slike

V tej nalogi pripravite metodo za skaliranje slike za celoštevilski faktor (decimacijo). Faktor 2 pomeni da izberete vsak 2 piksel slike, faktor 5 pa vsak 5 piksel (po višini in širini). Pri decimaciji efektivno spreminjate vzorčevalno frekvenco, zato morate sliko tudi ustrezno filtrirati. V nalogi omogočite izbiro filtra povprečenja in Gaussovega filtra.

Pripravite Python skripto z naslednjo funkcijo:

## def decimiraj_sliko(slika, faktor, filter, gauss_sigma=None):

- funkcije prejme 3 obvezne in eden opcijski parameter
    - slika je tabela oblike (H, W, 3) in tipa numpy.unit8
    - faktor je celo število, ki predstavlja faktor pomanjšave
    - filter je niz, ki je lahko 'mean' ali 'gauss'
        - 'mean' uporabi kvadratni filter, enake velikosti kot faktor
        - 'gauss' uporabi Gaussov filter
    - gauss_sigma je faktor glajenja, ki se uporabi v Gaussovem filtru, če je ta bil izbran
- funkcija vrne pomanjšano sliko oblike (H/faktor, W/faktor, 3)
- kadar dimenzije slike niso večkratnik faktorja, se robovi odrežejo (slika velikosti 14x20x3 se z faktorjem 3 pomanjša v 4x6x3)

Pripravite še odsek kode katero lahko lahko samostojno zaženete kot demo:

## if __name__ == '__main__':

- pripravite demo katerega lahko poženete
  - print("Modul za skaliranje slike!")
 
Pred oddajo je smiselno rešitev preizkusiti na pravih slikah.