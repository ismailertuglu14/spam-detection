### Test Size Değişikliği

Projenin içindeki `train_test_split` fonksiyonunda kullanılan `test_size` parametresi değiştirilerek modelin test seti üzerindeki performansı değerlendirilebilir.

| Test Size | Accuracy on Test Data |
|-----------|------------------------|
| 0.2       | 0.9820627802690582     |
| 0.3       | 0.9826555023923444     |
| 0.4       | 0.9816061013907582     |

### Diğer Sonuçlar

- **En İyi Parametreler ile Model Eğitimi:**

    ```python
    best_logreg_model = LogisticRegression(C=grid_search.best_params_['C'])
    best_logreg_model.fit(X_train_features, Y_train)
    ```

    - Eğitim Seti Doğruluğu: 1.0
    - Test Seti Doğruluğu: 0.9820627802690582