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
|中文|型態名|佔用空間|範圍|輸出入方法|
|-|-|-|-|-|
|字元|char|1byte|-128~127|%c(文字),%hhd(數字)|
|短整數|short|2byte|-32768~32767|%hd|
|整數|int|4byte|-2147483648~2147483648|%o(8進位),%d(10進位),%x(16進位)|
|長整數|long (int)|4byte|-2147483648~2147483648|%ld|
|長長整數|long long (int)|8byte|-9x10^18~9x10^18|%lld|
|無號整數|unsigned (int)|4byte|0~4294967295|%u|
|浮點數|float|4byte|-3.402823668x10^38~3.402823668x10^38|%f|
|雙精度浮點數|double|8byte|-1.7976931348x10^308~1.7976931348x10^308|%lf|


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
    scanf("%d",&score);
    level = score/10;
    
    switch(level){  //使用單字：switch case puts break default
        case 10:
        	
        case 9: 
        	puts("評級：A");
        	break ;
        
        case 8: 
        	puts("評級：B");
        	break ;
        
        case 7: 
        	puts("評級：C");
        	break ;
       
       default:
       		puts("下課找老師");
        
        }  
    return 0;
}

```

### for迴圈
```C
#include<stdio.h>

int main(){
    for(int i=1;i<10;i++){
        printf("%d",i);
    }

    return 0;
}

```

```C
#include<stdio.h>

int main(){
    for(int i=1;i<10;i++){       
	    for(int j=2;j<10;j++){
            printf("%d*%d=%2d ",j,i,j*i); //%2d在一位數左邊補空格 %3d在一位數字左邊補兩格 兩位數字補一格 
         }
         
         puts("");
    }

    return 0;
}
```
### while迴圈
```C
//算平均
#include<stdio.h>

int main(){
    double score = 0;
    int sum = 0;
    int count = -1;
    
    while(score != -1){ 		//若符合條件,則繼續迴圈
	count++;
	sum += score;
	printf("輸入成績（輸入-1結束）");
	scanf("%lf",&score);
    }
    
printf("平均：%lf",(double)sum/count);

return 0;
}
```
```C
#include<stdio.h>	 //do while迴圈
int main(){
	double score,sum;
	int replay = 0;
	do{
		printf("輸入分數");
		scanf("%lf",&score);
		sum=sum+score;
		
		printf("是否要繼續?Yes:1 No:0\n");
		scanf("%d",&replay);
	}while(replay);		//若符合條件，則結束迴圈
	
	printf("您的總分為:%.2lf",sum);
	
	return 0;
}
```
### break、 continue、goto
break 可以離開目前switch、for、while、do while區塊，並前進至區塊後下一個陳述句
countinue 與break類似，主要用於迴圈，所不同的是break會結束區塊的執行，而countinue只會結束接下來區塊中的陳述句，跳回至迴圈區塊的開頭繼續下一個迴圈，而不是離開迴圈
```C
#include<stdio.h> 

int main(){

    for(int i=1;i<10;i++){    
	if(i==5){
		break;
	}
	
	printf("%d ",i);
    }
    
return 0;
}

```



```C
#include<stdio.h> 

int main(){

    for(int i=1;i<10;i++){    
	if(i==5){
		continue;
	}
	
	printf("%d ",i);
    }
    
return 0;
}

```
```C
#include<stdio.h>

int main(){

return 0;
}
```
# 進階型態

## 陣列與字串

## 指標

## 副程式

### 回傳值;有return 
```C
#include<stdio.h>

int add(int a,int b);

int main(){
	int a,b;
	printf("請輸入數字:");
	scanf("%d",&a);
	printf("請輸入數字:");
	scanf("%d",&b);
	printf("相加結果為:%d",add(a,b));
	 
	return 0;
}

int add(int a,int b){
	return a+b;
}
```

### 不回傳值;沒有return
```C
#include<stdio.h>

void add(int a,int b);

int main(){
	int a,b;
	printf("請輸入數字:");
	scanf("%d",&a);
	printf("請輸入數字:");
	scanf("%d",&b);
	add(a,b);
	 
	return 0;
}

void add(int a,int b){
	printf("相加結果為:%d",a+b);
}
```
### 全域變數富程式寫法
```C
#include<stdio.h>

int add();
int a,b;

int main(){

	printf("請輸入數字:");
	scanf("%d",&a);
	printf("請輸入數字:");
	scanf("%d",&b);
	printf("相加結果為:%d",add());
	 
	return 0;
}

int add(){
	return a+b;
}
```
```C
#include<stdio.h>
void add();
int a,b;
int main(){

	printf("請輸入數字:");
	scanf("%d",&a);
	printf("請輸入數字:");
	scanf("%d",&b);
	add();
	 
	return 0;
}

void add(){
	printf("相加結果為:%d",a+b);
}
```

## 函式遞迴
### 基礎概念
```C
void f(void);
int main(){
	f();
	return 0;
} 
void f(void){
	f();
}
```
```C
int f(int);

int main(){
	printf("%d\n",f(0));
	return 0;
}

int f(int i){
	return f(i+1);
}
```
### 基礎範例
```C
#include<stdio.h>
void countTo3(int);

int main(){
	countTo3(1);
	return 0;
}

void countTo3(int i){
	if (i<=3){
		printf("%d\n",i);
		countTo3(i+1);
	}
}
```
```C
#include<stdio.h>
void countTo1(int);

int main(){
	countTo1(1);
	return 0;
}

void countTo1(int i){
	if (i<=3){
		countTo1(i+1);
		printf("%d\n",i);
	}
}
```
```C

```

## 複合型態

## 巨集

## 檔案I/O

