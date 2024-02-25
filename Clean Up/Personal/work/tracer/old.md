ini untuk akun Google & Login ke kemendikbud 
Username 	: minitracer22@gmail.com
Password 	: Tracerstudi_2022
Gmail backup Sementara : 311910008@student.machung.ac.id 

https://tracerstudy.kemdikbud.go.id/dashboard
Email 		: rubik@machung.ac.id
Password	: r03b1k1





```vb
=IFERROR(INDEX($A$2:$A$10; MATCH(0; INDEX(COUNTIF($B$1:B1; $A$2:$A$10)+(COUNTIF($A$2:$A$10; $A$2:$A$10)<>1);0;0); 0)); "")
```



```vb
Sheet1!$I$2:$I$3851
$I$1:I1
```

THE FIRST CELL OF AJ1 MUST NOT BE EMPTY
FORMULA ARE PLACED ON START WTIH AJ2, 3, 4, AND SO ON

```vb
=Sheet1!$K$2:$K$3851
```



# IGNORING BLANK
```vb
=IFERROR(INDEX($A$2:$A$10; MATCH(0; COUNTIF($B$1:B1; $A$2:$A$10&"") + IF($A$2:$A$10="";1;0); 0)); "")

=IFERROR(INDEX(Sheet1!$I$2:$I$3851; MATCH(0; COUNTIF($I$1:I1; Sheet1!$I$2:$I$3851&"") + IF(Sheet1!$I$2:$I$3851="";1;0); 0)); "")
```

# IGNORING BLANK AND NUMBER
```vb
=IFERROR(INDEX($A$2:$A$10, MATCH(0, COUNTIF($B$1:B1, $A$2:$A$10&"") + IF(ISTEXT($A$2:$A$10)=FALSE,1,0), 0)), "")
```


```vb
=IFERROR(INDEX(Sheet1!$J$2:$J$3851; MATCH(0; COUNTIF($J$1:J1; Sheet1!$J$2:$J$3851&"") + IF(ISTEXT(Sheet1!$J$2:$J$3851)=FALSE;1;0); 0)); "")
```




