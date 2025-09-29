# Bộ truyền động Cycloid (Cycloidal Drive)
## I. Giới thiệu: Khắc phục điểm yếu Mô-men xoắn (Torque)
### 1. Vấn đề của Servo Tiêu chuẩn:

Các động cơ Servo tiêu chuẩn (như 360° hoặc 180°) được chọn vì tốc độ và sự tiện lợi, nhưng chúng có mô-men xoắn đầu ra rất thấp so với tải trọng thực tế trong thi đấu (ví dụ: nâng, giữ vật nặng, hoặc chống lại va đập).

### 2. Giải pháp Cycloid:

Cycloidal Drive là một cơ cấu giảm tốc hiệu suất cao, cho phép chúng ta đánh đổi tốc độ quay của động cơ để nhận lại mô-men xoắn cực lớn với cùng một công suất đầu vào.

Mục tiêu: Biến một Servo yếu, tốc độ cao thành một bộ truyền động mạnh mẽ, chậm hơn, chịu tải tốt hơn.

## II. Cơ chế Hoạt động: Đĩa Cycloid và Nguyên lý Lệch tâm
Bộ truyền động Cycloid không dùng bánh răng thông thường mà dùng một cơ chế lệch tâm phức tạp hơn, mang lại tỷ số giảm tốc cao chỉ trong một tầng.

| Thành phần | Vai trò | Chú thích |
| ---------- |--------- |---------- |
| Trục Lệch Tâm (Eccentric Shaft) | Nối trực tiếp với động cơ (đầu vào tốc độ cao). | Trục này không quay theo tâm mà quay theo một quỹ đạo lệch. |
| Đĩa Cycloid (Cycloid Disc) | Bộ phận chính tạo ra sự giảm tốc. | Có biên dạng đặc biệt, quay lệch tâm bên trong vỏ. |
| Các Chốt/Pin (Outer Pins) | Các chốt/pin cố định (hoặc lăn) được sắp xếp xung quanh vỏ. | Các chốt này ăn khớp với các lỗ/biên dạng của đĩa Cycloid. |

Xuất sang Trang tính
Nguyên lý Giảm tốc:

Trục Lệch Tâm quay một vòng.

Đĩa Cycloid bị ép phải lắc lư, di chuyển trong các chốt/pin cố định.

Mỗi lần lắc lư, đĩa Cycloid chỉ tiến lên một khoảng bằng một răng so với các chốt.

Tỷ số truyền ~ số lượng chốt - 1. Ví dụ: Nếu có 21 chốt, tỷ số là 20:1.

Đầu ra (Output) được gắn với đĩa Cycloid, vì thế, 20 vòng quay của động cơ mới tạo ra 1 vòng quay của đầu ra.

## III. Lợi ích Thực chiến
Kinh nghiệm: Khi robot cần nâng một vật nặng hoặc giữ vững một cơ cấu sau khi di chuyển, mô-men xoắn cần phải cực lớn và ổn định.
### 1. Mô-men xoắn Tăng theo cấp số nhân:
Cycloid giúp đạt được mô-men xoắn cần thiết mà không cần dùng đến động cơ DC mạnh mẽ và đảm bảo thiết kế robot nằm trong khuôn khổ của luật thi đấu.

### 2. Độ cứng vững và Phản ứng ngược thấp (Low Backlash):
Cycloid có nhiều điểm tiếp xúc hơn, giúp giảm độ rơ gần như bằng 0. Điều này đảm bảo độ chính xác vị trí cao và khả năng giữ vững tải tuyệt vời.

### 3. Khả năng Chịu tải sốc (Shock Load Resistance):
Tải trọng được phân tán đều qua nhiều chốt, khiến bộ truyền Cycloid cực kỳ bền bỉ và ít bị hỏng hóc cơ khí hơn, đảm bảo robot hoạt động liên tục trong các trận đấu.
