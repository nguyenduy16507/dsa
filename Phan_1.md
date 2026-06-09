7) Trình bày Phương pháp chia để trị hàm mô tả ý tưởng phương pháp này, cho 
ví dụ minh hoạ.

- <img width="411" height="220" alt="image" src="https://github.com/user-attachments/assets/4021f593-e581-4a88-a149-825669e392b5" />
- <img width="404" height="250" alt="image" src="https://github.com/user-attachments/assets/e2bf0ea4-1067-41e4-9158-c2eca8ec5fe4" />
- <img width="409" height="199" alt="image" src="https://github.com/user-attachments/assets/5f3b261d-9862-43b6-aaa1-18a93dbf9a45" />
- <img width="434" height="245" alt="image" src="https://github.com/user-attachments/assets/d45f301c-b7e0-4075-a19c-df4f578f95ea" />

8) Trình bày Phương pháp qui hoạch động. Trình bày cách áp dụng Phương 
pháp quy hoạch để giải bài toán “Sắp xếp các đồ vật vào ba lô”, với số lượng các đồ 
vật không hạn chế.

* **Trình bày phương pháp:**
 - Khi tính nghiệm của bài toán lớn thông qua nghiệm của các bài toán con, ta chỉ việc sử dụng các kết quả đã được ghi lại
 - Điểm khác biệt của quy hoạch động là tiếp cận theo hướng Bottom-up(từ dưới lên trên), nghĩa là nó tính toán nghiệm của các bài toán con từ nhỏ đến lớn và ghi lại các kết quả đã tính được
 - Giải thuật được thiết kế bằng phương pháp quy hoạch động sẽ là giải thuật lặp
 - Điều đó giúp chúng ta tránh được phải tính toán nhiều lần nghiệm của cùng một bài toán con
 - khi cần nghiệm của bài toán lớn hơn, nó chỉ việc sử dụng các kết quả đã được lưu lại trong 1 bảng(thường là  mảng 1 chiều hoặc 2 chiều)
 - **Các bước chính để giải bài toán bằng quy hoạch động:**
   + Đưa ra cách tính nghiệm của các bài toán con đơn giản nhất
   + Tìm ra các công thức(hoặc quy tắc) để xây dựng nghiệm của bài toán lớn thông qua nghiệm của các bài toán con
   + Thiết kế bảng lưu trữ nghiệm của các bài toán con
   + Tính nghiệm của các bài toán con từ nhỏ đến lớn và lưu vào bảng
- Phương pháp quy hoạch động thường được áp dụng để giải quyết các bài toán tối ưu, nơi mục tiêu là tìm ra nghiệm có giá trị nhỏ nhất hoặc lớn nhất \

* Áp dụng Phương pháp quy hoạch động cho bài toán Sắp xếp các đồ vật vào Ba lô
  - **Đặt vấn đề bài toán**: Giả sử bạn có một chiếc ba lô có thể chứa được một khối lượng tối đa W. Bạn có n loại đồ vật, được đánh số từ 1 đến n. Mỗi loại đồ vật i có:

    + Khối lượng: si
    + Giá trị: vi Bạn muốn sắp xếp các đồ vật vào ba lô sao cho **tổng giá trị nhận được là lớn nhất có thể**. Nguồn tài liệu cũng ghi rõ "Giả sử mỗi loại đồ vật có đủ nhiều để xếp vào ba lô", điều này xác nhận   đây là phiên bản không giới hạn số lượng đồ vật của bài toán Ba lô (unbounded knapsack problem). Mục tiêu là tìm các số nguyên không âm xi (số lượng đồ vật loại i được chọn) sao cho:
    
       Tổng khối lượng ∑ xi*si ≤ W
      
       Tổng giá trị ∑ xi*vi đạt giá trị lớn nhất

Câu 9 : Trình bày phương pháp quay lui và mô tả ý tưởng

* Trình bày:Phương pháp quay lui (Backtracking) là một chiến thuật giải quyết vấn đề bằng cách thử từng bước các giải pháp tiềm năng. 

    1. **Thử từng bước:** Phương pháp này liên tục thực hiện các bước thử nghiệm để tìm ra lời giải.
    2. **Ghi nhớ thông tin:** Khi một lựa chọn được chấp nhận, các thông tin cần thiết sẽ được ghi nhớ.
    3. **Quay lui khi thất bại:** Nếu không tìm thấy một lựa chọn thích hợp nào, quá trình sẽ quay trở lại bước trước đó, xóa bỏ các ghi nhớ và thử các lựa chọn khác

 Hay:

     Giả sử cần tìm `(x1, x2, ..., xn)`:

       - Bắt đầu từ `x1`, chọn từng giá trị có thể trong `A1`, kiểm tra ràng buộc với `x1`.
       - Nếu hợp lệ, tiếp tục chọn `x2 ∈ A2`, kiểm tra ràng buộc với `x1`.
       - Tiếp tục như vậy cho đến `xn`.
       - Nếu tại bước nào đó không chọn được `xj` phù hợp → **quay lui** về `xj-1`, thử giá trị tiếp theo chưa thử.
       - Nếu quay lui đến `x1` mà không còn lựa chọn nào hợp lệ → **kết thúc** (không có lời giải, hoặc đã tìm đủ nghiệm).

* **Hàm mô tả ý tưởng**
```sh
  
   Backtrack(j) // Tìm thành phần thứ j của vector nghiệm
{
	for (mỗi xj thuoc Aj)
		if (xj thoả mãn các mối quan hệ ràng buộc với các thành phần đã chọn)
			{
				Lưu lại tình trạng khi chọn xj
				if (tìm được một nghiệm mới) //
						In nghiệm
				else
						Backtrack(j+1);
				Phục hồi lại tình trạng trước khi chọn xj //thể hiện sự quay lui
			}
		}
}

```

10) Trình bày Phương pháp nhánh cận hàm mô tả ý tưởng phương pháp này.
* <img width="1115" height="533" alt="image" src="https://github.com/user-attachments/assets/b7af3762-ce74-4595-851c-c9324498e0c3" />
* <img width="1217" height="683" alt="image" src="https://github.com/user-attachments/assets/bcb98bc0-8a86-4829-8eb8-9413e732edb1" />

* <img width="1016" height="670" alt="image" src="https://github.com/user-attachments/assets/fd291a17-5fab-4ed6-b63e-26911a004571" />



