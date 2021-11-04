![image](https://user-images.githubusercontent.com/93697962/140330295-6ed4f248-86b9-475a-9d6f-6fbb6986a4ad.png)

# Ý tưởng:
- Bài này mình nhìn ngược thấy là `x` sẽ tăng số mũ lên 1 bậc. Và mỗi lần tăng thì sẽ thêm một dấu căn nữa.
- Cho `S = 0` , `X = x`. Ta sẽ chạy vòng lặp ở bài này cho `i` chạy từ 1 đến `n`. Mỗi vòng lặp thì ta sẽ thực hiện công thức sau đây  
`S = S + sqrt(S + X)` và tăng số mũ của `x` lên 1 bậc bằng cách `X = X * x`.
- Ở vòng lặp thứ nhất ta được `S = sqrt(x)`. Tiếp vòng lặp 2 ta sẽ được `S = sqrt(x^2 + sqrt(x))` vì khi vòng lặp 1 kết thúc thì ta đã tự gán giá trị cho `S` luôn rồi.
- Ta tiếp tục chạy vòng lặp cho đến khi thỏa điều kiện thì thoi là xong :(( 
## Hãy hiểu bài đi làm ơn :(((((

# Lưu đồ thuật toán:
![image](https://user-images.githubusercontent.com/93697962/140332946-f58ab6c2-5556-420f-8595-22a113959a0f.png)

# Code C++ từ lưu đồ thuật toán nào:
```c++
#include <iostream>
#include <cmath>

int main()
{
	int x, n;
	std::cin >> x >> n;
	float S = 0;
	int X = x;
	for( int i = 1; i <= n; i++)
	{
		S = sqrt(S + X);
		X = X*x;
	}	
	std::cout << S;

	return 0;
}
```
