# Sorozat rangsor

Az eddig látott sorozataim szimpátia sorrendben, poszterekkel és pontszámokkal. Egyetlen statikus HTML oldal, nincs build lépés és nincs függőség.

- **1–3. hely:** dobogó
- **4–10. hely:** top 10 nagy számokkal
- **11–175. hely:** teljes lista sávokra bontva, kereséssel, pontszám szerinti rendezéssel, rács és lista nézettel
- Egy sorozatra kattintva adatlap nyílik (bemutató éve, csatorna, műfajok, leírás)

## Megnézés

Nyisd meg az `index.html`-t böngészőben, vagy kapcsold be a GitHub Pages-t: **Settings → Pages → Deploy from a branch → `main` / root**.

## Poszterek

A posztereket és az adatokat az oldal a megnyitáskor tölti le a [TVmaze](https://www.tvmaze.com) nyilvános API-jából (CC BY-SA). Először a látható rész töltődik be, a teljes lista kb. másfél perc alatt. Utána a böngésző megjegyzi a posztereket.

Ha egy poszter rossz vagy hiányzik, az `index.html` elején a `DATA` listában add hozzá a sorozat sorához a saját képlinkedet:

```js
{"t":"Dark","s":10.0,"y":2017,"img":"https://.../dark.jpg"}
```

## Adatok

A `DATA` listában egy sor egy sorozat, a sorrend a helyezés.

| mező | jelentés |
|------|----------|
| `t`  | cím |
| `s`  | pontszám (1–10) |
| `y`  | bemutató éve (ez alapján választja ki a TVmaze-találatot) |
| `q`  | keresőkifejezések a TVmaze-hez, ha eltérnek a címtől |
| `img`| saját posztert állít be, ilyenkor nincs TVmaze-keresés |
