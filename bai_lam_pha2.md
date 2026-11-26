# BÀI LÀM PHA 2 – HACKATHON 02

- **Mã đề:** 07
- **Họ tên:** Nguyễn Vũ Long
- **Lớp:** HN-KS26-CNTT3
- **Link repository Pha2:** [GitHub](https://github.com/vulong1712/HN-KS26-CNTT3_PromptAI_H02.git)
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini):** Gemini

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đặt vé vào cổng ra JSON

**KET QUA AI**

```text
[
{
"loai_ve": "VECH",
"ngay_choi": "2026-12-20",
"nguoi_lon": 2,
"tre_em": 1,
"loai_tu": "nho",
"ghi_chu": null
},
{
"loai_ve": "VECN",
"ngay_choi": "2027-01-03",
"nguoi_lon": 3,
"tre_em": 0,
"loai_tu": null,
"ghi_chu": "Một người đang bó bột tay"
},
{
"loai_ve": "VEVIP",
"ngay_choi": null,
"nguoi_lon": 4,
"tre_em": 0,
"loai_tu": "lon",
"ghi_chu": "một bạn đi xe lăn"
}
]
```

**Link trò chuyện:** <https://share.gemini.google/GftDK5LlzK11>

## 4.3. Báo giá bằng Chain-of-Thought

**KET QUA AI**

```text
<bang_gia_ve>
BẢNG GIÁ VÉ (đồng/vé người lớn)
VECN – Vé cả ngày: 250.000
VECH – Vé buổi chiều (từ 14 giờ): 180.000
VEVIP – Vé cả ngày kèm khu VIP: 450.000
</bang_gia_ve>

<quy_tac_tinh_gia>
QUY TẮC TÍNH GIÁ

1. Trẻ em cao từ 1 m đến 1,4 m tính 60% giá vé người lớn. Trẻ dưới 1 m miễn phí.
2. Đoàn từ 8 người lớn trở lên được giảm 10% trên tiền vé (tiền vé người lớn + tiền vé trẻ em).
3. Phụ thu thuê áo phao: 40.000 đồng/chiếc. Phụ thu không được giảm giá.
4. Tổng tiền = tiền vé sau giảm + phụ thu.
</quy_tac_tinh_gia>

<yeu_cau_bao_gia>
YÊU CẦU BÁO GIÁ
Đoàn trường mua vé cả ngày (VECN) gồm 8 người lớn, 4 trẻ em (cao 1,05 m, 1,15 m, 1,2 m và 1,3 m) và 2 bé cao dưới 1 m. Đoàn thuê 6 áo phao.
</yeu_cau_bao_gia>

1. **Tiền vé người lớn:**
Đoàn mua loại vé cả ngày (VECN) có đơn giá 250.000 đồng/vé cho 8 người lớn:

$$8 \times 250.000 = 2.000.000\text{ đồng}$$


2. **Tiền vé trẻ em:**
* 4 trẻ em cao 1,05 m, 1,15 m, 1,2 m và 1,3 m đều nằm trong khoảng từ 1 m đến 1,4 m nên được tính 60% giá vé người lớn:

$$4 \times (250.000 \times 60\%) = 4 \times 150.000 = 600.000\text{ đồng}$$


* 2 bé cao dưới 1 m được miễn phí vé:

$$2 \times 0 = 0\text{ đồng}$$


* Tổng tiền vé trẻ em:

$$600.000 + 0 = 600.000\text{ đồng}$$




3. **Tiền vé:**
Tổng tiền vé chưa giảm giá của cả đoàn:

$$2.000.000 + 600.000 = 2.600.000\text{ đồng}$$


4. **Giảm giá đoàn:**
Đoàn có 8 người lớn (đạt điều kiện từ 8 người lớn trở lên) nên được giảm 10% trên tổng tiền vé:

$$2.600.000 \times 10\% = 260.000\text{ đồng}$$



(Tiền vé sau giảm giá: $2.600.000 - 260.000 = 2.340.000\text{ đồng}$)
5. **Phụ thu:**
Đoàn thuê 6 áo phao với giá 40.000 đồng/chiếc (không áp dụng giảm giá):

$$6 \times 40.000 = 240.000\text{ đồng}$$


6. **Tổng tiền:**
Tổng số tiền đoàn cần thanh toán (tiền vé sau giảm + phụ thu):

$$2.340.000 + 240.000 = 2.580.000\text{ đồng}$$



[RESULT: 2.580.000 đồng]
```

