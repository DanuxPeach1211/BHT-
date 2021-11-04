![Screenshot 2021-11-04 202208](https://user-images.githubusercontent.com/93697962/140321030-e86cff45-5f8d-41c3-8f16-8bc6049ea61e.png)
# Ý tưởng:
- Bài này thì mình sẽ cho chạy vòng lặp, biến `i` ban đầu sẽ bằng 1 và sẽ tăng gấp 10 lần sau mỗi vòng để ta có thể xác định được từng số hạng của chữ số được nhập vào  `n`.

- Ta sẽ lấy `n` chia cho `i` lấy phần nguyên. Lúc này `i` bằng 1 thì `n` vẫn giữ nguyên. Sau đó ta chia lấy phần dư cho 10 thì ta được chữ số hàng đơn vị. Ta cộng chữ số hàng đơn vị vào biến `S` rồi tăng `i` lên 10 lần rồi chuyển qua vòng lặp tiếp.

- Lân này `n` chia cho `i` lấy phần nguyên lúc này bằng 10. Thì ta sẽ loại được chữ số hàng đơn vị và tiếp tục chia lấy phần dư cho 10 thì ta tìm được chữ số hàng chục. 

- Ta tiếp tục làm cho đến khi nào `i` lớn hơn `n` thì sẽ dừng vòng lặp.
## Ta có thể làm nhiều cách khác nhau nhưng mình chọn cách này :(( í kín gì hong -.-

# Từ suy nghĩ trên ta làm nên lưu đồ như sau:
![image](https://user-images.githubusercontent.com/93697962/140323105-7f3f7ca8-900f-4cfb-adea-7bfc924e2287.png)

# Ta làm code theo lưu đồ trên:
```c++
#include <iostream>

int main()
{
	int n;
	std::cin >> n;
	int S = 0;
	for( int i = 1; i <= n; i*=10)
	{
		S += ( n / i ) % 10 ;
	}
	
	std::cout << S;

	return 0;
}
```
