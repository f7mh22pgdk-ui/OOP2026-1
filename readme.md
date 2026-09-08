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
