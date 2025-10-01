# ATM Mini Project
ATM Mini Project - Software Engineering Lab
📌 Giới thiệu
Dự án này sẽ được phát triển tại môn Nhập khẩu Công nghệ Phần mềm Phần mềm .
Mục tiêu là ứng dụng quy trình phát triển phần mềm, từ phân tích yêu cầu, thiết kế, trình lập, kiểm tra và phát triển khai báo .

👥 Thành viên nhóm
- Nguyễn Lâm Bảo Khuyên – Leader
- Nguyễn Thị Kim Tuyền – Member
- Ngô Hải Triều - Member
🎯 Use Case chính
Quản lý người dùng
Quản lý sản phẩm/dịch vụ
Process transaction
Báo cáo & thống kê
(Trường hợp sử dụng sơ đồ có thể chèn hình ảnh vào đây)

📐 Hệ thống thiết kế
Biểu đồ trường hợp sử dụng :Trường hợp sử dụng
Biểu đồ trình tự :Sự liên tiếp
ERD (Sơ đồ thực thể quan hệ) :ERD
💻 Công nghệ sử dụng
Ngôn ngữ: Java / Python / JavaScript / PHP
IDE: Visual Studio Code
CSDL: MySQL / PostgreSQL
Quản lý phiên bản: Git + GitHub
Mô hình phát triển: Agile – Scrum
🚀 Cài đặt và thử nghiệm
Bản sao kho lưu trữ:
git clone https://github.com/vancv43/[ten-repo].git
cd [ten-repo]

Phòng thí nghiệm Kỹ thuật phần mềm | Bài giảng – 01-05

Lab 01 – Thiết lập môi trường & Quản lý dự án trên GitHub • Mục tiêu: Sinh viên làm quen với GitHub, Git và công cụ cài đặt. • Nội dung: o Tạo tài khoản GitHub, tạo kho lưu trữ dành riêng cho môn học. o Cấu hình Git (sao chép, cam kết, đẩy, kéo). o Cập nhật hồ sơ cá nhân trên README.md. o Upload bài tập đơn giản: file text giới thiệu bản thân.

Lab 02 – Phân tích yêu cầu & Ca sử dụng thiết kế • Mục tiêu: Sinh viên học cách mô tả hệ thống yêu cầu bằng UML. • Nội dung: o Chọn Mini Project (ví dụ: hệ thống quản lý đặt phòng khách sạn, hệ thống bán hàng trực tuyến). o Draw Use Case Diagram mô tả các chức năng chính và các tác nhân. o Viết Use Case Description cho ít nhất 2 chức năng quan trọng. o Tải bản vẽ (dạng ảnh hoặc file .drawio) lên GitHub.

Lab 03 – UML Design (Use case-UC, Sequence Diagram-SQ) • Mục tiêu: Sinh viên mô tả luồng tương tác chi tiết của hệ thống. • Nội dung: o Dựa trên ATM Mini Project, vẽ UC, SQ cho một quy trình nghiệp vụ. o Giải thích các tham số tham gia và trao đổi thông điệp. o Tải sơ đồ lên cùng một tệp mô tả GitHub.

Lab 04 – Coding giao diện đăng nhập (Form login) • Mục tiêu: Sinh viên áp dụng kỹ năng lập trình cơ bản front-end. • Nội dung: o Dùng Visual Studio Code viết form đăng nhập bằng HTML, CSS, JavaScript. o Yêu cầu: có tên đăng nhập/mật khẩu, nút Đăng nhập, Hủy, Ghi nhớ tôi. o Thực hiện kiểm tra cơ sở dữ liệu bằng JavaScript. o Đưa mã nguồn lên GitHub và chạy bản demo.

Lab 05 – Tích hợp, quản lý & báo cáo • Mục tiêu: Hoàn thiện quy trình phần mềm từ thiết kế đến phát triển khai. • Nội dung: o Xem tất cả các tạo phẩm (Ca sử dụng, Trình tự, Mã đăng nhập biểu mẫu). o Tạo Báo cáo Dự án (Markdown hoặc PDF) mô tả công việc quy trình. o Hướng dẫn push code, cập nhật readme, tạo tag phiên bản v1.0. o Compo link repo GitHub để thành viên đánh giá. Lab 06 – Design chi tiết lớp & kiến ​​trúc ATM Mục tiêu: từ Use Case và Sequence, sinh viên thiết kế Class Diagram và Package Diagram cho ATM. Công cụ: PlantUML/draw.io, VS Code. Steps

Thư mục: /labs/lab06-atm-class/.
Tạo class-atm.puml: @startuml class ATM {
atmId : int
vị trí: Chuỗi
cashLevel: gấp đôi
xác thực(thẻ:Thẻ, mã pin:Chuỗi) : boolean
rút tiền(thẻ:Thẻ, số tiền:gấp đôi) : Giao dịch
tiền gửi (thẻ: Thẻ, số tiền: gấp đôi) : Giao dịch
chuyển khoản(từ:Tài khoản, đến:Tài khoản, số tiền:gấp đôi) : Giao dịch }
Thẻ lớp {

cardNo : Chuỗi
pinHash: Chuỗi
trạng thái: Chuỗi }
lớp Tài khoản {

accountNo : Chuỗi
cân bằng: gấp đôi
ghi nợ (số tiền: gấp đôi)
tín dụng(số tiền:gấp đôi) }
lớp Giao dịch {

txId: số nguyên
loại: Chuỗi
số tiền: gấp đôi
thời gian: Ngày giờ
trạng thái: Chuỗi }
ATM --> Thẻ ATM --> Thẻ giao dịch --> Tài khoản tài khoản --> Giao dịch @enduml 3. Vẽ sơ đồ gói: UI, Controller, BankService, Hardware. 4. Xuất PNG, ghi chú. Phải nộp: class-atm.puml/png, package-diagram.puml/png, Notes.md. Rubric (10đ): đủ lớp & quan hệ (5), thuộc tính/phương thức đúng (3), Tài liệu & repo (2).

