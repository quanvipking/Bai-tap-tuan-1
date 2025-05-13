1. Mong muốn và định hướng của bạn là gì sau khi học xong môn học?
Sau khi học xong môn này, mình mong muốn có thể tự tay làm được một app di động đơn giản, có giao diện dễ nhìn, và có thể chạy thử trên điện thoại thật. Mình định hướng sẽ học thêm về Flutter vì thấy nó hỗ trợ cả Android lẫn iOS, sau này dễ làm dự án freelance hoặc xin thực tập ở các công ty phần mềm. Ngoài ra, mình cũng muốn hiểu rõ cách một ứng dụng hoạt động từ backend tới frontend.

2. Theo bạn, trong tương lai gần (10 năm) lập trình di động có phát triển không? Giải thích tại sao?
Theo mình là có, thậm chí còn phát triển mạnh hơn bây giờ. Lý do là vì ai cũng dùng điện thoại, từ học sinh, sinh viên tới người lớn tuổi. Mọi thứ giờ đều có app: mua đồ ăn, gọi xe, học online, quản lý tài chính... Công nghệ cũng đang thay đổi nhanh, ví dụ như AI hay AR đang được tích hợp vô app di động rất nhiều. Cho nên mình nghĩ lập trình di động vẫn là một hướng đi rất tiềm năng.

3. Viết một ứng dụng có UI như sau đẩy lên github
import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      debugShowCheckedModeBanner: false,
      home: UserProfileScreen(),
    );
  }
}

class UserProfileScreen extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('User Profile'),
        backgroundColor: Colors.blue,
      ),
      body: Center(
        child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: [
            CircleAvatar(
              radius: 50,
              backgroundImage: AssetImage('assets/profile.jpg'), // Thay bằng đường dẫn ảnh
            ),
            SizedBox(height: 10),
            Text(
              'Johan Smith',
              style: TextStyle(fontSize: 22, fontWeight: FontWeight.bold),
            ),
            Text(
              'California, USA',
              style: TextStyle(fontSize: 18, color: Colors.grey),
            ),
            SizedBox(height: 20),
            ElevatedButton(
              onPressed: () {
                // Thêm chức năng cần thiết
              },
              child: Text('Edit Profile'),
            ),
          ],
        ),
      ),
    );
  }
}
