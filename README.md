<div align="center">

## Shopping Cart


</div>

### Description

This is an Internet Shopping Cart which is an Accounting and E-Commerce Application
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[martin castañeda](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/martin-casta-eda.md)
**Level**          |Intermediate
**User Rating**    |3.9 (27 globes from 7 users)
**Compatibility**  |VbScript \(browser/client side\)

**Category**       |[Math](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/math__4-12.md)
**World**          |[ASP / VbScript](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/asp-vbscript.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/martin-casta-eda-shopping-cart__4-6136/archive/master.zip)





### Source Code

```
<HTML>
<CENTER>
<FONT SIZE=5>
Martin's Shopping Cart Sample
</FONT>
</CENTER>
<BR><BR>
<FORM NAME=SHOPPINGCARTFORM METHOD=POST ACTION=http://www6.ewebcity.com/martincastaneda/grocery.asp>
<PRE>
Name   : <INPUT NAME=NAME SIZE=30>
Email   : <INPUT NAME=EMAIL SIZE=30>
Telephone : <INPUT NAME=TELEPHONE SIZE=30>
Address  : <INPUT NAME=ADDRESS SIZE=50>
Item   : <SELECT NAME=ITEMX>
         <OPTION VALUE=Empty>Empty
         <OPTION VALUE=Bread>Bread
         <OPTION VALUE=Pampers>Pampers
         <OPTION VALUE=Milk>Milk
         <OPTION VALUE=Ice_Cream>Ice_Cream
      </SELECT>
Price   : <INPUT NAME=PRICE VALUE=0.00>
Quantity : <INPUT NAME=QUANTITY VALUE=1>
Amount  : <INPUT NAME=AMOUNT VALUE=0.00>
      <INPUT TYPE=BUTTON NAME=ADD VALUE="Add to Cart">
Transaction
<TEXTAREA NAME=TRANSACTION COLS=50 ROWS=20></TEXTAREA>
Total   : <INPUT NAME=TOTAL VALUE=0.00>
      <INPUT TYPE=RESET VALUE=Reset><INPUT TYPE=SUBMIT VALUE=Submit>
</PRE>
</FORM>
<SCRIPT LANGUAGE=VBSCRIPT>
<!--
SET ENTRYFORM = DOCUMENT.SHOPPINGCARTFORM
SUB ADD_OnClick
   ENTRYFORM.TRANSACTION.VALUE = ENTRYFORM.TRANSACTION.VALUE + "Item    : " + ENTRYFORM.ITEMX.VALUE + VBCRLF
   ENTRYFORM.TRANSACTION.VALUE = ENTRYFORM.TRANSACTION.VALUE + "Price    : " + ENTRYFORM.PRICE.VALUE + VBCRLF
   ENTRYFORM.TRANSACTION.VALUE = ENTRYFORM.TRANSACTION.VALUE + "Quantity  : " + ENTRYFORM.QUANTITY.VALUE + VBCRLF
   ENTRYFORM.TRANSACTION.VALUE = ENTRYFORM.TRANSACTION.VALUE + "Amount   : " + ENTRYFORM.AMOUNT.VALUE + VBCRLF + VBCRLF
   ENTRYFORM.TOTAL.VALUE = FORMATNUMBER(CINT(ENTRYFORM.TOTAL.VALUE) + CINT(ENTRYFORM.AMOUNT.VALUE), 2)
END SUB
SUB QUANTITY_OnChange
   CALL COMPUTE
END SUB
SUB COMPUTE
   ENTRYFORM.AMOUNT.VALUE = FORMATNUMBER(CINT(ENTRYFORM.PRICE.VALUE) * CINT(ENTRYFORM.QUANTITY.VALUE), 2)
   TOTALAMOUNT = CINT(ENTRYFORM.TOTAL.VALUE) + CINT(ENTRYFORM.QUANTITY.VALUE)
END SUB
SUB ITEMX_OnChange
   IF ENTRYFORM.ITEMX.SELECTEDINDEX = 0 THEN ENTRYFORM.PRICE.VALUE = "0.00"
   IF ENTRYFORM.ITEMX.SELECTEDINDEX = 1 THEN ENTRYFORM.PRICE.VALUE = "10.00"
   IF ENTRYFORM.ITEMX.SELECTEDINDEX = 2 THEN ENTRYFORM.PRICE.VALUE = "20.00"
   IF ENTRYFORM.ITEMX.SELECTEDINDEX = 3 THEN ENTRYFORM.PRICE.VALUE = "30.00"
   IF ENTRYFORM.ITEMX.SELECTEDINDEX = 4 THEN ENTRYFORM.PRICE.VALUE = "40.00"
   ENTRYFORM.QUANTITY.VALUE = "1"
   ENTRYFORM.QUANTITY.VALUE = INPUTBOX("Input Quantity of " + ENTRYFORM.ITEMX.VALUE, "Quantity", ENTRYFORM.QUANTITY.VALUE)
   CALL COMPUTE
END SUB
-->
</SCRIPT>
</HTML>
```

