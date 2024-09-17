- 👋 Hi, I’m @Gorzy27
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
Gorzy27/Gorzy27 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

import hashlib

# Gehashtes Passwort (z.B. SHA-256-Hash für 'password')
hashed_password = "5e884898da28047151d0e56f8dc6292773603d0d6aabbdd9e0c0e4e037edbdb"

# Wörterbuch-Datei öffnen
with open('/Users/gorzy27/Desktop/Programmieren/dc.txt', 'r') as file:
    for word in file:
        word = word.strip()  # Entfernen von Leerzeichen und Zeilenumbrüchen
        hashed_word = hashlib.sha256(word.encode('utf-8')).hexdigest()

        # Vergleichen des Hashes
        if hashed_word == hashed_password:
            print(f"Passwort gefunden: {word}")
            break
    else:
        print("Passwort nicht gefunden.")

