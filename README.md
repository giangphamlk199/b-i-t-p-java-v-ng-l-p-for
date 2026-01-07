
//pham truong giang
// cntt_6



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

//bài 6: mảng
//truong giang
import java.util.Scanner;
import java.util.Arrays;

public class BaiTapMang1Chieu {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // a. Nhập mảng một chiều các số nguyên
        System.out.print("Nhập số phần tử n: ");
        int n = sc.nextInt();

        int[] a = new int[n];

        System.out.println("Nhập các phần tử của mảng:");
        for (int i = 0; i < n; i++) {
            System.out.print("a[" + i + "] = ");
            a[i] = sc.nextInt();
        }

        // b. Xuất mảng
        System.out.print("\nMảng vừa nhập: ");
        for (int i = 0; i < n; i++) {
            System.out.print(a[i] + " ");
        }

        // c. Tìm vị trí của số nguyên x
        System.out.print("\n\nNhập số x cần tìm: ");
        int x = sc.nextInt();
        boolean found = false;

        for (int i = 0; i < n; i++) {
            if (a[i] == x) {
                System.out.println("Số " + x + " xuất hiện tại vị trí: " + i);
                found = true;
            }
        }

        if (!found) {
            System.out.println("Không tìm thấy số " + x + " trong mảng.");
        }

        // d. Tìm giá trị lớn nhất
        int max = a[0];
        for (int i = 1; i < n; i++) {
            if (a[i] > max) {
                max = a[i];
            }
        }
        System.out.println("\nGiá trị lớn nhất trong mảng: " + max);

        // e. Tìm giá trị nhỏ nhất
        int min = a[0];
        for (int i = 1; i < n; i++) {
            if (a[i] < min) {
                min = a[i];
            }
        }
        System.out.println("Giá trị nhỏ nhất trong mảng: " + min);

        // f. Tìm vị trí phần tử có giá trị lớn nhất
        int viTriMax = 0;
        for (int i = 1; i < n; i++) {
            if (a[i] > a[viTriMax]) {
                viTriMax = i;
            }
        }
        System.out.println("Vị trí của phần tử lớn nhất: " + viTriMax);

        // g. Sắp xếp mảng tăng dần
        Arrays.sort(a);
        System.out.print("\nMảng sau khi sắp xếp tăng dần: ");
        for (int i = 0; i < n; i++) {
            System.out.print(a[i] + " ");
        }
    }
}
