![image](https://user-images.githubusercontent.com/93697962/140374109-d0d1ac53-0b2e-4c53-ae26-f72e8750eb06.png)

# Ý tưởng:
- Ở bài này thì mình sẽ chạy vòng lặp `while` với điều kiện `n % 5 == 0`. Vì nếu điều kiện trên đúng thì có khả năng `n` có dạng 5^m vì những số này sẽ chia hết cho 5.
  - Nếu điều kiện đúng thì ta sẽ chia `n` cho 5 lấy phần nguyên để giảm dần `n` về với giá trị 5^m thấp nhất là 5^0 = 1. Rồi ta quay lại với điều kiện của vòng lặp
  - Nếu điều kiện sai thì ta thoát khỏi vòng lặp.
- Sau khi thoát khỏi vòng lặp thì ta so sánh `n == 1`.
  - Nếu điều kiện đúng thì sẽ xuất ra màn hình `n la so CP`.
  - Nếu điều kiện sai thì sẽ xuất ra màn hình `n khong phai la so CP`.

# Sau đây là lưu đồ thuật toán:
![image](https://user-images.githubusercontent.com/93697962/140375187-2b334695-57d0-4ab8-8f3d-2d8f312918c2.png)

# Mình code C++ ra từ lưu đồ nè:
```c++
#include <iostream>

int main(){
   int n;
   std::cin >> n;
   while ( n % 5 == 0 )
   {
       n = n / 5;
   }
   
   if ( n == 1 )
   {
       std::cout << "n co dang 5^m";
   }
   else
   { 
       std::cout<<"n khong co dang 5^m";
   }

   return 0;
}
```
