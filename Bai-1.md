![image](https://user-images.githubusercontent.com/93697962/140301149-d8dbd1a6-f2b1-4827-adc3-bbeecd082bc4.png)
# Ý tưởng:
- Bài này thì mình phải tăng số mũ của x lên 11. Mà tích của hai lũy thừa cùng cơ số là cộng số mũ của cơ số đó.
- Nên mình tách x^11 = x^6 . x^5 = (x^3.x^3) . (^3.x^2). Từ đây ta phải đưa x lên số mũ 2, 3, 5, 6 là sẽ lên được x^11 với 5 phép nhân.
- Ta nhân `x.x` thì sẽ được `x^2` rồi từ `x^2 . x`ta được `x^3`. Để lên `x^5` thì ta lấy `x^2 . x^3` là được. Tương tự thì `x^6` sẽ bằng  
`x^3 . x^3`.
- Giờ ta chỉ cần lấy `x^5 . x^6` là được `x^11` rồi.
### Ta có thể làm theo nhiều cách khác nhau. Nhưng ở phép toán này thì 5 phép nhân là ít nhất nha!
# Từ đó ta soạn ra lưu đồ thuận toán như sau:
![image](https://user-images.githubusercontent.com/93697962/140318829-6ee65918-55b7-4171-86fc-e8fa44154d10.png)

# Từ lưu đồ thuật toán ta chuyển qua code C++:
```c++
#include <iostream>

int main()
{
	int x;
	std::cin >> x;
	int x2 = x * x;
	int x3 = x2 * x; 
	int x5 = x3 * x2;
	int x6 = x3 * x3;
	int x11 = x5 * x6;

	std::cout << x11;

	return 0;
}
  ```
