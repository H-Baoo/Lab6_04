Đầu tiên mở terminal cd thư mục simple_auth cài: npm install

A. Chạy server node basic_auth.js

B1: Chạy server: node basic_auth.js

B2: Mở POSTMAN 
- Chạy URL: GET http://localhost:3000/
  Khi send sẽ hiện ra "Welcome! Visit first public resource."
<img width="1919" height="1079" alt="image" src="../simple_auth/public/image/public_1.png" />

- Chạy URL: GET http://localhost:3000/public
  Khi send sẽ hiện ra "Welcome! Visit second public resource."
<img width="1919" height="1079" alt="image" src="../simple_auth/public/image/public_2.png" />

- Chạy URL: GET http://localhost:3000/secure
  Khi đó sẽ chọn Authorzatiton, ở Auth type sẽ chọn Basic Auth 
  
 + Nếu nhập Username, Password đúng thì khi send sẽ gửi trả về "You have accessed a protected resource 🎉"
<img width="1919" height="1079" alt="image" src="../simple_auth/public/image/secure_1.png" />

 + Nếu nhập Username, Password sai thì khi send sẽ gửi trả về "Access denied."
<img width="1919" height="1079" alt="image" src="../simple_auth/public/image/secure_2.png" />

B. Chạy server node cookie_auth.js

B1: Chạy server node cookie_auth.js

B2: Mở POSTMAN 

- Chạy URL: POST http://localhost:3001/login trong body nhập {"username": "admin","password": "12345"}
 + Nếu đúng thì khi send sẽ gửi trả về "Logged in!" và lưu cookie
<img width="1919" height="1079" alt="image" src="../simple_auth/public/image/login_1.png" />
<img width="1919" height="1079" alt="image" src="../simple_auth/public/image/login_2.png" />
<img width="1919" height="1079" alt="image" src="../simple_auth/public/image/login_3.png" />

 + Nếu sai thì khi send sẽ gửi trả về "Invalid credentials"
<img width="1919" height="1079" alt="image" src="../simple_auth/public/image/login_4.png" />

- Chạy URL: GET http://localhost:3001/profile Nếu cookie hợp lệ, trả về: Welcome user 1, your cookie is valid.
<img width="1919" height="1079" alt="image" src="../simple_auth/public/image/profile_1.png" />

- Chạy URL: POST http://localhost:3001/logout thì Cookie bị xóa cả trên browser/Postman và trong MongoDB.
<img width="1919" height="1079" alt="image" src="../simple_auth/public/image/logout_1.png" />
<img width="1919" height="1079" alt="image" src="../simple_auth/public/image/logout_2.png" />
<img width="1919" height="1079" alt="image" src="../simple_auth/public/image/logout_3.png" />

