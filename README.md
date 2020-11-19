# google-translate

```javascript
export async function translate(text, language, key) {
    const url = `https://translation.googleapis.com/language/translate/v2?key=${key}`;
    const response = await fetch(url, {
        method: 'POST',
        headers : {
            'Content-Type': 'application/json',
        },
        body: JSON.stringify({
            target: language,
            format: "text",
            q: text
        }),
    });
    return await response.json();
}
```
