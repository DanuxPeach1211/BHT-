![image](https://user-images.githubusercontent.com/93697962/140324657-3942b8db-b749-42a6-9a6c-6cbebc668624.png)

# Ý tưởng:
- Ở bài này ta nhìn đề thấy được rằng bài sẽ theo quy tắc là phần tử với cơ số là `x` sẽ có số mũ tăng dần. Còn phần mẫu thì sẽ là tổng các số mũ của `x` qua từng lần tăng thêm.

- Nên ta sẽ chạy vòng lặp thui.
## Bài này nghĩ vậy thui chứ khum có khó nên hong bít nói sao ::(

# Từ ý tưởng siêu dễ hiểu trên ta viết lưu đồ thuật toán sau:
![image](https://user-images.githubusercontent.com/93697962/140326672-86c67b24-1525-4721-bc74-70625eca02c2.png)

# Code C++ từ lưu đồ trên thoi:
```c++
#include <iostream>

int main()
{
	int x, n;
	std::cin >> x >> n;
	float S = 0;
	int P = 0;
	int X = x;
	for( int i = 1; i <= n; i++)
	{
		P += i;
		S += (1.0*X)/P;
		X *= x;
	}
	
	std::cout << S;

	return 0;
}
```
