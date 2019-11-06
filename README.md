## 3.3 Traveling salesman problem
# Skupina 9: Double-tree algorithm and Christofides’ algorithm for metric TSP (1 or 2 students)

Študenta: Urh Peček, Jan Škoberne

# Predstavitev problema:

V svoji projektni nalogi bova obravnavala metrično različico problema potujočega trgovca.
Programirala bova v programu Sage.

Problem potujočega trgovca smo spoznali že lansko leto pri predmetu Optimizacijske metode. Problem nas sprašuje, katera je, glede na seznam mest in danih razdalj med posameznimi mesti, najkrajša pot, ki obišče vsa mesta in se vrne v prvotno mesto.
Problem potujočega trgovca je NP-težek problem. To so problemi, pri katerih lahko učinkovito preverimo, ali je rešitev pravilna, vendar za reševanje ne poznamo učinkovitih algoritmov in ne verjamemo da obstajajo.

# Pristop h reševanju problema:

Problem potujočega trgovca bova modelirala kot neusmerjen graf, kjer vozlišča predstavljajo mesta, poti med mesti pa so povezave grafa, kjer je razdalja med mestoma dana s težo povezave. Torej imamo utežen graf.
Gre za težavo z minimizacijo, ki se začne in konča v določeni točki, potem ko smo vmes obiskali vsa druga vozlišča grafa natančno enkrat. Iskala bova torej cikel, katerega povezave imajo najmanjšo težo. 

Kot prvo bova izvedla algoritem za reševanje problema za drevo z minimalno težo.
Drevo z minimalno težo je podmnožica povezav povezanega, obteženega (uteži na povezavah) in usmerjenega ? grafa, ki povezuje vsa vozlišča, je brez ciklov in ima najmanjšo skupno težo povezav.
Na njem bova dobila točne rezultate problema za različne grafe. Grafi bodo v prostorih različnih dimenzij, z različno veliko oglišči in cenami povezav med njimi.
Nato bova napisala program za algoritem z dvojnim drevesom in Christofidesov algoritem.

Slednja algoritma vrneta zgolj približek za optimalno rešitev potujočega trgovca.
Pognala jih bova na identičnih manjših grafih kot zgornjega, ki vrne točen rezultat. 
Algoritma bova primerjala med sabo in ugotavljala na katerih grafih deluje bolje eden in na katerih drugi, vendar za večje grafe ne bova mogla dobiti točnega rezultata.
Grafi, ki jih bova uporabljala bodo morali biti dovolj enostavni, sicer algoritem za reševanje problema z minimalno težo ne bo deloval, ker bi za optimalno rešitev porabil preveč časa.
