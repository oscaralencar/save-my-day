# save-my-day
Links/códigos úteis que salvam o dia

## Javascript

### Converte File para base64
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

### Arquivo salvando em branco com FileSaver
https://stackoverflow.com/questions/33100281/angularjs-filesaver-producing-empty-file

## VueJs
### Geral
#### Axios get concatenar filtros
```
import Qs from 'qs'

consultar: (filtro) => {
  if (filtro.dataEnvio) {
    filtro.dataEnvio = dateFormatterMixin.methods.convertDateBrToUs(filtro.dataEnvio)
  }
  return http.get(`/operacao`, {
    params: filtro, paramsSerializer: function (params) { 
      return Qs.stringify(params, { arrayFormat: 'brackets' })
    }
  })
}

```


### Quasar

#### Tabs validação
https://forum.quasar-framework.org/topic/5176/multiple-tabs-with-q-inputs-keep-refs-for-validation/4


