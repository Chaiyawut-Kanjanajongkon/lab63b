# การทดลองที่ 2 เรื่อง การเขียนโปรแกรมค้นหาไวไฟ

## วัตถุประสงค์
1. ศึกษาการเขียนโปรแกรมค้นหาไวไฟเพื่อรันบนไมโครคอนโทรเลอร์

## อุปกรณ์ที่ใช้
1. ไมโครคอนโทรเลอร์ ESP-01
2. สาย USB 
3. Serial port
4. คอมพิวเตอร์

## ศึกษาข้อมูลเบื้องต้น
https://www.youtube.com/watch?v=yBjab0UNuB8&t=4s

## วิธีการทำการทดลอง
1. ต่อไมโครคอนโทรเลอร์ ESP-01 เข้ากับ Serial port แล้วต่อสาย USB เข้าคอมพิวเตอร์
   * ![lab1 1](https://user-images.githubusercontent.com/80879980/112278589-96172300-8cb5-11eb-9b5f-75f22d957d95.png)
2. เปิด code โปรแกรมของตัวอย่างที่ 2
   * ![lab2 1](https://user-images.githubusercontent.com/80879980/112285667-24db6e00-8cbd-11eb-9413-eeff2b6e9f0a.png)
   * ![lab2 2](https://user-images.githubusercontent.com/80879980/112285750-39b80180-8cbd-11eb-9a4a-42afd281a5af.png)
3. พิมพ์คำสั่ง pio run -t upload เพื่ออัพโหลดโปรแกรมลงไมโครคอนโทรเลอร์ ESP-01
4. กดปุ่มดำ และปุ่ม reset ที่ไมโครคอนโทรเลอร์ ESP-01 เพื่อรับโปรแกรม
   * ![lab1 3](https://user-images.githubusercontent.com/80879980/112279233-44bb6380-8cb6-11eb-9f02-2bc7af6e2a99.png)
5. พิมพ์คำสั่ง pio device monitor เพื่อรันโปรแกรม
