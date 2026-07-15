# **RankTune 🎵**

RankTune is an interactive, beautiful, and fluid web application that allows music lovers to rank every single track of their favorite albums, playlists, or artists through an addictive head-to-head voting system based on the ELO rating algorithm.

### **🚀 Try it Live**

No setup or keys required\! Play it directly here:

👉 [**orenbenn.github.io/albumranking**](https://orenbenn.github.io/albumranking)

## **🌍 Table of Contents / Table des matières / תוכן עניינים**

* [🇫🇷 Français](#francais) 
* [🇬🇧 English](#english)  
* [🇮🇱 עברית](#עברית)

<span id="francais"></span>
## **Français**

### **📝 Le Concept**

Combien de fois avez-vous débattu pour savoir quelle était la meilleure chanson d'un album ? **RankTune** résout ce problème de manière ludique et scientifique. En important un album, un artiste ou une playlist depuis Spotify, l'application génère une série de duels aléatoires entre les morceaux.

Grâce à un système de classement **ELO** (le même algorithme utilisé pour classer les joueurs d'échecs), chaque choix ajuste dynamiquement le score des pistes. À la fin du processus, vous obtenez un classement d'une précision absolue de vos morceaux favoris, accompagné d'une analyse statistique poussée.

### **✨ Fonctionnalités clés**

* **Import Flexible :** Recherchez un artiste en temps réel ou collez directement un lien Spotify (Artiste, Album ou Playlist).  
* **Classification Intelligente de la Discographie :** L'application récupère toute la discographie de l'artiste et la classe automatiquement de façon claire en 4 catégories :  
  * **Albums** (Albums studios classiques)  
  * **Deluxe & Remastered** (Rééditions et versions augmentées)  
  * **EPs & Mixtapes** (Formats intermédiaires de plus de 2 titres)  
  * **Singles** (Morceaux uniques)  
* **Accès Immédiat :** Hébergé directement sur GitHub Pages, aucune configuration d'API locale n'est requise.  
* **Algorithme d'Évaluation ELO :** Système dynamique de score individuel par chanson avec gestion des égalités (*passer*) et historique d'annulation (*undo*).  
* **Double Moteur d'Extraits Audio :** Récupération automatique d'extraits d'écoute de 30 secondes via Spotify et l'API Apple Music/iTunes pour une couverture maximale.  
* **Console de Synchronisation (Dev Panel) :** Panneau de logs accessible en un clic pour analyser le processus d'alignement des chansons et diagnostiquer les connexions API en temps réel.  
* **Statistiques Avancées :** Un modal interactif calcule et affiche vos pourcentages d'appréciation pour chaque piste à l'issue de vos duels.  
* **Ergonomie Mobile & Raccourcis Clavier :** Entièrement responsive sur mobile (gestes tactiles) et contrôlable sur ordinateur avec les flèches du clavier (←, →, ↓ et Backspace).  
* **Reprise de Session :** Sauvegarde automatique locale de vos duels en cours pour ne jamais perdre votre progression.

### **🛠️ Sous le capot (Technique)**

* **Architecture Serverless :** L'intégralité de l'application tourne côté client. Les jetons d'accès et les requêtes API vers Spotify et iTunes sont gérés de manière transparente et sécurisée directement par le navigateur.  
* **Tri de la Discographie & Dé-doublonnage :** Pour éviter d'encombrer l'écran, l'algorithme normalise les noms d'albums et applique un filtre de similarité strict pour séparer les rééditions Deluxe des albums originaux et regrouper intelligemment les singles.  
* **Algorithme ELO :** Les scores commencent tous à 1000 points. À chaque duel, le calcul de la probabilité de victoire ajuste les scores avec un facteur ![][image1].  
* **Fuzzy Matching :** Pour associer les morceaux de Spotify avec les extraits d'Apple Music, un algorithme nettoie les chaînes de caractères (accents, ponctuations, mentions "Deluxe/Bonus") afin de garantir le meilleur taux de correspondance possible.

<span id="english"></span>
## **English**

### **📝 The Concept**

How many times have you debated which song is truly the best on an album? **RankTune** solves this in a fun, elegant, and scientific way. By importing any album, playlist, or artist from Spotify, the application generates a series of random head-to-head duels between songs.

Using the **ELO Rating System** (the very algorithm used to rank chess players), each of your choices dynamically adjusts the tracks' scores. At the end, you get an extremely accurate, personalized ranking of your favorite tracks, complete with custom taste analytics.

### **✨ Key Features**

* **Flexible Import:** Search for an artist in real-time or directly paste a Spotify link (Artist, Album, or Playlist).  
* **Smart Discography Classification:** The app automatically fetches the entire artist catalog and cleans it into 4 organized sections:  
  * **Albums** (Standard studio albums)  
  * **Deluxe & Remastered** (Expanded versions & special editions)  
  * **EPs & Mixtapes** (Mid-length projects with over 2 tracks)  
  * **Singles** (Standalone releases)  
* **Instant Play:** Hosted directly on GitHub Pages, meaning you don't need to configure any local keys or credentials.  
* **ELO Rating Algorithm:** Dynamic scoring for each song with tie support (*skip*) and action history for undoing votes (*undo*).  
* **Dual-Engine Audio Previews:** Automated retrieval of 30-second audio previews from Spotify and iTunes/Apple Music API fallbacks.  
* **Sync Console (Dev Panel):** Interactive log panel to monitor real-time API performance, search queries, and audio-matching results.  
* **Taste Analytics:** An elegant statistics modal that calculates and visualizes your appreciation percentage for every track based on your duel history.  
* **Mobile-Friendly & Keyboard Support:** Fully responsive with optimized touch targets for mobile, and keyboard shortcuts (←, →, ↓, and Backspace) for desktop power-users.  
* **Session Recovery:** Automatic in-memory save system to resume interrupted sessions anytime.

### **🛠️ Under the Hood (Technical)**

* **Serverless Architecture:** The entire app runs fully client-side. Access tokens and API requests to Spotify and iTunes are seamlessly and securely handled directly in the browser.  
* **Catalog Sorting & De-duplication:** To prevent clutter, the algorithm normalizes album names and applies strict similarity checks to differentiate original releases from Deluxe versions while consolidating singles.  
* **ELO Algorithm:** Song ratings start at 1000 points. Every matchup outcome calculates expected victory probabilities and updates ratings using a dynamic ![][image2]\-factor of 32\.  
* **Fuzzy String Matching:** To map Spotify track lists to Apple Music audio previews, an intelligent cleaner strips special characters (accents, punctuation, "Deluxe/Bonus" suffixes) to guarantee maximum matching coverage.

<span id="עברית"></span>
## **עברית**

### **📝 הקונספט**

כמה פעמים התוכחתם עם חברים איזה שיר באמת הכי טוב באלבום מסוים? **RankTune** פותרת את הבעיה הזו בצורה חווייתית, אלגנטית ומדעית. על ידי ייבוא של אלבום, פלייליסט או אמן מספוטיפיי, האפליקציה מייצרת סדרת דו-קרבים אקראיים (ראש בראש) בין השירים.

בעזרת שימוש בשיטת מד הכושר **ELO** (אותו אלגורิตם המשמש לדירוג שחקני שחמט), כל בחירה שלכם מעדכנת באופן דינמי את הניקוד של השירים. בסיום התהליך, תקבלו דירוג מדויק להפליא של השירים האהובים עליכם, יחד עם ניתוח סטטיסטי אישי.

### **✨ תכונות עיקריות**

* **ייבוא גמיש:** חיפוש אמנים בזמן אמת או הדבקה ישירה של קישור ספוטיפיי (אמן, אלבום או פלייליסט).  
* **מיון דיסקוגרפיה חכם:** האפליקציה שולפת אוטומטית את קטלוג האמן ומארגנת אותו ב-4 קטגוריות ברורות ללא כפילויות:  
  * **אלבומים** (אלבומי אולפן רגילים)  
  * **מהדורות דלוקס** (גרסאות מורחבות ומיוחדות)  
  * **EP ומיקסטייפ** (פרויקטים באורך בינוני עם יותר מ-2 שירים)  
  * **סינגלים** (רצועות בודדות)  
* **גישה מיידית:** האפליקציה מאוחסנת ישירות ב-GitHub Pages, מה שאומר שאין צורך להגדיר מפתחות או הרשאות מקומיות כדי להתחיל לשחק.  
* **אלגוריתם דירוג ELO:** ניקוד דינמי לכל שיר עם אפשרות לתיקו (*דלג*) והיסטוריית פעולות לביטול הצבעות קודמות (*בטל*).  
* **מנוע כפול לתצוגה מקדימה של שמע:** שליפה אוטומטית של קטעי האזנה בני 30 שניות מספוטיפיי וגיבוי חכם מ-iTunes/Apple Music API.  
* **לוח בקרת סנכרון (מסוף פיתוח):** חלון תיעוד אינטראקטיבי המציג בזמן אמת את קריאות ה-API, שאילתות החיפוש והתאמות השירים.  
* **ניתוח העדפות מתקדם:** מונחון סטטיסטיקה מרהיב המחשב ומציג באחוזים את רמת ההערכה שלכם לכל שיר בהתבסס על תוצאות הדו-קרב.  
* **מותאם לנייד ומקלדת:** תאימות מלאה למסכי מגע בניידים, ותמיכה בקיצורי מקלדת (←, →, ↓ ו-Backspace) למשתמשי מחשב.  
* **שחזור מפגש:** שמירה אוטומטית מקומית כדי להמשיך בדירוג בדיוק מהנקודה שבה הפסקתם.

### **🛠️ מאחורי הקלעים (צד טכני)**

* **ארכיטקטורת Serverless:** האפליקציה פועלת כולה בצד הלקוח. קבלת האסימונים וקריאות ה-API מול Spotify ו-iTunes מבוצעות בצורה מאובטחת ושקופה ישירות מהדפדפן של המשתמש.  
* **מיון קטלוג ומניעת כפילויות:** כדי למנוע עומס ויזואלי, האלגורิตם מנרמל את שמות האלבומים ומבצע בדיקות דמיון קפדניות על מנת להפריד בין אלבומי מקור למהדורות דלוקס תוך איחוד סינגלים.  
* **אלגוריתם דירוג ELO:** הדירוג של כל השירים מתחיל ב-1000 נקודות. לאחר כל דו-קרב, סיכויי הניצחון מחושבים מחדש והניקוד מתעדכן דינמית עם מקדם שינוי של ![][image1].  
* **התאמת מחרוזות חכמה (Fuzzy Matching):** כדי לשייך בצורה מושלמת בין רשימת השירים מספוטיפיי לקטעי השמע של Apple Music, אלגוריתם חכם מנקה תווים מיוחדים (סימני פיסוק, מבטאים ותוספות כמו "Deluxe/Bonus") כדי להבטיח אחוזי התאמה מקסימליים.

[image1]: <data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAEMAAAAaCAYAAADsS+FMAAAC8klEQVR4Xu1XS2tTQRS+l1bwLVpjbF6Tl4QuxEVQKCgiKCi0UlRQcK8uuitk6w/Qgogbu1CqCCK0GxHFVcGFqKB0pYgbRQQXWhAUs7Dx+7hnzMk0baJgksJ88JF7HjNz5pwz906CwMPDw+MfkclkThlj7oBTDo/RHovFNsLnorZBPuLO0yGEyWRyoFAo7MBzn2u0KJfLaxDjfvpCDF37skilUrtVQj5ls9kL4Fgikdgu9nWwn4PtB0lfa+sksPYQ+BJ8Ab6XeMaDxqSEiG8E+s/gV7AGvsN+Diqf1sCgq0xI4GQyHo9vgP4GFrlZLBY3a1ungAqnEMMrFknkATw/52ZZPOuXTqePQzePAhYhhrCdhvwLXLA+LWGirH/BhstaD/kZFtirdd0A4jiM+BbBKjhMHTY6LZWfo4zfQRN1DBM0bcdCPiF+Q1a3IuwA2/5y5iqYdKfr2yWEuVxuj1TcHt1HsslJq8PzfdFN2IHwG6XOLfSyMNERqeExxKTb8DyDRDx2/XoF6NYDiLGKGN8iSUaZ+kql0iYls4POc2/YV1Lrm4KD4fxEMsrj8lqe2z9nClyUL9m/ITvRnacZpFAnwZ/gbKvO1R0UtPNVMfUzVePLUnTjosu5/r0AJg+x3WOM2GzFtRPomH0sKPgwn89vce1NYeSIgLeULgd+RObPaN9egqkXseraCB4h2G7bArcEsrrVRN9tTnpWmULI18A5XrqUvitAHIOIdUTfbyCXof/O2LUvwU6A/rI6fv08Yg1OLox8UsFvfFs7tmFwERk+qvWtQH9Jbtt0X3ou4DMvvg8w/1rq+Mk30cWrIRnyVZkK1GWMReddRbktBQbNyCKzyPp6bZNzSRuzfyhY4fr7v4EEXEEMb7DRXZT1O0M2TvD2WRHdEsLeX59RwURV5wWmYYDNuql3zB8bFvqA9su4c3UCbHusfxdxLCDG6/h9KnFdYifQx6hLVzO6c6564A9aGskYQ2JG5U+Yh4eHh4eHh0fP4jfrPfqDrteZUwAAAABJRU5ErkJggg==>

[image2]: <data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABMAAAAaCAYAAABVX2cEAAABO0lEQVR4XmNgGAUUATk5uRB5efmlQDwLDXsiqalHl0c2Aw5kZGR0kQz8r6CgkAHEAVJSUiIwNUD5NKDcNxAGsmeA1CObgQGACieBDAMyGbHIzQMaMF9FRYUPXQ4DABVrAvFbIP6KJu4ENOQkshhBANQUBHIVEF8F8Y2NjVmBhpQB+auAXpZAV48XwLwI8gowDIWA7LVAQ3YBw40LXS1eoK6uzgvUfBjqsmggvg5lv5eVldVBV48XIHkR7DKoWA5U7AkQK6LrwQnkoV4E4kVALjNUTBFqECipRKBpwQ6ALhEEajgNNSwaSYoRyJ8CFT+AJI4byCOSxCdFRUV9NDlLIP4JxP+QxXECoMK1UNvXocccKHkAxXuh8o4M0CDAAEi2ghQi461QeZiL4XLAIHmkpKQkh27WKBgFQw4AAEQyaCbXWZfvAAAAAElFTkSuQmCC>
