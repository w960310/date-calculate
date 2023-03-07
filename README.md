# date-calculate

112/02/28|決算日|  
112/01/31|上月底|=LEFT($B$3,7)&DAY(EOMONTH($B$13,-1))  
112/01/01|上月初|=IF(MID($B$1,5,2)-1<1,MID($B$1,1,3)-1&"/"&$B$10,MID($B$1,1,3)&"/"&$B$10)  
111/02/28|去年同期決算日|=MID($B$1,1,3)-1&"/"&MID($B$1,5,2)&"/"&DAY(EOMONTH($B$13,-12))  
112/02|決算月|=MID($B$1,1,3)&MID($B$1,4,3)  
111/02|去年同月|=MID($B$1,1,3)-1&MID($B$1,4,3)  
11202|決算年月(無/)|=MID($B$1,1,3)&MID($B$1,5,2)  
03/01|下月初(月日)|=IF(LEN($B$11)<5,"0"&$B$11,$B$11)  
02/28|決算日(月日)|=MID($B$1,5,5)  
01/01|上月初(月日)|=IF(LEN($B$12)<5,"0"&$B$12,$B$12)  
3/01|下月初(未補齊)|=IF(MID($B$1,5,2)+1>12,MID($B$1,5,2)+1-12,MID($B$1,5,2)+1)&"/01"  
1/01|上月初(未補齊)|=IF(MID($B$1,5,2)-1<1,MID($B$1,5,2)-1+12,MID($B$1,5,2)-1)&"/01"  
2023/02/28|決算日(西元)|= TEXT(DATE(MID($B$1,1,3)+1911,MID($B$1,5,2),MID($B$1,8,2)),"yyyy/mm/dd")  
112/3/31|決算日(當日判斷)|=IF(DAY(TODAY())*1<7,YEAR(EOMONTH(TODAY(),-1))-1911&"/"&MONTH(EOMONTH(TODAY(),-1))&"/"&DAY(EOMONTH(TODAY(),-1)),YEAR(EOMONTH(TODAY(),0))-1911&"/"&MONTH(EOMONTH(TODAY(),0))&"/"&DAY(EOMONTH(TODAY(),0)))  

111 (11)|"&$B$16&"|=LEFT($B$26,3)&" ("&MID($B$26,5,2)&")"  
111 (12)|"&$B$17&"|=LEFT($B$20,3)&" ("&MID($B$20,5,2)&")"  
112 (01)|"&$B$18&"|=LEFT($B$2,3)&" ("&MID($B$2,5,2)&")"  
112 (02)|"&$B$19&"|=MID($B$1,1,3)&" ("&MID($B$1,5,2)&")"  
111/12/31||=LEFT($B$21,7)&DAY(EOMONTH($B$13,-2))  
111/12/01||=IF(MID($B$1,5,2)-2<1,MID($B$1,1,3)-1&"/"&$B$22,MID($B$1,1,3)&"/"&$B$22)  
12/01||=IF(LEN($B$23)<5,"0"&$B$23,$B$23)  
12/01||=IF(MID($B$1,5,2)-2<1,MID($B$1,5,2)-2+12,MID($B$1,5,2)-2)&"/01"  
112/03/31|下月底|=LEFT($B$25,7)&DAY(EOMONTH($B$13,1))  
112/03/01|下月初|=IF(MID($B$1,5,2)+1>12,MID($B$1,1,3)+1&"/"&$B$8,MID($B$1,1,3)&"/"&$B$8)  
111/11/30||=LEFT($B$27,7)&DAY(EOMONTH($B$13,-3))  
111/11/01||=IF(MID($B$1,5,2)-3<1,MID($B$1,1,3)-1&"/"&$B$28,MID($B$1,1,3)&"/"&$B$28)  
11/01||=IF(LEN($B$29)<5,"0"&$B$29,$B$29)  
11/01||=IF(MID($B$1,5,2)-3<1,MID($B$1,5,2)-3+12,MID($B$1,5,2)-3)&"/01"  
11202|"&$B$30&"|=MID($B$1,1,3)&MID($B$1,5,2)  
11201|"&$B$31&"|=LEFT($B$2,3)&MID($B$2,5,2)  
11112|"&$B$32&"|=LEFT($B$20,3)&MID($B$20,5,2)  
112|當前決算月(年份)|=LEFT($B$1,3)  
112|上個決算月(年份)|=LEFT($B$2,3)  
111|上上決算月(年份)|=LEFT($B$20,3)  
2023/01/31|上個決算日(西元)|= TEXT(DATE(MID($B$2,1,3)+1911,MID($B$2,5,2),MID($B$2,8,2)),"yyyy/mm/dd")  
2022/12/31|上上決算日(西元)|= TEXT(DATE(MID($B$20,1,3)+1911,MID($B$20,5,2),MID($B$20,8,2)),"yyyy/mm/dd")  
2302|當前決算月(西年月)|=MID($B$13,3,2)&MID($B$13,6,2)  
2301|上個決算月(西年月)|=MID($B$36,3,2)&MID($B$36,6,2)  
2212|上上(西年月)|=MID($B$37,3,2)&MID($B$37,6,2)  
202302||=LEFT($B$13,4)&MID($B$13,6,2)  
202301||=LEFT($B$36,4)&MID($B$36,6,2)  
202212||=LEFT($B$37,4)&MID($B$37,6,2)  
   
