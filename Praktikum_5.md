# Praktikum 5
Sellel nädalal tegelesime Linuxi failiõigustega.

5.1. Minimaalsed õigused peavad olema:

a) Peab olema lugemisõigus.

b) Peab olema kirjutamisõigus ja kustutamisõigus.

5.2. "chmod a = x" - annab failile käivitamisõiguse kõigile kasutajatele. Aga selleks, et faili käivitada on vajalik lugemis- ja käivitamisõigus, sellepärast selleks, et faili oleks võimalik käivitada õigused peavad olema vähemalt "chmod a = rx"

5.3. See lihtsustab grupipõhist koostööd, võimaldab failide juurdepääsu kontrollimist, ja aitab tugevdada süsteemi turvalisust.

5.4. 

5.5.

5.6. See võib väendada süsteemi turvalisust, sest see võimaldab programmil käivitada kõrgemate privileegidega. Kui seda kontrollita, võivad teised inimesed, isegi tavaksutajad, saada ligipääsu süsteemi kriitilistele ressurssidele.

5.7. Kasutajad kes saavad kustutada faili: "õpetaja", "peeter", muu kasutaja kes loonud faile.

5.8. 
# file: hinded.txt
# owner: peeter
# group: peeter
user::rw-
group::rw-
other::r--


5.9. Kasutadaes "chattr +i" faili sisu muuta ei saa, ainult "root" kasutaja võib seda teha.
