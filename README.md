# OOP2026
### Homework1
```java
class triangle {
    public static void main(String[] args) {
        for (int i=0; i<10; i++){
            for(int j=0; j<=i; j++){
                System.out.print("#");
            }
            for(int j=i+1; j<10;j++){
                System.out.print(" ");
            }
            System.out.println();
        }
        System.out.println();

        for (int i=0; i<10; i++){
            for(int j=i; j<10; j++){
                System.out.print("#");
            }
            for(int j=0; j<=i-1; j++){
                System.out.print(" ");
            }
            System.out.println();
        }
        System.out.println();

        for (int i=0; i<10; i++){
            for(int j=i+1; j<10; j++){
                System.out.print(" ");
            }
            for(int j=0; j<=i; j++){
                System.out.print("#");
            }
            System.out.println();
        }
        System.out.println();

        for (int i=0; i<10; i++){
            for(int j=0; j<i; j++){
                System.out.print(" ");
            }
            for(int j=i; j<10; j++){
                System.out.print("#");
            }
            System.out.println();
        }    
    }
}

```

![Alt homework11](./images/homework1.png)

### Homework2
```java
public class Main {
    public static void main(String[] args) {
        int a = 1;
        int b = 1;

        for (int i = 1; i <= 20; i++) {
            System.out.print(a + " ");

            int next = a + b;
            a = b;
            b = next;
        }
    }
}

```
![Alt homework11](./images/homework2.png)

### Homework3
```java
public class Main {
    public static void main(String[] args) {

        int a = 1;
        int b = 1;

        for (int i = 1; i <= 20; i++) {

            int next = a + b;
            a = b;
            b = next;

            System.out.println(b + "/" + a + " = " + (double)b / a);
        }
    }
}

```
![Alt homework11](./images/homework3.png)

### Homework4
```java
public class Main {
    public static void main(String[] args) {

        for (int i = 1; i <= 9; i++) {
            for (int j = 1; j <= 9; j++) {
                System.out.print(j + "*" + i + "=" + (j * i) + " ");
            }
            System.out.println();
        }
    }
}

```
![Alt homework11](./images/homework4.png)

### Homework5
```java
public class Main {
    public static void main(String[] args) {

        // Gregory-Leibniz
        double pi1 = 0.0;

        for (int i = 0; i < 1000000; i++) {
            if (i % 2 == 0) {
                pi1 += 4.0 / (2 * i + 1);
            } else {
                pi1 -= 4.0 / (2 * i + 1);
            }
        }

        System.out.println("Gregory-Leibniz = " + pi1);


        // Madhava
        double pi2 = 0.0;

        for (int i = 0; i < 20; i++) {
            double term = 1.0 / ((2 * i + 1) * Math.pow(3, i));

            if (i % 2 == 0) {
                pi2 += term;
            } else {
                pi2 -= term;
            }
        }

        pi2 = Math.sqrt(12) * pi2;

```
![Alt homework11](./images/homework5.png)

### Homework6
```java
        System.out.println("Madhava = " + pi2);
    }
}public class Main {
    public static void main(String[] args) {

        int binomial[][] = new int[10][10];

        for (int i = 0; i < 10; i++) {

            binomial[i][0] = 1;
            binomial[i][i] = 1;

            for (int j = 1; j < i; j++) {
                binomial[i][j] =
                    binomial[i - 1][j - 1] + binomial[i - 1][j];
            }
        }

        for (int i = 0; i < 10; i++) {
            for (int j = 0; j <= i; j++) {
                System.out.print(binomial[i][j] + " ");
            }
            System.out.println();
        }
    }
}

```
![Alt homework11](./images/homework6.png)

### Homework7
```java
public class Main {
    public static void main(String[] args) {

        int data[] = new int[20];

        // 0~99 랜덤 숫자 생성
        for (int i = 0; i < 20; i++) {
            data[i] = (int)(Math.random() * 100);
        }

        // 정렬 전
        System.out.println("정렬 전");

        for (int i = 0; i < 20; i++) {
            System.out.print(data[i] + " ");
        }

        System.out.println();


        // Selection Sort
        for (int i = 0; i < 19; i++) {

            int min = i;

            for (int j = i + 1; j < 20; j++) {
                if (data[j] < data[min]) {
                    min = j;
                }
            }

            int temp = data[i];
            data[i] = data[min];
            data[min] = temp;
        }


        // 정렬 후
        System.out.println("정렬 후");

        for (int i = 0; i < 20; i++) {
            System.out.print(data[i] + " ");
        }
    }
}

```
![Alt homework11](./images/homework7.png)

