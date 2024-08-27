# Desafio Alura: Decodificador de Texto

Apresento a todos o "Decodificador de Texto", uma aplicação que criptografa textos de uma área de entrada, enviando o texto para uma segunda área já criptografado, e descriptografa esse texto quando inserido na área de entrada, mostrando o resultado na segunda área. Apenas letras minúsculas e sem acento são aceitos no texto.

## Funcionalidades

### 1. Como Funciona a Criptografia

Quando o botão `"Criptografar"` é pressionado, o texto inserido é criptografado usando um mapa predefinido:

    ```js
    const encryptionMap = {
        a: "ai",
        e: "enter",
        i: "imes",
        o: "ober",
        u: "ufat",
    };
    ```
### 2. Como Funciona a Descriptografia

Quando o botão `"Descriptografar"` é pressionado, o texto criptografado é descriptografado usando o mapa inverso, com a função `invertObject`:

    ```js
    function invertObject(obj) {
        const invertedObj = {};
        for (const key in obj) {
            if (obj.hasOwnProperty(key)) {
                invertedObj[obj[key]] = key;
            }
        }
        return invertedObj;
    }
    ```

### 3. Informações Complementares

Quando o botão `"Copiar"` é pressionado, o texto na área de resposta é guardado na área de transferência.
Se não houver texto na área de entrada, será apresentado alerta de que a respectiva área está vazia.