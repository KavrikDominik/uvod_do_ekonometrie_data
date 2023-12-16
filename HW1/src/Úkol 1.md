
---




![[Screenshot 2023-12-14 at 8.36.45.png|500]]


### 2)
Odhad koeficientu l_lotsize s intervaly spolehlivosti: $0.2454$. Vypočet intervalu spolehlivosti: 
$$0.2454 \pm  1.96 * 0.0669$$

---
### 3 
#### a)

Test, zdali jsou domy se sklepem dražší oproti vhodně zvolené *jednostranné* alternativě:

$$H_0: \beta_5 = 0$$$$H_1: \beta_5 < 0$$
Výpočet p-hodnoty: $$ \text{p-hodnota testu} = \frac{\text{p-hodnota \textit{fullbase}}}{2} = 0.00555$$

Zamítáme $H_0$ na 5 $\%$ hladině významnosti.

---

### 4
#### a)  

Otázka: Je elasticita ceny domu vzhledem k rozloze jeho pozemku je rovna jedné?

$$ H_0: \beta_1 = 1 $$
$$ H_1: \beta_1 \neq 1 $$
**2 způsoby:**
- t-test 
- test lineárních restrikcí (F-test)
#### b) 
Výpočet t-statistiky pro nulovou hypotézu (a)
$$\text{t-statistika} = \frac{\hat{\beta}_1 - 1}{se(\beta_1)} = -11.28$$

Test lineárních restrikcí v Gretlu:

![[Pasted image 20231216122026.png|500]]
![[Pasted image 20231216122313.png|500]]

![[Pasted image 20231216122437.png|500]]

Závěr: Zamítáme H_0 na 1% hladině významnosti


---
#### 5.

Test sdružené významnosti dummy proměnných:

V Gretlu v Modelu: testy > vynechání proměnných a tam zvolíte všechny dummy proměnné v modelu:
![[Pasted image 20231216123207.png|500]]

Výsledek:

![[Pasted image 20231216123526.png|500]]
#### a)
$\text{F-stat. = 10.3}$
#### b)
DF1 (čitatel F statistiky): 3
#### c) 
DF2 (jmenovatel): 76 

### d) 
Kritická hodnota z tabulek: 

![[Pasted image 20231216124256.png|350]]

### 5. e)

Zamítáme $H_0$ na 1% hladině výzmanosti.

---

### 6.
Test, zdali má příjezdová cesta stejný vliv na cenu jako sklep.
#### 6. a)

$$H_0: \beta_4 = \beta_5$$
$$H_1: \beta_4 \neq \beta_5$$
#### 6. b) 
Opět v původním odhadnutém modelu: Testy > lineární restrikce:


![[Pasted image 20231216130606.png|500]]

![[Pasted image 20231216130630.png|500]]


![[Pasted image 20231216130518.png|500]]

#### 6. c)
Nezamítáme $H_0$ na 5% hl. významnosti

---
### 7.

Model:

$$log(wage) = \beta_0 + \beta_1 age + \beta_2 age^2 + \beta_3educ + \beta_4 married + \beta_5female + \beta_6 urban + \beta_7 (female\times urban) + u$$
#### 7.a)

bod zlomu a tvar: potřebujeme získat $\hat{\beta}_2$ a $\hat{\beta_3}$:

![[Pasted image 20231216145251.png|500]]

Podmínka pro maximum vzhledem k proměnné *age*:
$$\frac{\partial log(wage)}{\partial age} = 0$$

$$0.0632 + 2 \times -0.000676 \times age = 0$$
Vyjádřením *age* získáme bod zlomu v efektu věku na logaritmickou mzdu:
$$age = 46.74$$ 

### 8
#### 8.a)

Je dán aproximativní vztah:
$$\% \Delta \approx 100 \times (\beta_1 + 2 \beta_2 age) \Delta age)$$

Zde je podle zadání:

*"Najděte mezní efekt třicátého a dvaačtyřicátého roku života na mzdu (efekt jednoho dodatečného roku stáří pro dva různé referenční věky)"*.

Bez informace v závorce by se zdálo, že je otázka na mezní efekt 30. a 42. roku, tudíž bychom dosazovali do vzorce za age 29 a 41. Informace v závorce ale říká, že zadané roky máme brát jako referenční a vlastně tím zkoumáme efekt zestárnutí z 30 na 31 a ze 42 na 43. Dle úkolu se tedy mělo dosazovat 30 a 42, ale při hodnocení jsem uznával i výsledky po dosazení 30 a 42.

#### 8. b)
Mezní efekt dodatečného roku při 30 letech věku:

$$\% \Delta \approx 100 \times (\beta_1 + 2 \beta_2 age) \Delta age)$$$$100 * (0.0632 + (2* (-0.000676) * 30)) = 2.263\%$$
#### 8. c)
Mezní efekt dodatečného roku při 42. letech věku:
$$\% \Delta \approx 100 \times (\beta_1 + 2 \beta_2 age) \Delta age)$$$$100 * (0.0632 + (2* (-0.000676) * 42)) = 0.6405 \%$$

---

### 9.
#### 9. a) 

Efekt pro vesnici: 

$$(e^{\hat{\beta}_5}-1)\times100$$
$$ (e^{-0.28}-1 )*100 = -24.42 \; \% $$
#### 9. b)

Efekt pro město:

$$(e^{\hat{\beta}_5 +\hat{\beta}_7} - 1) \times 100 $$
$$(e^{-0.28 + 0.031}- 1) \times 100  = 22.04 \;\% $$



#### 9. d) 
Interval spolehlivosti pro součet parametrů:

![[Pasted image 20231216153506.png|400]]




$$\text{CI spodní mez }= (exp(-0.249 - 1.96 * 0.031) - 1 ) \times 100$$
$$\text{CI spodní mez
}= -26.72 \%$$

$$\text{CI horní mez }= (exp(-0.249 + 1.96 * 0.031) - 1 ) \times 100$$
$$\text{CI horní mez }= -17,07$$



 ---

### 10.

#### 10. a

$$H_0:\; \beta_7 = 0$$
$$H_1:\; \beta_7 \neq 0$$


#### 10. b)


![[Pasted image 20231216155405.png|500]]


#### 10. c)

Nezamítáme $H_0$.






