# Duran Sicimler Teoremi X — Yayın Paketi (Külliyat Taç Taşı)

> **English:** [README.md](./README.md)

**Duran Sicimler Teoremi X: Tokamak H-Modu ve ELM Bastırması, Kaçak Elektron-Pozitron Çığ Doyumu ve 30-Mertebeli Evrensel Girdap-Sicim Ölçekleme Yasası**

Yazar: Fahri Meral · Tarih: 17 Ekim 2026 · Sürüm: v1 (Makale X)

> **Durum:** Yayımlanmamış ön baskı (v1). Hakem denetiminden geçmemiştir.

## İçerik

| Dosya | Açıklama |
|---|---|
| `paper/duran_sicimler_teoremi_X.tex` | Ana makale, Türkçe (Tablo 1–4, Şekil 1 2×2) |
| `paper/duran_sicimler_teoremi_X_EN.tex` | İngilizce sürüm |
| `figs/fig12_tokamak_elm_runaway_and_universal_scaling.pdf` | Test T26–T28 şekli (TR, 2×2) |
| `figs/fig12_tokamak_elm_runaway_and_universal_scaling.png` | Test T26–T28 şekil önizlemesi (TR) |
| `figs/fig12_tokamak_elm_runaway_and_universal_scaling_en.pdf` | Test T26–T28 şekli (EN, 2×2) |
| `figs/fig12_tokamak_elm_runaway_and_universal_scaling_en.png` | Test T26–T28 şekil önizlemesi (EN) |
| `CITATION.cff` | Atıf kaydı |
| `LICENSE` | CC BY 4.0 |

## Sayısal üretim

Test T26–T28, **V. makale deposundaki** ([`stationary-strings-v`](https://github.com/fahrim/stationary-strings-v)) çözücüyle üretilir:

```bash
git clone https://github.com/fahrim/stationary-strings-v
pip install numpy scipy matplotlib
python duran_sicimler_sim/solver_engine.py   # T1–T28 (28/28 PASS)
python duran_sicimler_sim/mini_check_x.py    # bağımsız çapraz kontrol (15/15 PASS)
python duran_sicimler_sim/generate_figures.py  # Şekil 1 (+_en)
```

Bağımsız çapraz kontrol çözücüyü import etmez.

## Kilit bulgular

- T26 (Teorem X.1): FENE-P RMP Süper-Peeling-Ballooning sınırı (`χ=0,75` için `1,970942×`),
  `α_MHD = 1,5 α_crit^std` aşırı-basınçlı kaidede sınırlı ELM filaman salınımı ve ITER ile SPARC'ı ateşleme rejimine taşıyan `H_98^string = 3,1560` (`χ=0,50`) / `5,5516` (`χ=0,75`).
- T27 (Teorem X.2): Kiral-elastik kritik alan yükseltmesi `E_c^eff/E_c = S_loss(1+4Σ_string) = 23,788450` (`χ=0`) ve `38,928355` (`χ=0,75`); `E_||/E_c = 30` tokamak yıkımında kaçak çığın tam sönümlenmesi (`γ_RA^std = +33,5550 /s → γ_RA^string = −0,2654 /s < 0`).
- T28 (Teorem X.3): Ölçekten bağımsız `Π_Meral = µ_s^Meral = 0,2044088237` ve `I_shield = 2√2` değişmezleri ile 30 büyüklük mertebesi (`10^-10 m → 3×10^20 m`) boyunca birim eğimli (`m = 1,000000000000000`, `R^2 = 1,0`) evrensel ölçekleme doğrusu.

## Lisans

CC BY 4.0 — bkz. `LICENSE`. İçerik hakem denetiminden geçmemiştir.
