// bài 1: tính tổng số nguyên từ 1 đến n bằng vòng lặp for
import java.util.Scanner;

public class SoNguyen {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n;
        System.out.print("Nhập n (n >= 1): ");
        n = sc.nextInt();

        for (int i = n; i >= 1; i--) {
            System.out.println(i);
        }
    }
}

//bài 2: in ra màn hình các số chẵn nhỏ hơn 11
public class SoChan {
    public static void main(String[] args) {
        for (int i = 0; i < 11; i++) {
            if (i % 2 == 0) {
                System.out.println(i);
            }
        }
    }
}

// bài 3: tính tổng số nguyên chẵn từ 0 đến n, vòng lặp for
import java.util.Scanner;

public class TongChan {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n;
        System.out.print("Nhập n (n >= 0): ");
        n = sc.nextInt();

        int sum = 0;

        for (int i = 0; i <= n; i += 2) {
            sum += i;
        }

        System.out.println("Tổng các số chẵn từ 0 đến " + n + " là: " + sum);
    }
}


// bài 4: in bảng cửu chương 1 đến 9 vòng lặp for lồng
public class CuuChuong {
    public static void main(String[] args) {
        for (int i = 1; i <= 9; i++) {          
            for (int j = 1; j <= 9; j++) {      
                System.out.printf("%d x %d = %2d   ", i, j, i * j);
            }
            System.out.println();              
        }
    }
}

// bài 5: viết chương trình cho yêu cầu sau input n=3, output 1     1 2     1 2 3
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();

        for (int i = 1; i <= n; i++) {          
            for (int j = 1; j <= i; j++) {      
                System.out.print(j + " ");
            }
            System.out.println();               
        }
    }
}



//bài 6: viết chương trình liệt kê từ 1 đến n

import java.util.Scanner;

public class LietKe {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Nhap n: ");
        int n = sc.nextInt();

        System.out.print("So cot moi hang: ");
        int cols = sc.nextInt();

        
        if (n < 1 || cols < 1) {
            System.out.println("n va so cot phai >= 1");
            return;
        }

        int count = 1;

      
        for (int i = 0; count <= n; i++) {
            for (int j = 0; j < cols && count <= n; j++) {
                System.out.printf("%3d", count);
                count++;
            }
            System.out.println(); 
        }

        sc.close();
    }
}

