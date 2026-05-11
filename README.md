# NASA Airfoil Self-Noise — Regresyon Modelleri Karşılaştırması

## Proje Hakkında
Bu projede NASA tarafından düşük hızlı rüzgar tüneli testlerinden elde edilen **Airfoil Self-Noise** veri seti üzerinde 11 farklı regresyon modeli uygulanmış ve karşılaştırılmıştır.

**Amaç:** Kanadın fiziksel özelliklerini (frekans, hız, açı vb.) kullanarak ürettiği ses basınç seviyesini (dB) tahmin eden en iyi modeli bulmak.

## Veri Seti
- **Kaynak:** NASA Langley Araştırma Merkezi
- **Gözlem sayısı:** 1503
- **Bağımlı değişken:** SSPL — Ses Basınç Seviyesi (dB)
- **Bağımsız değişkenler:** Ses frekansı, hücum açısı, kanat uzunluğu, akış hızı, sınır tabakası kalınlığı

## Uygulanan Modeller
| Sıra | Model | RMSE | R² |
|:----:|-------|:----:|:--:|
| 1 | **Gradient Boosting** ★ | 1.5776 | 0.9473 |
| 2 | Random Forest | 1.8157 | 0.9302 |
| 3 | Bagging | 1.8699 | 0.9259 |
| 4 | SVR (RBF) | 3.9896 | 0.6629 |
| 5 | ANN (MLP) | 4.0231 | 0.6572 |
| 6 | Karar Ağacı | 4.6351 | 0.5450 |
| 7 | Doğrusal Regresyon | 4.8670 | 0.4983 |
| 8 | PLS | 4.8676 | 0.4982 |
| 9 | SVR (Linear) | 4.9077 | 0.4898 |
| 10 | PCR | 4.9213 | 0.4870 |
| 11 | KNN | 6.0467 | 0.2256 |

## Sonuç
**En iyi model: Gradient Boosting** — Gürültü seviyesindeki değişimlerin **%94.7'sini** açıklamaktadır (RMSE = 1.58 dB).

Doğrusal modellerin R² ≈ 0.50 düzeyinde kalması, veri setindeki ilişkilerin büyük ölçüde doğrusal olmadığını ortaya koymaktadır.

## Kullanılan Teknolojiler
- Python
- NumPy, Pandas
- Scikit-learn
- Statsmodels
- Matplotlib, Seaborn

