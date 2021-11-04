![image](https://user-images.githubusercontent.com/93697962/140327772-270fecae-6504-4b7f-b218-234906439300.png)

# Ý tưởng:
- Bài này ta nhìn thấy giống cấp số nhân với phần tử đầu tiên là `-x^2` và sẽ tăng lên `-x^2` qua từng phần tử. 
- Nên ta sẽ sử dụng vòng lặp ở bài này nha. Nhìn lưu đồ thuật toán ik tại bài này dễ lắm :(( 

# Lưu đồ thuật toán:
![image](https://user-images.githubusercontent.com/93697962/140329197-cf2014d0-671f-4665-80d0-e7fde1ad06a8.png)

# Từ lưu đồ trên ta code C++ như sau:
```c++
#include <iostream>

int main()
{
	int x, n;
	std::cin >> x >> n;
	int S = 0;
	int D = 1;
	int X = - x*x;
	for( int i = 1; i <= n; i++)
	{
		D *= X;
		S += D;
	}	
	std::cout << S;

	return 0;
}
```
