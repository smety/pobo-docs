# Kódování nových widgetů

Widgety (HTML bloky) se stylují metodikou [BEM](https://www.vzhurudolu.cz/prirucka/bem) a dále se využívají funkce z
  [Bootstrap 4](https://getbootstrap.com/docs/4.0/getting-started/introduction/).

## Jmenné konvence a příklady 

Všechny widgety musejí při definování tříd v CSS obsahovat prefix `.rc-*` (např. `.rc-conversion-three {}`). Název by 
měl vystihovat stručný popis komponent. 

## Postup při vytváření komponent

1. Naklonujeme si repozitář `git clone git@github.com:smety/pobo-docs.git`
2. Nainstalujeme závislosti `npm install` 
3. Vytvoříme si novou větev `git checkout -b component-abcd/master`
4. V adresáři `widget` si vytvořte nový SASS soubor s názvem widgetu (např. `gift-rating.scss`)
5. V adresáři `html`si vytvoříme nový HTML soubor s totožným názvem jako SASS (`gift-rating.html`)

Zkopírujeme do něj:

```html
<!DOCTYPE html>
<html lang="cs">
<head>
  <meta charset="UTF-8">
  <title></title>
  <link rel="stylesheet" type="text/css" href="./../css/gift-rating.css">
</head>
<body>
<div class="gift-rating">
  <!-- ... my HTML code -->
</div>
</body>
</html>
```

6. Spustíme `npm run dev` a nakódujeme HTML šablonu 
7. Commitneme a pushneme 

## Seznam komponent 

```
├── advantages-three.scss - 3 bloky s nadpisy a textem vedle sebe 
├── header-text.scss -  Velký nadpis a pod ním velký text  
├── image-half-left.scss  50/50 (obrázek v vlevo a text v pravo) 
├── image-half-right.scss -  50/50 (obrázek v pravo a text v vlevo) 
├── image-left.scss -  Text v pravo a obrázek vlevo 
├── image-right.scss -  Text v vlevo a obrázek v pravo 
├── rating-two.scss - Klady a zápory
└── text.scss - Klasický dlouhý text
```
