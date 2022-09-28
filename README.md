# C語言學習筆記

### 基本架構
```C
#include<stdio.h>          //外部函示庫

int main(){                //主程式

    printf("Hello World"); //程式主題
    
    return 0;              //主程式結尾
}

```

### 常用格式控制字串
|'%'|字符格式|'\\'|控制格式|
|-|-|-|-|
|%s|替換為字串|\n|換行|
|%d|替換為十進位數字|\t|下一個水平位點（一個tab鍵）|
|%f|替換為符點數|\a|逼一聲|
|%c|替換為一個字元|\\'|一個單引號|
|%%|替換為一個%| \\\\ |一個倒斜線|

## 常用變數
![](https://miro.medium.com/max/1400/1*vacBGZ4E9MandE5CECup1g.png)

## 流程控制

### if條件判斷
```C
#include <stdio.h>

int main(void) {
    int input = 0;
    int remain = 0;

    printf("輸入整數：");
    scanf("%d", &input);

    remain = input % 2;
    if(remain == 1) {
        printf("%d 為奇數\n", input);
    }
    else {
        printf("%d 為偶數\n", input);
    }

    return 0;
}
```

```C
#include <stdio.h>
int main(){
int score = 0

printf("輸入分數：");
scanf("%d", & score);

if(score >= 90 && score <= 100){
    put("評級：A");
}

if else(score >= 80 && score < 90){
    put("評級：B");
}

if else(score >= 70){
    put("評級：C");
}

else{
    put("下課找老師");
}

return 0;
}

```
### switch條件判斷
```C
#include<stdio.h>

int main(){
    int score = 0;
    int level = 0;
    printf("請輸入成績：");
    scanf("%d,&score);
    level = score/10;
    
    switch(level){  //使用單字：switch case puts break default
        case 10;
        
        case 9;
        puts(
        break ;
       
        
        
}
    
    
    
    return 0;
}

```

### for迴圈
```

```

### while迴圈
```

```
### break、 continue、goto
