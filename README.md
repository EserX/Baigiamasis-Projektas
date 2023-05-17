
# Automobilių kainos prognozavimo baigiamasis projektas
Šis projektas skirtas automobilių kainų prognozavimui naudojant mašininį mokymąsi.

## Projekto aprašymas
Šio projekto tikslas yra sukurti modelį, kuris gali prognozuoti automobilių kainas pagal įvairius parametrus, tokius kaip metai, variklio galingumas, rida ir t.t. 


## Duomenų rinkinys
Projekte naudojami duomenys gauti pasitelkiant web-scraping metodą iš automobilių skelbimų portalų:
-Autoplius.lt
-Autobilis.lt
-Autogidas.lt 

## Duomenų apdorojimas
Prieš pradedant modelio kūrimą, duomenys yra apdorojami naudojant 'pandas' biblioteką. Pagrindiniai žingsniai:
-Duomenų pažiūrėjimas ir supratimas apie jų struktūrą ir turinį.
-Pašalinami arba užpildomi trūkstami duomenys.
-Išskirtys yra pašalinamos supratus nelogiškas kainos reikšmes ir naudojant z balus.
-Kategoriniai kintamieji yra konvertuojami į dummy kintamuosius arba koduojami naudojant OneHotEncoder.
-Skaitiniai kintamieji yra standartizuojami naudojant StandardScaler.

## Šiame projekte yra taikomi trys skirtingi mašininio mokymosi modeliai:
-Linear Regression
-Decision Tree
-Random Forest
Modeliai yra treniruojami naudojant treniravimosi duomenis, o tada yra atliekamos prognozės naudojant testavimo duomenis santykiu 80/20. Galiausiai yra įvertinamas kiekvieno modelio efektyvumas naudojant šaknies iš vidutinės kvadratinės paklaidos (RMSE). Taip pat yra atliekami parametrų optimizavimo metodai, tokiu būdu ieškant geriausių modelio parametrų, naudojama RandomizedSearchCV ir GridSearchCV.

## Rezultatai
Geriausias rezultatas buvo pasiektas naudojant Random Forest modelį su GridSearchCV hiperparametrų optimizavimu. Šis modelis pasiekė mažiausią RMSE ir aukštą R-kvadrato rezultatą, tai reiškia, kad jis gerai prognozuoja automobilių kainas pagal turimus duomenis.

## Naudojamos bibliotekos
Naudojamos bibliotekos pridedamos į requirements.txt failą.

## Autorystė
Šį projektą sukūrė Ričardas Baliutis kaip CODE ACADEMY mašininio mokymosi užduoties galutinį projektą.
