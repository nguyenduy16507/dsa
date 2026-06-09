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
    + Giá trị: vi Bạn muốn sắp xếp các đồ vật vào ba lô sao cho **tổng giá trị nhận được là lớn nhất có thể**. Nguồn tài liệu cũng ghi rõ "Giả sử mỗi loại đồ vật có đủ nhiều để xếp vào ba lô", điều này xác nhận đây là phiên bản không giới hạn số lượng đồ vật của bài toán Ba lô (unbounded knapsack problem). Mục tiêu là tìm các số nguyên không âm xi (số lượng đồ vật loại i được chọn) sao cho:
    
       Tổng khối lượng ∑ xi*si ≤ W
      
       Tổng giá trị ∑ xi*vi đạt giá trị lớn nhất    
