![image](https://user-images.githubusercontent.com/93697962/140337750-2b260421-aeef-4abb-8154-5f243e13d59d.png)

# Ý tưởng:
- Bài này thì mình chỉ ghép cái đề bài zô xong chạy vòng lặp for với `i = 2` thoi :V đơn giản đúng khum :(( 

# Lưu đồ thuật toán:
![image](https://user-images.githubusercontent.com/93697962/140338497-984517a5-1b61-4066-8b01-975171bb06fe.png)

- Ở phần lưu đồ này thì thay vì ở đề bài là 2*(3^n) thì ở đầu mình gán `P = 2*3` xong trong vòng lặp tăng  `P` thêm 3 lần nữa thì sẽ giống với đề :V tương tự với `Q` thì mình cũng làm như vậy. Mình làm như vậy để vòng lặp bớt đi 2 phép nhân cho rút ngắn thời gian hay gì đó mình nghĩ là z :)))
 
# Code lại trên C++ nè:
```c++
#include <iostream>

int main()
{
	int n;
	std::cin >> n;
	int S = -2;
	int P = 3*2;
	int Q = 7*6;
	for( int i = 2; i <= n; i++)
	{
		P *= 3;
		Q *= 7;
		S = 5*S + P - Q + 12; 
	}	
	std::cout << S;

	return 0;
}

```
