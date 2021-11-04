![image](https://user-images.githubusercontent.com/93697962/140334668-19da2128-e8e1-4492-83eb-15e4f893a3e0.png)

# Ý tuởng:
- Thật ra lúc đầu làm bài này mình cũng không hiểu đề cho lắm nên ko biết ý tưởng như nào đâu :((
- Nhưng sau một hồi tham khảo qua kênh ytb của thầy và bài của các bạn. Mình đã hiểu được vấn đề.
- Bài này thì ta cần đặt một biến `e = 1` tượng trưng cho sai số rồi chạy vòng lặp `e >= 10^(-6)` để khi nào `e < 10^(-6)` là thỏa mãn yêu cầu của đề bài thì ta kết thúc vòng lặp.
- Trong vòng lặp ta thêm biến `i = 1` tăng dần qua mỗi vòng lặp để tìm ra đáp án của đề nha :(( ta gán `e = 1/i` để cho e giảm dần khi nào bé hơn 10^(-6) để kết thúc vòng lặp. Và ta cộng vào `S` để xuất ra màn hình đáp án.
## Bài này mình cũng lú lắm nên là không giải đáp rõ cho các bạn được :(( 

# Ta có lưu đồ thuật toán như sau: 
![image](https://user-images.githubusercontent.com/93697962/140336021-64dc7fe1-9817-4ac4-a9f3-70d55cef49a1.png)

- Mình lỡ bấm  `e` thành `E` rồi nhìn tạm đi khum sao đâu :((

# Code C++ thoi :V
- Lưu ý là bài này mình nên dùng vòng lặp do-while hoặc while-do sẽ dễ hơn for :V thực ra mình nhìn for nghĩ là khó nên dùng while chứ ko bít code for có được không nữa.
```c++
#include <iostream>
#include <cmath>

int main()
{
	float E = 1;
	float S = 0;
	int i = 1;
	do
	{
		E = 1.0/i ;
		S += E;
		i++;
	}while( E >= 10^(-6) );
	std::cout << S;

	return 0;
}

```

