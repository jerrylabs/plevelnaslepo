# Návod na editaci webu

## Struktura souborů

- **Hlavní stránka** je v `index.md`
- **Podstránky** jsou ostatní MD soubory, např. obsah stránky `/o-mne` je v souboru `o-mne.md`
- **Obrázky** se nachází v `assets/images/`
- **Hlavní menu** lze najít v `_includes/menu.html`, kde se dá měnit text či pořadí jednolitvých položek

## Markdown front matter

Metadata stránky sloužící např. k určení šablony (`layout`), titulku stránky, příp. definici náhledů pro Facebook atp. se nacházejí na začátku HTML souborů mezi pomlčkami `---` a `---`. Na každém řádku se nachází název proměnné oddělené dvojtečkou od její hodnoty.

## Značky v markdownu

Zbytek MD souboru (pod druhým `---`) obsahuje text zobrazený na stránce formátovaný pomocí **Markdownu**

### Nadpisy

Hlavní nadpis stránky vznikne tak, že se před něj umístí `# `. Před nadpis druhé třídy `## `, třetí `### ` atp. Např. nadpisy použité v tomto návodu vypadají v Markdownu takto:

```
# Návod na editaci webu

## Značky v markdownu

### Nadpisy
```

### Odstavce

Odstavce se vzájemně oddělují dvojitým enterem.

### Zalomení řádku v odstavci

Řádkový zlom v rámci jednoho odstavce se vytvoří jedním enterem s tím, že na konci zalamovaného řádku se třeba napsat 2 mezery. Obyčejný enter Markdown velkoryse ignoruje.

### Nezalomitelná mezera

Zabránit zalomení řádku za předložkou či spojkou lze provést tak, že se v MD souboru mezi předložku a následující slovo místo mezery umístí vlnovka `~`. Např. `S~láskou` zajistí, že "S" nikdy nezůstane samo na konci řádku. 

### Odkazy

Odkaz vypadá takto:

```
[text odkazu](adresa odkazu)
```

Např. `[odkaz na gůgl](https://www.google.com)` se zobrazí jako [odkaz na gůgl](https://www.google.com). Pokud chceme otvírat odkazy v novém okně (tabu), je třeba za něj přidat ještě `{:target="_blank"}` - např  `[odkaz na gůgl v novém okně](https://www.google.com){:target="_blank"}`.

### Seznamy
Číslovaný seznam vznikne, když na začátek každého řádku číslo s tečkou (číslo může být jakékoliv, správné se automaticky). Položky nečíslovaného seznamu (s puntíky) začínají hvězdičkou. Příklady:

```
1. kytice
1. z údolí
1. Bystřice
```

1. kytice
1. z údolí
1. Bystřice

```
* jedna
* dvě
* Honza jde
```

* jedna
* dvě
* Honza jde

### Další formátování

**Tučné písmo** ohraničíme dvěma hvězdičkami. *Kurzívu* jednou hvězdičkou. Zdrojový kód předchozích vět vypadá takto:

```
**Tučné písmo** ohraničíme dvěma hvězdičkami. *Kurzívu* jednou hvězdičkou. 
```

### HTML

Bonus: V Markdownu by mělo fungovat i standardní HTML, čili všechno výše zmíněné formátování lze provést i standardními HMTL tagy jako `<a href="">`, `<ol>`, `<ul>`, `<p>`, `<b>`, `<br>`, atp.