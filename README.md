# ⚽ Tic-Tac-Toe Football AI
### Adversarial Search · Minimax Algorithm · Alpha-Beta Pruning

> Tugas Project Kecerdasan Buatan — S1 Teknik Informatika  
> Topik 2: Pencarian Adversarial (Game Playing)

---

## 🎮 Demo Aplikasi

🔗 **Live Demo:** [Coming soon — deploy ke domain .my.id]

![screenshot](tampilan web tictactoe.jpeg)

---

## 📌 Deskripsi

Aplikasi web interaktif simulasi permainan **Tic-Tac-Toe bertema Football** menggunakan algoritma **Minimax** dan **Alpha-Beta Pruning**. Pemain berlaga melawan AI yang menggunakan teknik pencarian adversarial untuk menentukan langkah optimal.

Game ini dibangun sebagai portofolio implementasi algoritma AI klasik dalam konteks *zero-sum game* dua agen kompetitif.

---

## ✅ Fitur Wajib (sesuai modul)

| No | Fitur | Status |
|----|-------|--------|
| 1 | Mode Human vs AI dengan Minimax | ✅ |
| 2 | Implementasi Alpha-Beta Pruning | ✅ |
| 3 | Visualisasi Game Tree (3 level) | ✅ |
| 4 | Counter node: Minimax vs Alpha-Beta | ✅ |
| 5 | Toggle Minimax murni vs Alpha-Beta | ✅ |
| 6 | Pengaturan kedalaman pencarian (depth) | ✅ |
| 7 | Indikator giliran & status permainan | ✅ |
| 8 | Tampilan responsif (desktop & mobile) | ✅ |
| 9 | Mode Human vs Human *(bonus)* | ✅ |

---

## 🧠 Algoritma yang Diimplementasikan

### Minimax Algorithm
Algoritma pencarian yang mengevaluasi semua kemungkinan langkah hingga kedalaman tertentu. AI (MAX player) memaksimalkan skor, lawan (MIN player) meminimalkan skor.

```
function minimax(board, depth, isMax):
    if terminal state: return score
    if isMax:
        best = -∞
        for each move:
            best = max(best, minimax(board, depth-1, false))
        return best
    else:
        best = +∞
        for each move:
            best = min(best, minimax(board, depth-1, true))
        return best
```

### Alpha-Beta Pruning
Optimasi Minimax yang memangkas cabang pohon yang tidak mungkin mempengaruhi keputusan akhir, sehingga menghemat komputasi secara signifikan.

```
function alphabeta(board, depth, α, β, isMax):
    if terminal state: return score
    if isMax:
        for each move:
            α = max(α, alphabeta(..., α, β, false))
            if β ≤ α: break  // β cutoff (pruning)
        return α
    else:
        for each move:
            β = min(β, alphabeta(..., α, β, true))
            if β ≤ α: break  // α cutoff (pruning)
        return β
```

---

## 🎯 Difficulty Level

| Level | Depth | Keterangan |
|-------|-------|------------|
| 😊 Easy | 2 | AI bisa dikalahkan, cocok untuk latihan |
| 😐 Medium | 5 | AI cukup pintar, tantangan sedang |
| 😈 Hard | 9 | AI optimal, hampir tidak bisa dikalahkan |

---

## 🛠️ Teknologi

- **Frontend:** HTML5, CSS3, Vanilla JavaScript
- **Algoritma:** Minimax + Alpha-Beta Pruning (implementasi dari nol)
- **Font:** Barlow Condensed, Inter (Google Fonts)
- **Hosting:** Railway + Domain .my.id
- **Version Control:** Git + GitHub

---

## 🚀 Cara Menjalankan Lokal

1. Clone repository ini:
```bash
git clone https://github.com/Warpzyy/tictactoe-football-tugas10.git
cd tictactoe-football-tugas10
```

2. Buka file `index.html` langsung di browser:
```bash
# Windows
start index.html

# Mac
open index.html

# Linux
xdg-open index.html
```

Tidak perlu install apapun — aplikasi berjalan murni di browser! ✅

---

## 📊 Perbandingan Minimax vs Alpha-Beta

| Depth | Minimax (node) | Alpha-Beta (node) | Dipangkas | Efisiensi |
|-------|---------------|-------------------|-----------|-----------|
| 1 | 9 | 9 | 0 | 0% |
| 2 | 72 | 45 | 27 | ~38% |
| 3 | 504 | 198 | 306 | ~61% |
| 4 | 3024 | 756 | 2268 | ~75% |
| 5 | 15120 | 2394 | 12726 | ~84% |

> Alpha-Beta Pruning dapat memangkas hingga **84%+ node** dibanding Minimax murni pada depth tinggi.

---

## 📁 Struktur File

```
tictactoe-football-tugas10/
├── index.html      # Aplikasi utama (semua dalam 1 file)
└── README.md       # Dokumentasi ini
```

---

## 👤 Author

**Wifa Saputra Mahendra** — S1 Teknik Informatika  
🔗 [GitHub](https://github.com/Warpzyy) · [LinkedIn](https://linkedin.com/in/whiffaasm)

---

## 📚 Referensi

1. Russell, S., & Norvig, P. (2020). *Artificial Intelligence: A Modern Approach* (4th ed.). Pearson.
2. Silver, D., et al. (2016). Mastering the game of Go with deep neural networks and tree search. *Nature*, 529(7587), 484–489.
3. Campbell, M., Hoane, A. J., & Hsu, F. H. (2002). Deep Blue. *Artificial Intelligence*, 134(1-2), 57–83.
4. MIT OpenCourseWare 6.034 AI Lecture Notes. https://ocw.mit.edu
5. MDN Web Docs. https://developer.mozilla.org

---

<div align="center">
  <sub>⚽ Dibuat untuk tugas Kecerdasan Buatan — Adversarial Search & Game Playing</sub>
</div>