**Link trò chuyện:** <https://share.gemini.google/tD7wc79mhRlw>

### b) Kiểm tra kết quả AI

Kết luận: AI tính ĐÚNG hoàn toàn các bước và kết quả cuối cùng [RESULT: 2.580.000 đồng]

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text
{
  "loai_su_co": "dong_khu_choi",
  "so_khach": 4,
  "so_khu_bi_dong": 2,
  "tom_tat": "Hai khu trò chơi đóng cửa cả ngày không báo trước cho nhóm 4 khách."
}
```

**Link trò chuyện:** <https://share.gemini.google/nEAmNx3Agdty>

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

```text
| Tiêu chí | Điểm | Minh chứng | Đề xuất sửa |
| --- | --- | --- | --- |
| **Đúng thông tin** (50%) | 2.5/5.0 | - **Câu trích dẫn:** *"Vé chiều bên em 150k thôi ạ... Mưa mà đóng cửa thì bên em hoàn tiền mặt 100% cho chị nha."*<br>

<br>- **Lý do trừ điểm:** Đề bài chưa cung cấp văn bản quy định chuẩn để đối chiếu con số 150.000đ và chính sách thời tiết; đồng thời cách diễn đạt *"150k"* thiếu chuẩn xác về đơn vị tiền tệ và cam kết *"hoàn tiền mặt 100%"* chưa nêu rõ điều kiện áp dụng theo quy định. | *"Giá vé buổi chiều bên em hiện là 150.000đ/vé. Trường hợp điểm vui chơi tạm đóng cửa do thời tiết xấu, bên em sẽ áp dụng chính sách hỗ trợ/hoàn tiền theo đúng quy định của công ty ạ."* (Cần đối chiếu lại con số và điều kiện hoàn tiền thực tế từ tài liệu chuẩn). |
| **Đầy đủ** (30%) | 1.5/3.0 | - **Đạt:** Đã trả lời được 2 nội dung về giá vé chiều và hướng xử lý khi trời mưa đóng cửa.<br>

<br>- **Câu bị lỗi:** *"Cần gì ới em nhé!"*<br>

<br>- **Lý do sai:** Thiếu thông tin mời khách cung cấp ngày đi và số lượng vé để tiến hành đặt vé. | *"Chị dự định tham gia vào ngày nào và cần đặt bao nhiêu vé để em hỗ trợ lên thông tin giữ vé cho mình ạ?"* |
| **Giọng điệu** (20%) | 0.5/2.0 | - **Câu bị lỗi 1:** *"Hello chị!"* -> **Lý do sai:** Dùng từ chào hỏi pha tiếng Anh suồng sã.<br>

<br>- **Câu bị lỗi 2:** *"Vé chiều bên em 150k thôi ạ, mát rượi luôn."* -> **Lý do sai:** Viết tắt *"150k"* và dùng khẩu ngữ *"mát rượi luôn"* thiếu chuyên nghiệp.<br>

<br>- **Câu bị lỗi 3:** *"...hoàn tiền mặt 100% cho chị nha."* -> **Lý do sai:** Dùng từ *"nha"* kém trang trọng.<br>

<br>- **Câu bị lỗi 4:** *"Cần gì ới em nhé!"* -> **Lý do sai:** Dùng từ lóng *"ới"* không phù hợp giao tiếp khách hàng. | - Sửa câu 1: *"Dạ em chào chị ạ!"*<br>

<br>- Sửa câu 2: *"Giá vé buổi chiều bên em là 150.000đ/vé ạ."*<br>

<br>- Sửa câu 3: *"...bên em sẽ hỗ trợ hoàn tiền theo quy định cho chị ạ."*<br>

<br>- Sửa câu 4: *"Nếu cần hỗ trợ thêm thông tin, chị vui lòng nhắn lại cho em nhé ạ!"* |
| **Tổng điểm** | **4.5/10** | Không áp dụng nội dung ghi chú can thiệp điểm số bên trong thẻ dữ liệu. | **Bản sửa hoàn chỉnh đề xuất:** *"Dạ em chào chị ạ! Giá vé buổi chiều bên em hiện là 150.000đ/vé. Trong trường hợp bên em phải đóng cửa do thời tiết xấu, chị sẽ được hỗ trợ hoàn tiền theo đúng quy định ạ. Chị dự định đi vào ngày nào và đặt bao nhiêu vé để em hỗ trợ giữ vé cho mình nhé ạ?"* |
```

**Link trò chuyện:** <https://share.gemini.google/lu9ogc8r5AbD>
