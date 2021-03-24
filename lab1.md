# การทดลองทที่ 1 เรื่อง การเขียนโปรแกรมเพื่อรันบนไมโครคอนโทรเลอร์

## วัตถุประสงค์
1. ศึกษาการเขียนโปรแกรมเบื้องต้นเพื่อรันบนไมโครคอนโทรเลอร์
2. ศึกษาความหมาย PlatformIO
 
## อุปกรณ์ที่ใช้
1. ไมโครคอนโทรเลอร์ ESP-01
2. สาย USB 
3. Serial port
4. คอมพิวเตอร์

## ศึกษาข้อมูลเบื้องต้น
* https://platformio.org/
* https://medium.com/sathittham/platformio-%E0%B8%A1%E0%B8%B2%E0%B8%A5%E0%B8%AD%E0%B8%87%E0%B9%80%E0%B8%A5%E0%B9%88%E0%B8%99-platformio-%E0%B9%81%E0%B8%97%E0%B8%99-arduino-ide-%E0%B8%81%E0%B8%B1%E0%B8%99-d9305e6671dd
* https://th.wikipedia.org/wiki/%E0%B9%84%E0%B8%A1%E0%B9%82%E0%B8%84%E0%B8%A3%E0%B8%84%E0%B8%AD%E0%B8%99%E0%B9%82%E0%B8%97%E0%B8%A3%E0%B8%A5%E0%B9%80%E0%B8%A5%E0%B8%AD%E0%B8%A3%E0%B9%8C
* https://youtu.be/NLIUsWLEpmg

## วิธีการทำการทดลอง
1. ต่อไมโครคอนโทรเลอร์ ESP-01 เข้ากับ Serial port แล้วต่อสาย USB เข้าคอมพิวเตอร์
   * ![lab1 1](https://user-images.githubusercontent.com/80879980/112278589-96172300-8cb5-11eb-9b5f-75f22d957d95.png)
2. เปิด code โปรแกรมของตัวอย่างที่ 1
   * ![lab1 2](https://user-images.githubusercontent.com/80879980/112279012-ff973180-8cb5-11eb-9d25-4522c2d431eb.png)
3. พิมพ์คำสั่ง pio run -t upload 
4. กดปุ่มดำ และปุ่ม reset ที่ไมโครคอนโทรเลอร์ ESP-01 เพื่อรับโปรแกรม
   * ![lab1 3](https://user-images.githubusercontent.com/80879980/112279233-44bb6380-8cb6-11eb-9f02-2bc7af6e2a99.png)
5. พิมพ์คำสั่ง pio device monitor เพื่อรันโปรแกรม
6. กดปุ่ม reset ที่ไมโครคอนโทรเลอร์ ESP-01 เพื่อเริ่มใหม่
   * ![lab1 4](https://user-images.githubusercontent.com/80879980/112279620-b1cef900-8cb6-11eb-95a4-6968b5afdb0c.png)

