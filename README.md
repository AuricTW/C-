# C語言學習筆記

## 資料型態與變數

### 基本架構

### 輸入輸出

## 運算


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
### switch條件判斷

### for迴圈

### while迴圈

### break、 continue、goto
