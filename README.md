## Hordozható Quiz rendszer 
1) Telepítsd a Node.js LTS verziót.
2) Másold a teljes 'quiz' mappát a gépre.
3) Nyisd parancssort a mappában, futtasd:
   npm init -y
   npm install express sqlite3 body-parser
4) Indítás:
   inditas.bat
5) Tanári menü: http://192.168.1.100:3000/teacher.html
   - Jelszó: bossboss
   - Itt választható a quiz (GitHub/Python/HTML/Arduino)
6) Diák felület: http://192.168.1.100:3000
7) Eredmények (alternatíva): http://192.168.1.100:3000/ertekel.html
8) Távelérés tartományitűzfal kikapcsolva, http://10.30.10.20

Kérdésfájl csere: a gyökérben lévő questions-*.json fájlokkal.
Az aktuális választás a current-quiz.txt-ben tárolódik, így újraindítás után is megmarad.

## 1. quiz/
2. ├── server.js
├── init-db.js
├── current-quiz.txt          # az aktuálisan kiválasztott JSON fájl neve (tartósításhoz)
├── questions-github.json      # kérdések (példa)
├── questions-python.json      # kérdések (példa)
├── questions-html.json        # kérdések (példa)
├── questions-arduino.json     # kérdések (példa)
├── public/
│   ├── teacher.html         # tanári menü (jelszavas)
│   ├── index.html           # diák felület
│   ├── ertekel.html         # tanári eredmény nézet
│   └── script.js            # közös kliens logika
├── inditas.bat              # Windows indító fájl
└── README.txt               # rövid használati útmutató

