# Vaja4-interrupt-button-STM32F0
<h4> Glede na vašo razvojno ploščico in razširitveno vezje s tipkami, izberite ustrezen digitalni vhod kot interrupt (GPIO_EXT…) in izhod za zeleno LED. Zapišite izbrana pina: </h4>
<p> GPIO_EXTI0 -> PA0 ter zelena led PC9 in modra led PC8. </p>
<h4> Znotraj te funkcije zapišite ukaz za vklop/izklop zelene LED </h4>
<p> HAL_GPIO_TogglePin(GPIOC,GPIO_PIN_9). </p>
<h4> Znotraj iste funkcije dodajte še zakasnitev, ki je potrebna, ko uporabimo mehanska tipkala/stikala: for(uint32_t i=0; i<10000; i++); Koliko znaša (v mili sekundah) zapisana zakasnitev? </h4>
<p> Zakasnitev znaša 500ms. </p>
<h4> V user code begin 3 - zanka while(1) - zapišite ukaz za utripanje modre LED. </h4>
<p> HAL_GPIO_TogglePin(GPIOC,GPIO_PIN8);. </p>
<h4> V to zanko dodajte ukaz za zakasnitev z funkcijo Delay iz knjižnice HAL, in sicer pol sekunde.</h4>
<p> HAL_Delay(500).</p>
<h4> Opazujte delovanje (utripanje modre LED). Kaj se zgodi, ko pritisnemo na modro tipko na STM32F0? </h4>
<p> Modra LED vedno utripa, ko pa pritisnemo na modro tipko se pa prižge še zelena LED. </p>
<h4> Ali pritisk na modro tipko vpliva na utripanje modre LED in zakaj? </h4>
<p> Ne vpliva na utripanje modre LED saj je zelena LED samo interrupt za zeleno LED. </p>
<h4> Komentar </h4>
<p> Če smo navodila pravilno upoštevali bo morala modra LED vedno utripati zelena se pa prižge in ugasne samo takrat ko pritisnemo na modro tipko. </p>