Lab 07 – Phát triển Development Module Rút tiền (Prototype Java/Python) Mục tiêu: viết mã module mô phỏng Rút tiền trong ATM. Công cụ: Java hoặc Python + MySQL Connector. Steps

Thư mục: /labs/lab07-withdraw-module/.
Mã Python (ví dụ): nhập mysql.connector, hashlib
def verify_pin(card_no, pin): conn = mysql.connector.connect(user="root", password="123456", database="atm_demo") cur = conn.cursor() cur.execute("SELECT pin_hash FROM cards WHERE card_no=%s", (card_no,)) row = cur.fetchone() conn.close() trả về row và row[0] == hashlib.sha256(pin.encode()).hexdigest()

def withdraw(card_no, amount): conn = mysql.connector.connect(user="root", password="123456", database="atm_demo") cur = conn.cursor() try: conn.start_transaction() cur.execute("SELECT account_id, balance FROM accounts JOIN cards USING(account_id) WHERE card_no=%s FOR UPDATE",(card_no,)) account_id,balance = cur.fetchone() if balance < amount: raise Exception("Không đủ tiền") cur.execute("UPDATE accounts SET balance=balance-%s WHERE account_id=%s",(amount,account_id)) cur.execute("INSERT INTO transactions(account_id,card_no,atm_id,tx_type,amount,balance_after) GIÁ TRỊ(%s,%s,1,'RÚT TIỀN',%s,%s)",(account_id,card_no,amount,balance-amount)) conn.commit() print("Rút tiền thành công") ngoại trừ Ngoại lệ như e: conn.rollback() print("Error:", e) cuối cùng: conn.close() 3. Test rút tiền với card_no demo. Phải dựa: mã nguồn, ảnh màn hình. Rubric (10đ): kết nối DB đúng (3), xử lý giao dịch (3), kiểm tra số dư (2), nhật ký giao dịch (2).

Lab 08 – Kiểm tra thử ATM (Kiểm tra đơn vị & Kiểm tra tích hợp) Mục tiêu: Thực hành Kiểm tra đơn vị và Kiểm tra tích hợp mô-đun ATM. Công cụ: Python (pytest) hoặc Java (JUnit), Selenium (cho form Đăng nhập). Steps

Thư mục: /labs/lab08-testing/.
Viết bài kiểm tra đơn vị cho hàm verify_pin và rút tiền. o Test case: PIN đúng/sai, đủ tiền/không đủ tiền.
Viết bài kiểm tra tích hợp với Form Đăng nhập (Lab 04) bằng Selenium. o Test case: đăng nhập thành công, đăng nhập sai, đầu vào trống.
Lưu test_withdraw.py, Selenium_test_login.py.
Chạy thử nghiệm → xuất báo cáo. Phải nộp: kiểm tra nguồn + ảnh đạt/không đạt. Phiếu tự đánh giá (10đ): bài kiểm tra đơn vị đủ trường hợp (4), đăng nhập biểu mẫu kiểm tra tích hợp (4), báo cáo (2).
Lab 09 – Quản lý dự án ATM trên Jira (Agile) Mục tiêu: mô phỏng quản lý phát triển hệ thống ATM bằng Scrum. Công cụ: Jira/ClickUp/Trello. Steps

Tạo dự án “Hệ thống ATM”.
Tạo Epic: “Các chức năng cơ bản của ATM”.
Tạo User Stories: o US1: Là khách hàng, tôi muốn rút tiền. o US2: Là khách hàng, tôi muốn kiểm tra số dư. o US3: Là khách hàng, tôi muốn chuyển tài khoản. o US4: Là kỹ thuật viên, tôi muốn bảo trì.
Phân chia thành các Nhiệm vụ/Nhiệm vụ con (ví dụ: thiết kế giao diện người dùng, viết mã, kiểm tra).
Lập Sprint 1 (2 tuần): Rút tiền + Xem số dư.
Giao việc → ảnh chụp màn hình: Backlog, Board, Burndown. Phải nộp: tệp báo cáo (.pdf hoặc .md) với ảnh chụp Jira. Phiếu tự đánh giá (10đ): backlog đầy đủ (3), sprint board (3), báo cáo sprint (2), proof image (2).
Lab 10 – Báo cáo tổng hợp & Demo cuối kỳ Mục tiêu: tổng hợp tất cả lab trước ATM Mini Project. Công cụ: GitHub, PowerPoint/Markdown. Steps

Thư mục: /labs/lab10-final-demo/.
Bao gồm toàn bộ artifacts: o Use Case (Lab 02) o Sequence (Lab 03) o Class Diagram (Lab 06) o ERD + DB (Lab 05) o Form Login (Lab 04) o Withdraw module (Lab 07) o Test (Lab 08) o Jira report (Lab 09)
Viết báo cáo Final-report.md: o Giới thiệu ATM mini-project o Mô hình UML o Cơ sở dữ liệu & mã minh họa o Kết quả test & sprint report o Kết luận & định hướng mở rộng
Demo trên lớp: chạy biểu mẫu đăng nhập → rút kết nối DB demo → trình bày bảng Jira. Phải nộp: Final-report.md, slide PPT (nếu có), link repo GitHub. Phiếu tự đánh giá (10đ): plugin hợp lý đầy đủ (4), chạy bản demo (3), báo cáo & trình bày (3).
