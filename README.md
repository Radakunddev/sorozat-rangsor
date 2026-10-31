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

Ha egy poszter rossz vagy hiányzik, tedd a képet a `posters` mappába (vagy használj egy képlinket), és az `index.html` elején a `DATA` listában add hozzá a sorozat sorához:

```js
{"t":"Dark","s":10.0,"y":2017,"img":"posters/dark.webp"}
```

## Adatok

A `DATA` listában egy sor egy sorozat, a sorrend a helyezés.

| mező | jelentés |
|------|----------|
| `t`  | cím |
| `s`  | pontszám (1–10) |
| `y`  | bemutató éve (ez alapján választja ki a TVmaze-találatot) |
| `q`  | keresőkifejezések a TVmaze-hez, ha eltérnek a címtől |
| `season` | melyik évad plakátja legyen, pl. `[6,5]`: a 6. évadé, ha nincs, az 5.-é, ha az sincs, a sorozat posztere |
| `img`| saját poszter (a `posters` mappából vagy képlinkkel); az évet, csatornát és leírást ilyenkor is a TVmaze-ről tölti |
