![image](https://user-images.githubusercontent.com/93697962/140341421-c22ab995-4efc-48a1-843c-a4d59f5e6b18.png)

# Ý tưởng:
- Ở bài này thì mình sẽ chạy vòng lặp `i=0` đến `n`. Vì số 0 vẫn là 1 số chính phương. Ở đây mình sẽ dùng một biến `S` là một biến đúng/sai.
- Mình sẽ dùng vòng lặp while với điều kiện `i*i <= n` mình dùng `i*i` thay cho `i` vì nếu dùng `i` không thôi thì sẽ có thể làm vòng lặp chạy khá lâu nếu `n` không phải là một số chính phương.
- Ở trong vòng lặp thì mình sẽ dùng `if` để kiểm tra xem `i*i == n` hay không. 
   - Nếu `if` sai thì ta tăng `i` lên 1 đơn vị và tiếp tục chạy vòng lặp.
   - Nếu `if` đúng thì ta gán `S = 1`.
- Sau khi thoát khỏi vòng lặp ta sẽ dùng `if` để so sánh biến `S` để xem `n` có phải là số chính phương hay không nha :((

# Lưu đồ thuật toán:
![image](https://user-images.githubusercontent.com/93697962/140363490-348c2f6a-af77-40fe-975c-2a6ec33f5fac.png)

# Code C++ nè đuối lắm rùi á:
```c++
#include <iostream>

int main()
{
	int n;
	std::cin >> n;
	int i = 0;
	int S = 0;
	while( i*i <= n )
	{
		if( i*i == n )
		{
			S = 1;
		}
		i++;
	}

	if(S == 1)
	{
		std::cout << "n la so CP";
	}
	else
	{
		std::cout << "n khong phai la so CP";
	}

	return 0;
}
```
