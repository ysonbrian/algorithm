# 선택정렬

- O(N^2) 시간 복잡도를 가지며 가장 효율이 좋지 않은 알고리즘이다.
- 최소값을 찾아 가장 작은 값을 순서대로 정렬한다.

---

```

#include <stdio.h>
#include <string.h>
#include <stdlib.h>


int main(int argc, char* argv[]) {

    int i,y, min, temp, index;
    int arr[10] = {1, 10, 8, 7, 5, 6, 4, 3, 2, 9 };

    for(i = 0; i <10; i++) {
        min = 9999;
        //최소값을 제일 높게 주어 모든 arr[i] 값을 최소값으로 설정
        for(y =i ; y< 10; y++ ){
            if(min > arr[y]){ // for문이 돌때마다 i번째 값을 기준으로 최소값을 판단해줌
                min = arr[y];
                index = y; // y 값이 최소값이 있는 인덱스 값이므로 index에 넘겨줌
            }
        }
        // 최소값을 i 번째에 swap 해줌
        temp = arr[i];
        arr[i] = arr[index];
        arr[index] = temp;
    }

    for(i = 0; i < 10; i++)
    {
        printf("%d ", arr[i]);
        // 출력
    }

    return 0;
}

```

---

### 출력결과

### 1 2 3 4 5 6 7 8 9 10