### Homework8
```java
public class Main {
    public static void main(String[] args) {

        int score[][] = new int[30][5];

        // 점수 생성
        for (int i = 0; i < 30; i++) {

            for (int j = 0; j < 4; j++) {
                score[i][j] = (int)(Math.random() * 101);
            }

            // 합계
            score[i][4] =
                score[i][0] +
                score[i][1] +
                score[i][2] +
                score[i][3];
        }


        // 출력
        System.out.println("번호\t국어\t영어\t수학\t과학\t합계");

        for (int i = 0; i < 30; i++) {

            System.out.print((i + 1) + "\t");

            for (int j = 0; j < 5; j++) {
                System.out.print(score[i][j] + "\t");
            }

            System.out.println();
        }
    }
}

```
![Alt homework11](./images/homework8.png)

### Homework9
(1.75)₁₀   = (1.11)₂
(1.625)₁₀  = (1.101)₂
(1.5625)₁₀ = (1.1001)₂
(1.875)₁₀  = (1.111)₂
(13.875)₁₀ = (1101.111)₂
(45.875)₁₀ = (101101.111)₂

### Homework10
```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        
        int array_count = sc.nextInt();
        int max_value = sc.nextInt();
        int bin_size = sc.nextInt();
        int display_scale = sc.nextInt();
        
        int hist_size = max_value / bin_size;
        
        int[] arr = new int[array_count];
        int[] hist = new int[hist_size];
        
        for (int i = 0; i < array_count; i++) {
            arr[i] = (int) (Math.random() * max_value);
        }
        
        for (int i = 0; i < array_count; i++) {
            hist[arr[i] / bin_size]++;
        }
        
        for (int i = 0; i < hist_size; i++) {
            int start = i * bin_size;
            int end = (i + 1) * bin_size - 1;
            
            System.out.printf("%2d~%2d\t", start, end);
            
            int count = hist[i] / display_scale;
            for (int j = 0; j < count; j++) {
                System.out.print("#");
            }
            System.out.println();
        }
        
        sc.close();
    }
}

```
![Alt homework11](./images/homework10.png)

### Homework11
```java
import java.util.Arrays;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        
        System.out.print("데이터 개수 입력: ");
        int array_count = sc.nextInt();
        
        int[] arr = new int[array_count];
        
   
        for (int i = 0; i < array_count; i++) {
            arr[i] = (int) (Math.random() * 100) + 1;
        }
        
    
        System.out.print("생성된 데이터: ");
        for (int i = 0; i < array_count; i++) {
            System.out.print(arr[i] + " ");
        }
        System.out.println("\n");
        
    
        double sum = 0;
        for (int i = 0; i < array_count; i++) {
            sum += arr[i];
        }
        double arithmeticMean = sum / array_count;
        
    
        double prod = 1.0;
        for (int i = 0; i < array_count; i++) {
            prod *= arr[i];
        }
        double geometricMean = Math.pow(prod, 1.0 / array_count);
        
      
        double harmonicSum = 0;
        for (int i = 0; i < array_count; i++) {
            harmonicSum += 1.0 / arr[i];
        }
        double harmonicMean = array_count / harmonicSum;
        
      
        int[] sortedArr = arr.clone();
        Arrays.sort(sortedArr);
        double median;
        if (array_count % 2 == 1) {
            median = sortedArr[array_count / 2];
        } else {
            median = (sortedArr[array_count / 2 - 1] + sortedArr[array_count / 2]) / 2.0;
        }
        
      
        System.out.println("=== [통계 계산 결과] ===");
        System.out.printf("산술평균 (Arithmetic Mean) : %.4f\n", arithmeticMean);
        System.out.printf("기하평균 (Geometric Mean)  : %.4f\n", geometricMean);
        System.out.printf("조화평균 (Harmonic Mean)   : %.4f\n", harmonicMean);
        System.out.printf("중앙값 (Median)            : %.4f\n", median);
        
        sc.close();
    }
}

```
![Alt homework11](./images/homework11.png)

