# 버블 정렬

- O(N<sup>2</sup>) 시간 복잡도를 가지며 가장 효율이 낮은 정렬
- 선택정렬보다 안좋은 점은 모든 요소를 한번씩 확인해가가며 연산을 실행 하기 때문

---

```

int main(int argc, char* argv[]) {

    int i,j,temp;
    int index = 9;
    int arr[10] = {1, 10, 8, 7, 5, 6, 4, 3, 2, 9 };

    for(i = 0 ; i < 10; i++) {
        for(j = 0; j < 9-i; j++){
            if(arr[j] > arr[j+1]){
                temp = arr[j];
                arr[j] = arr[j+1];
                arr[j+1] = temp;
            }
        }

    }


    for(i = 0; i < 10; i++){
        printf("%d ", arr[i]);
    }

    return 0;
}

```

---

### 출력결과

### 1 2 3 4 5 6 7 8 9 10
