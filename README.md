## Hordozható Quiz rendszer 
1) Telepítsd a Node.js LTS verziót. (node -v)
2) Másold a teljes 'quiz' mappát a gépre, a zip file mindent tartalmaz, klónozhatod is.
3) Nyisd parancssort a mappában, futtasd:
   - npm init -y 
   - npm install express sqlite3 body-parser parancsokat
4) Indítás:
   inditas.bat
5) Tanári menü: http://192.168.1.100:3000/teacher.html
   - Jelszó: bossboss
   - Itt választható a quiz (GitHub/Python/HTML/Arduino...)
6) Diák felület: http://192.168.1.100:3000
7) Eredmények (alternatíva): http://192.168.1.100:3000/ertekel.html
8) Táveléréshez a tartományitűzfal kikapcsolva, http://192.168.1.100:3000

Kérdésfájl csere: a gyökérben lévő questions-*.json fájlokkal.
Az aktuális választás a current-quiz.txt-ben tárolódik, így újraindítás után is megmarad.

# Projektstruktúra

```
quiz/
├── server.js                   # Node.js szerver
├── init-db.js                  # Adatbázis inicializálása
├── current-quiz.txt            # Az aktuális kérdéssor neve (tartósításhoz)
├── questions-github.json       # Példakérdések (GitHub témában)
├── questions-python.json       # Példakérdések (Python témában)
├── questions-html.json         # Példakérdések (HTML témában)
├── questions-arduino.json      # Példakérdések (Arduino témában)
├── public/
│   ├── teacher.html            # Tanári menü (jelszavas)
│   ├── index.html              # Diák felület
│   ├── ertekel.html            # Tanári eredmény nézet
│   └── script.js               # Közös kliens logika
├── inditas.bat                 # Windows indító fájl
└── README.txt                  # Rövid használati útmutató
```
