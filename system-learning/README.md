# Hệ thống học trực tuyến

Thiết kế và vận hành cơ sở dữ liệu cho hệ thống học trực tuyến của một trường đại học. Hệ thống quản lý sinh viên, khóa học, giảng viên, các lượt đăng ký học và kết quả học tập. Bài làm theo đủ quy trình **DDL → INSERT → UPDATE → DELETE → SELECT**.

> Đề bài gọi giảng viên là *Teacher* và kết quả là *Score* trong phần mô tả, nhưng yêu cầu tạo bảng `Instructor` và `Result`. Bài làm dùng tên bảng theo phần yêu cầu: `Instructor` (Teacher) và `Result` (Score).

## 1. Sơ đồ ERD

[![ERD Hệ thống học trực tuyến](erd-online-learning.png)](erd-online-learning.png)

[Xem sơ đồ ERD trên draw.io](https://www.draw.io/?title=erd-online-learning.drawio#R7V3bcuI4EP0aXqd8AUIeiUN2piaXXSbZyxMlsADVCIuSRRLy9dvyFdsiAUIcB6mKpKyWLGT1aR%2B5uy1arrd4%2FoOj5fyG%2BZi2HGvGid9yL1uOY8EfCJZohjcE7qDlepwxER8tnj1M5XnFs6621NppnxwHYpcTxOiXWPmycXTiI6KrZDQFeSjWNJGHc7SUhwKNpegiFIiLX%2BRFytw2CCYsEIgEmIPAjsqUomVIouaXlpTMCfWv0ZqtRNpRWrqYkmfsD9lTmJzN2dM1dJYWp9D5r2QwsowomQVwPIGhym%2BE8yn1GGU8Gq3rI9ybTqJhcvYbb9R0Jz08nqZdxuO35fiTmcBc4Oets2pnugL9YrbAgq%2BhSXJCO9HtOi72kuIT8cU8FrndRDbHZDZPO213YyEKY8Es6zlXIRwkWnxDoyNuVZT6ujZh2uH654yTF6lDmqhrU8NR%2BYksKArwd4z8kuiC%2BetEtKmIgAVYiQSfs%2BU94jMsEsGSkUBEV9%2B5gA9cgWd967Q6MFYPynZeho9szoXHAlAuIE72gVEonnAoKhonwRxzIuWCLZMvo3iafi9PtCCPx0wItkgAthMaClZURUUCA7COnWDg9I6LgtHvCg7%2B%2FLkVCXBdgiA6xBOBgllk4gwuf0olOC7nxIdeYysPZJNclwqF76WCbNrL%2Bijb%2FKbBWnurKDGLqpY21NLZUytJZ%2Fmc7d0bonD7CpAAC1oFflhRdTbO%2FbX%2FWNF%2BmFRCc6AHtw%2F%2Fve%2F9YcvpdVrOeS3ISO%2Fbsf6PBJRwiSYkmF3HTbsl6HSOB5XnomI3Ddo%2BKnR26u7DsGMb%2FmgSf3SdT%2BEPW8EfGrOHrRN72Ar2mK4oHQVogTPy%2BLs%2FTPjDtqyIQazbu3v5%2F%2BH6%2BpTo5EhY0YQ%2BHEMfTaKPc%2BtT6MMx9FExCl3ow1HQhw%2FfM2LT0ZhwGGNKIZf9%2B4GhjdcxogltuIY2mkQbtt37FN5wFbzx8JfGzOHqxByugjnwAhFqHjoOxMlps8cg4HCbXqgCWeWqLxvLmk6nzkQZy%2FK7426n%2BzGxrI5zYDDLPgof5Noz8awaVwZFo2lISKuAhS1RLe9Kw9BWxUhOfJlQBIIJcO0d4NoBMLqsF0yYq3m0Um%2Bkq4AFQyvqu4StGa2oIl8TtuIhNqzyDrzowyom%2BtU0Vqk3AFbAgomBqaxDIzpRRcJwVD%2BSAbFyHOxycNV%2FuJbeTO9hOBzc3o%2FiCu28mjtg5rQpxYvWHBXsbIq%2FbnJ%2BB%2Ff8tsqh2XPGbveDHJoQLjjQo3nWPgYxxKoz3swaFwi5tTTEk5lhwOTmV23ixJcFue7NE%2Ba%2BT5hv4ESHpYDxVzaLOOr1VWYYME%2BUZYvQhDZecUyapPzDsaIHdRinZJOoo16HZIYBQx1li9CEOpTp%2BDiccLIUhAUK6nA6p%2FbgcRx46MEWJhO%2FSWxRcyJ%2BBgJDF2WT0IQuVDn4goFdj0IchkAYYcYYP26jWNX3gfdTypzuTERzm3rateQOV2fuaBvuaBJ3pDtL1csdbQV3XGkc3mhrxB5tBXsQaS2riWB8a4jDOKleAcppU8ePDB0V4JSrvmzKA7Yh6eFMlfJw3j1z0UelPLR7n%2FoSV64%2Bk%2FZQ48KgaDUNSX0oYMGkP6jt48TXCEUMHLRO0D4VYgfM6LJcMCkRzSOVetMiClgwDkuVdWhEKWbXwkOePXdAjD6EYhIlmkYo9SZLFLBgdqJS24dGlOKY%2FajeQSdaZlEMcbii1e2oNsVfeCsq3N2yFdXZ%2Bdiy6tmKynXr%2FWGVWHXGhVnj4iC3loa4LzMMmI1CylrSw3eZA8DsO7W30%2FINoOiwIDDOymbRR72OygwDhj6qdwVbI%2Fow%2B0sdzh62zuxhPJNNYo96vZIZBkyIq2wRmtCGyg%2B5gKFhvhiFE8Y3dpIaeD9u%2BuB57MHzsefEHsk0Q99qDZwWJIGdZ7cyrXyTbyBHDyIxb3c1iUhqfrsrA4FhkrJJaMIkqre7piSQb3cZHjkObk6ZRzimVY1jf4ZTc4RpImI9xBTJd8sHec3FXCxoYq8RefQ5j5AwGC5Q4N9FesaBn4tfMGf37AYF6%2FSUK0JT%2FoGWG6UYEP8kU%2BNkqpQjez3qBBcCj98TrP4NaMcSKRHtuoE%2Bjy79sfi177lrQ4f2SU95aWfE7TNu1zfjzknPuOLFjOKsv%2FFC0kfMuPvqjMOSbs5mDHjqCLN9F%2BADJhs%2FE%2FFv2haO%2F5PH3zrRmXC5WZUs5HWHqkjxSxVFFb3hFXuviqDIGRObRMHRcn7DfCxb%2FA8%3D)

| Quan hệ | Loại | Thể hiện trong SQL |
|---|---|---|
| Instructor – Course | 1 – N: một giảng viên dạy nhiều khóa học | `Course.instructor_id` là khóa ngoại tới `Instructor` |
| Student – Course | N – N: sinh viên đăng ký nhiều khóa, khóa có nhiều sinh viên | Bảng trung gian `Enrollment` |
| Enrollment – Result | 1 – 0..1: mỗi lượt đăng ký có tối đa một kết quả | `Result` có khóa chính và khóa ngoại kép `(student_id, course_id)` tới `Enrollment` |

## 2. Phần I – Thiết kế & tạo bảng (DDL)

### Đối chiếu nghiệp vụ với ràng buộc

| Quy tắc nghiệp vụ | Ràng buộc |
|---|---|
| Mỗi sinh viên, khóa học, giảng viên có mã riêng | `PRIMARY KEY` trên `student_id`, `course_id`, `instructor_id` |
| Email sinh viên (và giảng viên) không được trùng | `UNIQUE (email)` |
| Họ tên, ngày sinh, email, tên khóa học là bắt buộc | `NOT NULL` |
| Số buổi học phải hợp lệ | `CHECK (total_sessions > 0)` |
| Một giảng viên dạy nhiều khóa học | `FOREIGN KEY Course.instructor_id → Instructor` |
| Sinh viên **không được đăng ký trùng** một khóa học | `PRIMARY KEY (student_id, course_id)` trong `Enrollment` |
| Mỗi lượt đăng ký lưu ngày đăng ký | `enroll_date DATE NOT NULL DEFAULT (CURRENT_DATE)` |
| Điểm từ 0 đến 10 | `CHECK (midterm_score BETWEEN 0 AND 10)`, `CHECK (final_score BETWEEN 0 AND 10)` |
| **Mỗi sinh viên chỉ có một kết quả** cho mỗi khóa học | `PRIMARY KEY (student_id, course_id)` trong `Result` |
| Chỉ có kết quả khi sinh viên **đã đăng ký** khóa học | `FOREIGN KEY (student_id, course_id) → Enrollment` |

### Lựa chọn kiểu dữ liệu

- **Mã (`CHAR(5)`):** các mã có độ dài cố định (`SV001`, `KH001`, `GV001`), nên dùng `CHAR` để tiết kiệm bộ nhớ và so sánh nhanh.
- **Họ tên, email (`VARCHAR(100)`), mô tả (`VARCHAR(255)`):** độ dài thay đổi, nên `VARCHAR` chỉ tốn đúng số byte cần dùng.
- **Ngày sinh, ngày đăng ký (`DATE`):** chỉ cần ngày, tháng, năm.
- **Điểm (`DECIMAL(4,2)`):** lưu chính xác các mức như `8.25`, `9.50`, không bị sai số như `FLOAT`.
- **Điểm cho phép `NULL`:** nghĩa là chưa có điểm, ví dụ sinh viên chưa thi cuối kỳ. Trong MySQL, `CHECK` với giá trị `NULL` không bị coi là vi phạm.

### Thứ tự tạo bảng

Bảng cha phải có trước bảng con: `Student` → `Instructor` → `Course` → `Enrollment` → `Result`. Khi xóa bảng thì làm theo thứ tự ngược lại.

## 3. Phần II – Nhập dữ liệu ban đầu

- 5 sinh viên (`SV001`–`SV005`), 5 giảng viên (`GV001`–`GV005`), 5 khóa học (`KH001`–`KH005`).
- 8 lượt đăng ký và 8 kết quả học tập. Có kết quả chưa có điểm cuối kỳ (`NULL`).
- Dữ liệu được thêm theo thứ tự bảng cha trước, bảng con sau, để không vi phạm khóa ngoại.

## 4. Phần III – Cập nhật dữ liệu

Mọi lệnh `UPDATE` đều có `WHERE` theo **khóa chính**, nên chỉ tác động đúng một dòng.

| Yêu cầu | Lệnh |
|---|---|
| Cập nhật email sinh viên SV003 | `UPDATE Student SET email = '...' WHERE student_id = 'SV003';` |
| Cập nhật mô tả khóa học KH002 | `UPDATE Course SET description = '...' WHERE course_id = 'KH002';` |
| Cập nhật điểm cuối kỳ SV001 – KH002 | `UPDATE Result SET final_score = 8.0 WHERE student_id = 'SV001' AND course_id = 'KH002';` |

Với bảng `Result`, khóa chính gồm **2 cột**, nên `WHERE` phải có đủ cả `student_id` và `course_id`. Nếu chỉ lọc theo `student_id`, điểm của sinh viên đó ở **mọi khóa học** sẽ bị sửa.

## 5. Phần IV – Xóa dữ liệu

Lượt đăng ký `SV005 – KH005` không hợp lệ cần bị xóa. Lượt đăng ký này đã có kết quả học tập, và `Result` tham chiếu tới `Enrollment` bằng khóa ngoại. Vì vậy phải **xóa kết quả (bảng con) trước**, rồi mới xóa lượt đăng ký (bảng cha):

```sql
DELETE FROM Result
WHERE student_id = 'SV005' AND course_id = 'KH005';

DELETE FROM Enrollment
WHERE student_id = 'SV005' AND course_id = 'KH005';
```

Nếu xóa `Enrollment` trước, MySQL báo lỗi vi phạm khóa ngoại và từ chối lệnh xóa. Đây chính là ràng buộc giúp hệ thống không có "kết quả mồ côi", tức điểm của một khóa học mà sinh viên không đăng ký.

## 6. Phần V – Truy vấn dữ liệu

| Yêu cầu | Câu lệnh |
|---|---|
| Danh sách sinh viên | `SELECT student_id, full_name, date_of_birth, email FROM Student;` |
| Danh sách giảng viên | `SELECT instructor_id, full_name, email FROM Instructor;` |
| Danh sách khóa học | `SELECT course_id, course_name, description, total_sessions, instructor_id FROM Course;` |
| Các lượt đăng ký | `SELECT student_id, course_id, enroll_date FROM Enrollment;` |
| Kết quả học tập | `SELECT student_id, course_id, midterm_score, final_score FROM Result;` |

Các câu truy vấn liệt kê rõ tên cột thay vì `SELECT *`, để kết quả không đổi khi bảng được thêm cột sau này.

## 7. Kiểm thử ràng buộc

| Lệnh thử | Kết quả |
|---|---|
| Đăng ký lại `SV001 – KH001` | ❌ Bị từ chối: trùng khóa chính (đăng ký trùng khóa học) |
| Thêm sinh viên có email đã tồn tại | ❌ Bị từ chối: vi phạm `UNIQUE` |
| Nhập điểm giữa kỳ = 11 | ❌ Bị từ chối: vi phạm `CHECK` (0–10) |
| Nhập kết quả cho `SV003 – KH001` (chưa đăng ký) | ❌ Bị từ chối: vi phạm khóa ngoại tới `Enrollment` |
| Xóa lượt đăng ký `SV001 – KH001` khi vẫn còn kết quả | ❌ Bị từ chối: vi phạm khóa ngoại |

## 8. Script SQL hoàn chỉnh

```sql
-- =====================================================
-- HỆ THỐNG HỌC TRỰC TUYẾN
-- DDL (CREATE) -> DML (INSERT, UPDATE, DELETE) -> SELECT
-- MySQL 8.0.16+ (CHECK cần 8.0.16+, DEFAULT (CURRENT_DATE) cần 8.0.13+)
-- =====================================================

-- =====================================================
-- PHẦN I: THIẾT KẾ & TẠO BẢNG (DDL)
-- =====================================================
CREATE DATABASE IF NOT EXISTS online_learning
    DEFAULT CHARACTER SET utf8mb4;
USE online_learning;

-- Xóa bảng cũ (nếu có): bảng con trước, bảng cha sau
DROP TABLE IF EXISTS Result;
DROP TABLE IF EXISTS Enrollment;
DROP TABLE IF EXISTS Course;
DROP TABLE IF EXISTS Instructor;
DROP TABLE IF EXISTS Student;

-- 1. Sinh viên
CREATE TABLE Student (
    student_id    CHAR(5)      NOT NULL,
    full_name     VARCHAR(100) NOT NULL,
    date_of_birth DATE         NOT NULL,
    email         VARCHAR(100) NOT NULL,
    CONSTRAINT pk_student       PRIMARY KEY (student_id),
    CONSTRAINT uq_student_email UNIQUE (email),
    CONSTRAINT chk_student_email CHECK (email LIKE '%_@_%._%')
);

-- 2. Giảng viên
CREATE TABLE Instructor (
    instructor_id CHAR(5)      NOT NULL,
    full_name     VARCHAR(100) NOT NULL,
    email         VARCHAR(100) NOT NULL,
    CONSTRAINT pk_instructor       PRIMARY KEY (instructor_id),
    CONSTRAINT uq_instructor_email UNIQUE (email),
    CONSTRAINT chk_instructor_email CHECK (email LIKE '%_@_%._%')
);

-- 3. Khóa học (1 giảng viên dạy nhiều khóa học)
CREATE TABLE Course (
    course_id      CHAR(5)      NOT NULL,
    course_name    VARCHAR(100) NOT NULL,
    description    VARCHAR(255),
    total_sessions INT          NOT NULL,
    instructor_id  CHAR(5)      NOT NULL,
    CONSTRAINT pk_course          PRIMARY KEY (course_id),
    CONSTRAINT chk_course_sessions CHECK (total_sessions > 0),
    CONSTRAINT fk_course_instructor
        FOREIGN KEY (instructor_id) REFERENCES Instructor (instructor_id)
);

-- 4. Đăng ký học (N - N giữa Student và Course)
CREATE TABLE Enrollment (
    student_id  CHAR(5) NOT NULL,
    course_id   CHAR(5) NOT NULL,
    enroll_date DATE    NOT NULL DEFAULT (CURRENT_DATE),
    CONSTRAINT pk_enrollment PRIMARY KEY (student_id, course_id),   -- không đăng ký trùng
    CONSTRAINT fk_enrollment_student
        FOREIGN KEY (student_id) REFERENCES Student (student_id),
    CONSTRAINT fk_enrollment_course
        FOREIGN KEY (course_id)  REFERENCES Course (course_id)
);

-- 5. Kết quả học tập (mỗi lượt đăng ký có tối đa 1 kết quả)
CREATE TABLE Result (
    student_id    CHAR(5)      NOT NULL,
    course_id     CHAR(5)      NOT NULL,
    midterm_score DECIMAL(4, 2),
    final_score   DECIMAL(4, 2),
    CONSTRAINT pk_result PRIMARY KEY (student_id, course_id),       -- 1 kết quả / sinh viên / khóa học
    CONSTRAINT chk_result_midterm CHECK (midterm_score BETWEEN 0 AND 10),
    CONSTRAINT chk_result_final   CHECK (final_score   BETWEEN 0 AND 10),
    CONSTRAINT fk_result_enrollment
        FOREIGN KEY (student_id, course_id) REFERENCES Enrollment (student_id, course_id)
);

-- =====================================================
-- PHẦN II: NHẬP DỮ LIỆU BAN ĐẦU (bảng cha trước, bảng con sau)
-- =====================================================
INSERT INTO Student (student_id, full_name, date_of_birth, email) VALUES
    ('SV001', 'Nguyễn Văn An',   '2005-03-12', 'an.nguyen@student.edu.vn'),
    ('SV002', 'Trần Thị Bình',   '2005-07-25', 'binh.tran@student.edu.vn'),
    ('SV003', 'Lê Hoàng Cường',  '2004-11-02', 'cuong.le@student.edu.vn'),
    ('SV004', 'Phạm Thu Dung',   '2005-01-18', 'dung.pham@student.edu.vn'),
    ('SV005', 'Hoàng Minh Đức',  '2004-09-30', 'duc.hoang@student.edu.vn');

INSERT INTO Instructor (instructor_id, full_name, email) VALUES
    ('GV001', 'TS. Nguyễn Quang Huy', 'huy.nq@university.edu.vn'),
    ('GV002', 'ThS. Trần Mai Lan',    'lan.tm@university.edu.vn'),
    ('GV003', 'TS. Lê Văn Khoa',      'khoa.lv@university.edu.vn'),
    ('GV004', 'ThS. Phạm Ngọc Anh',   'anh.pn@university.edu.vn'),
    ('GV005', 'PGS. Đỗ Thanh Tùng',   'tung.dt@university.edu.vn');

INSERT INTO Course (course_id, course_name, description, total_sessions, instructor_id) VALUES
    ('KH001', 'Cơ sở dữ liệu',          'Thiết kế CSDL quan hệ và ngôn ngữ SQL',  15, 'GV001'),
    ('KH002', 'Lập trình Python',       'Python cơ bản cho người mới bắt đầu',    20, 'GV002'),
    ('KH003', 'Cấu trúc dữ liệu',       'Mảng, danh sách liên kết, cây, đồ thị',   15, 'GV003'),
    ('KH004', 'Mạng máy tính',          'Mô hình OSI, TCP/IP và định tuyến',      12, 'GV004'),
    ('KH005', 'Trí tuệ nhân tạo',       'Tìm kiếm, học máy và mạng nơ-ron',       18, 'GV001');

INSERT INTO Enrollment (student_id, course_id, enroll_date) VALUES
    ('SV001', 'KH001', '2026-09-01'),
    ('SV001', 'KH002', '2026-09-01'),
    ('SV002', 'KH001', '2026-09-02'),
    ('SV002', 'KH003', '2026-09-02'),
    ('SV003', 'KH004', '2026-09-03'),
    ('SV004', 'KH005', '2026-09-03'),
    ('SV005', 'KH002', '2026-09-04'),
    ('SV005', 'KH005', '2026-09-05');   -- lượt đăng ký không hợp lệ (sẽ xóa ở Phần IV)

INSERT INTO Result (student_id, course_id, midterm_score, final_score) VALUES
    ('SV001', 'KH001', 8.0,  8.5),
    ('SV001', 'KH002', 7.5,  NULL),     -- chưa thi cuối kỳ
    ('SV002', 'KH001', 9.0,  9.5),
    ('SV002', 'KH003', 6.5,  7.0),
    ('SV003', 'KH004', 5.0,  6.0),
    ('SV004', 'KH005', 8.5,  9.0),
    ('SV005', 'KH002', 7.0,  7.5),
    ('SV005', 'KH005', 4.0,  NULL);

-- =====================================================
-- PHẦN III: CẬP NHẬT DỮ LIỆU (luôn có WHERE theo khóa chính)
-- =====================================================
-- 1. Cập nhật email cho sinh viên SV003
UPDATE Student
SET email = 'cuong.lehoang@student.edu.vn'
WHERE student_id = 'SV003';

-- 2. Cập nhật mô tả cho khóa học KH002
UPDATE Course
SET description = 'Python từ cơ bản đến xử lý dữ liệu với pandas'
WHERE course_id = 'KH002';

-- 3. Cập nhật điểm cuối kỳ cho sinh viên SV001 ở khóa KH002
UPDATE Result
SET final_score = 8.0
WHERE student_id = 'SV001' AND course_id = 'KH002';

-- =====================================================
-- PHẦN IV: XÓA DỮ LIỆU
-- Lượt đăng ký SV005 - KH005 không hợp lệ
-- Phải xóa kết quả (bảng con) TRƯỚC, rồi mới xóa lượt đăng ký (bảng cha)
-- =====================================================
DELETE FROM Result
WHERE student_id = 'SV005' AND course_id = 'KH005';

DELETE FROM Enrollment
WHERE student_id = 'SV005' AND course_id = 'KH005';

-- =====================================================
-- PHẦN V: TRUY VẤN DỮ LIỆU
-- =====================================================
-- 1. Danh sách sinh viên
SELECT student_id, full_name, date_of_birth, email
FROM Student;

-- 2. Danh sách giảng viên
SELECT instructor_id, full_name, email
FROM Instructor;

-- 3. Danh sách khóa học
SELECT course_id, course_name, description, total_sessions, instructor_id
FROM Course;

-- 4. Các lượt đăng ký khóa học
SELECT student_id, course_id, enroll_date
FROM Enrollment;

-- 5. Kết quả học tập
SELECT student_id, course_id, midterm_score, final_score
FROM Result;
```
