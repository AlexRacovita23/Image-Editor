# Image-Editor
This repo contains a basic .bmp image editor. It can insert other images on the current picture, draw lines and fill image segments with a certain colour.

Task 0:
	Pentru consola interactiva mi-am luat instructiunea curenta, am parsat-o si am pus-o intr-o matrice.
Am folosit strcmp pentru a identifica operatia si dupa am apelat-o cu parametrii necesari.

Task 1:
	Pentru operatia de edit in functia de citire, am citit File Header si Info Header cu o singura instructiune de fread,
citind din fisier exact numarul necesari de octeti. Iar pentru fiecare pixel din matrice am procedat la fel pentru a citi
cate 3 octeti deodata.
	Pentru operatia de scriere a imaginii am procedat la fel, intai scriind toti octetii pentru header si infoheader
si scriind cate 3 octeti pentru fiecare pixel. Dupa fiecare linie am avut grija sa adaug paddingul necesar.

Task 2:
	Pentru operatia de insert am folosit functia de memcpy pentru a copia pe rand fiecare linie de pixeli din imaginea 
de inserat in imaginea editata la pozitia corespunzatoare de pe coloana. Am folosit verificarile necesare pentru a nu iesi
in afara imaginii.

Task 3:
	Pentru desenarea unei linii identific daca ea trebuie parcursa pe ox sau oy. In ce functie de parcurgere imi scot 
fiecare pereche (i,j) de pixeli care trebuie editati folosindu-ma de ecuatia dreptei care uneste cele doua capete ale dreptei.
Pentru perechea (i,j) apelez o functie care imi deseaza toti pixeli din patratul cu latura line_width si centrul in (i,j).
	Pnetru a desena drepunghiuri si triunghiuri ma folosesc de functia de desenare unei linii. 

Task 4:
	Operatie Fill este implementata recursiv, desenand pixelul curent, apoi autoapelandu-se pentru vecinii acestuia. Se 
opreste cand nu mai are pixeli de modificat.


