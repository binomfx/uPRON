# uPRON - Synthetic Promissory Notes
### Lending Services Killer<br>

The aim of the project is to create a decentralized analogue of the promissory note.<br>

## Fiat definitions
From [Investopedia](https://www.investopedia.com/terms/p/promissorynote.asp):
>A promissory note is a debt instrument that contains a written promise by one party (the note's issuer or maker) to pay another party (the note's payee) a definite sum of money, either on-demand or at a specified future date. A promissory note typically contains all the terms pertaining to the indebtedness, such as the principal amount, interest rate, maturity date, date and place of issuance, and issuer's signature.<br>
>Although financial institutions may issue them—for instance, you might be required to sign a promissory note in order to take out a small personal loan—promissory notes **usually allow companies and individuals to get financing from a source other than a bank**. This source can be an individual or a company willing to carry the note (and provide the financing) under the agreed-upon terms. In effect, promissory notes can enable anyone to be a lender.<br>

![image](https://user-images.githubusercontent.com/25432493/142755603-8b7ed6e7-971e-4c6c-9fce-484d53d7e043.png)

In the fiat world, the circulation of promissory notes is regulated by the [UNIFIED LAW ON BILLS OF EXCHANGE AND PROMISSORY NOTES](https://github.com/binomfx/uPRON/blob/main/UNIFORM_LAW_FOR_BILLS_OF_EXCHANGE_AND_PROMISSORY_NOTES).<br>
The important parameters and provisions of the promissory note are listed in the following quote from the [UNIFIED LAW ON BILLS OF EXCHANGE AND PROMISSORY NOTES](https://github.com/binomfx/uPRON/blob/main/UNIFORM_LAW_FOR_BILLS_OF_EXCHANGE_AND_PROMISSORY_NOTES):
>A promissory note contains:
>1. The term 'promissory note' inserted in the body of the instrument and expressed in the language employed in drawing up the instrument;
>2. An unconditional promise to pay a determinate sum of money;
>3. A statement of the time of payment
>4. A statement of the place where payment is to be made
>5. The name of the person to whom or to whose order payment is to be made;
>6. A statement of the date and of the place where the promissory note is issued;
>7. The signature of the person who issues the instrument (maker).
>
>The following provisions relating to bills of exchange apply to promissory notes so far as they are not inconsistent with the nature of these instruments, viz:
>- Endorsement (Article 11 to 20);
>- Time of payment (Articles 33 to 37);
>- Payment (Articles 38 to 42);
>- Recourse in case of non-payment (Articles 43 to 50, S2 to 54);
>- Payment by intervention (Articles 55, 59 to 63);
>- Copies (Articles 67 and 68);
>- Alterations (Article 69);
>- Limitation of actions (Articles 70 and 71);
>- Holidays, computation of limits of time and prohibition of days of grace (Articles 72, 73 and 74).
>
>The following provisions are also applicable to a promissory note: 
>- The provisions concerning a bill of exchange payable at the address of a third party or in a locality other than that of the domicile of the drawee (Articles 4 and 27): stipulation for interest (Article 5); 
>- discrepancies as regards the sum payable (Article 6); 
>- the consequences of signature under the conditions mentioned in Article 7, the consequences of signature by a person who acts without authority or who exceeds his authority (Article 8); 
>- and provisions concerning a bill of exchange in blank (Article 10).
>
>The following provisions are also applicable to a promissory note: 
>- Provisions relating to guarantee by aval (Articles 30-32); 
>- in the case provided for in Article 31, last paragraph, if the aval does not specify on whose behalf it has been given, it is deemed to have been given on behalf of the maker of the promissory note.

## Synt Idea
Создать синтетический токен, функционирующий аналогично простому векселю, обеспеченный токенами USDC.<br> 
Срок инструмента соответствует сроку погашения векселя.<br>
Цена синтетического токена привязана к дисконту и по мере приближения срока погашения приближается к стоимости обеспечения.<br>
Индосамент - блокчейн. !!! можно ли сделать солидарную ответственность все, через чьи руки прошел вексель?<br>

### Электронный вексель.
Вексель представляет собой очень удобный и продуманный инструмент расчетов, по нему наработана огромная практика. Реализовать обращение векселей на блокчейне было бы очень интересно и полезно.
Обращение векселей определяется ***Женевской конвенцией 1930 года***, имеющей целью разрешение некоторых коллизий законов о переводных и простых векселях.
Ст. 3 этой Конвенции устанавливает:
``
Форма, в которой приняты обязательства по переводному или простому векселю, определяется законом той страны, на территории которой эти обязательства были подписаны.
``
Если обязательства по векселю были подписаны в месте где векселя в электронном виде не запрещены, но такой вексель в силу положений Женевской конвенции 1930 года, имеющая целью разрешение некоторых коллизий законов о переводных и простых векселях будет действительным везде, в том числе в юрисдикциях, требующих подписания векселя исключительно в бумажной форме. 
Например, выпуск таких электронных векселей в соответствии с нормами английского права возможен на платформе cryptonomica.net/bills-of-exchange (см. описание на русском). Место выпуска векселя и платежа по векселю при этом может быть в Великобритании, однако такие ЦФА могут приобретаться и отчуждаться российскими резидентами через оператора обмена цифровых финансовых активов, и возможен их вариант обращения в централизованной информационной системе оператором которой является резидент РФ в соответствии с положениями Закона.

## Two-side market
***Покупатель*** - выпускает вексель, обеспеченный не более чем на 100% токенами (допущенными в качестве коллатерал в UMA)
***Продавец*** - получает вексель в качестве оплаты за товар, сжигает его и получает токены коллатерал, которые может обменять на фиатную валюту.<br>
Если вексель обеспечен менее чем на 100%, то у Покупателя (выпустившего вексель) имеется обязательство довести обеспечение до 100% к моменту экспирации. В этом случае, Продавец сможет получить 100% номинала векселя только при насуплении экспирации.

## Architecture

## Interface

