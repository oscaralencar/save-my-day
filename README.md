# save-my-day
Links/códigos úteis que salvam o dia

## Javascript

Converte File para base64
```
/**
 * Converte File para Base64
 * @param {File} file
 * @returns {Promise<String>}
 */
toBase64(file) {
    return new Promise((resolve, reject) => {
        const reader = new FileReader()
        reader.readAsDataURL(file)
        reader.onload = () => resolve(reader.result)
        reader.onerror = error => reject(error)
    })
}
```
