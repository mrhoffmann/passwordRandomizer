;keys: control+p standard

^p::
;swedish
variation := "ljus|mörk|extra|liten|stor"
word := "Rosa|Grön|Röd|Blå|Grå|Svart|Gul|Brun|Orange|Silvrig|Guldig"
what := "Traktor|Bil|Skoter|Lastbil|Släpvagn|Kross|Cykel"
symbols := "!|#|¤|&|_|-|/|(|)|=|*"

;english
;variation := "bright|dark|extra|tiny|large|big"
;word := "Pink|Green|Red|Blue|Gray|Black|Yellow|Brown|Orange|Silvery|Golden"
;what := "Tractor|Car|Snowmobile|Lorry|Trailer|Cross|Bike"

   random, random, 1, 4
   random, rando, 1, 10
   random, rand, 1, 11
   random, ran, 1, 7
   random, ra, 1971, 2020

   stringsplit, list, variation, |
   stringsplit, list1, word, |
   stringsplit, list2, what, |
   stringsplit, list3, symbols, |

   nVar = % list%random%
   nWord = % list1%rando%
   nWhat = % list2%rand%
   nSym = % list3%ran%

   container = %nVar%%nWord%%nWhat%%ra%%nSym%
   Clipboard := container

return