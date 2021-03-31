# การทดลองที่ 7 เรื่อง การเขียนโปรแกรมเอ้าพุทสัญญาณดิจิทัล

## วัตถุประสงค์
1. ศึกษาการเขียนโปรแกรมเอ้าพุทสัญญาณดิจิทัลเพื่อรันบนไมโครคอนโทรเลอร์
2. ศึกษาการใช้ Adapter port

## อุปกรณ์ที่ใช้
1. ไมโครคอนโทรเลอร์ ESP-01
2. สาย USB 
3. Serial port
4. คอมพิวเตอร์
5. Adapter port
6. LED 

## ศึกษาข้อมูลเบื้องต้น
* https://youtu.be/CCnN1WJsXQY
* https://www.primusthai.com/primus/Knowledge/info?ID=132
  * สัญญาณดิจิตอล (Digital Signal) หมายถึง สัญญาณที่เกี่ยวข้องกับข้อมูลแบบไม่ต่อเนื่อง (Discrete Data) ที่มีขนาดแน่นอนซึ่งขนาดดังกล่าวอาจกระโดดไปมาระหว่างค่าสองค่า คือ สัญญาณระดับสูงสุดและสัญญาณระดับต่ำสุด ซึ่งสัญญาณดิจิตอลนี้เป็นสัญญาณที่คอมพิวเตอร์ใช้ในการทำงานและติดต่อสื่อสารกันเป็นค่าของเลขลงตัว โดยปกติมักแทนด้วยระดับแรงดันที่แสดงสถานะเป็น "0" และ "1" หรืออาจจะมีหลายสถานะซึ่งจะกล่าวถึงในเรื่องระบบสื่อสารดิจิตอลมีค่าที่ตั้งไว้ (Threshold) เป็นค่าบอกสถานะ ถ้าสูงเกินค่าที่ตั้งไว้สถานะเป็น "1" ถ้าต่ำกว่าค่าที่ตั้งไว้สถานะเป็น "0" ซึ่งมีข้อดีในการทำให้เกิดความผิดพลาดน้อยลง
  * สัญญาณอนาลอก (Analog Signal) หมายถึง สัญญาณข้อมูลแบบต่อเนื่อง (Continuous Data) มีขนาดของสัญญาณไม่คงที่ มีการเปลี่ยนแปลงขนาดของสัญญาณแบบค่อยเป็นค่อยไป มีลักษณะเป็นเส้นโค้งต่อเนื่องกันไป โดยการส่งสัญญาณแบบอนาล็อกจะถูกรบกวนให้มีการแปลความหมายผิดพลาดได้ง่าย เช่น สัญญาณเสียงในสายโทรศัพท์ เป็นต้น

## วิธีการทำการทดลอง
1. ต่อไมโครคอนโทรเลอร์ ESP-01 เข้ากับ Adapter port จากนั้นต่อทั้งหมดเข้ากับ Serial port แล้วต่อสาย USB เข้าคอมพิวเตอร์
   * ![lab3 1](https://user-images.githubusercontent.com/80879980/112292056-4a6b7600-8cc3-11eb-8237-0c01f0754c19.png)
2. เปิด code โปรแกรมของตัวอย่างที่ 3
   * ![lab](https://user-images.githubusercontent.com/80879980/113111136-10095800-9232-11eb-88b8-0f7dc2ae856c.png)
3. พิมพ์คำสั่ง pio run -t upload เพื่ออัพโหลดโปรแกรมลงไมโครคอนโทรเลอร์ ESP-01
4. กดปุ่ม upload และปุ่ม reset ที่ไมโครคอนโทรเลอร์ ESP-01 เพื่อรับโปรแกรม
   * ![lab3 3](https://user-images.githubusercontent.com/80879980/112292783-07f66900-8cc4-11eb-923a-8fa061152b36.png)
5. พิมพ์คำสั่ง pio device monitor เพื่อรันโปรแกรม
6. กดปุ่ม reset ที่ไมโครคอนโทรเลอร์ ESP-01 เพื่อเริ่มรันโปรแกรมใหม่

## การบันทึกผลการทดลอง
จากการทดลอง เมื่อทำการอัพโหลดโปรแกรมลงบนไมโครคอนโทรเลอร์ ESP-01 และรันโปรแกรม จะพบว่า ไมโครคอนโทรเลอร์จะนับเวลาไปเรื่อยๆ และแสดงผลบนหน้าจอว่า Time (seconds): 1...2...3... เมื่อครบทุกๆ 1 นาที LED ที่ Port 0 จะส่องสว่าง และจะแสดงผลบนหน้าจอมอนิเตอร์ว่า Time (minutes): 1...2...3... 
  * ![labt](https://user-images.githubusercontent.com/80879980/113116341-8bb9d380-9237-11eb-8f1d-576197b26f0b.png)

## อภิปรายผลการทดลอง
จากการทดลองจะเห็นได้ว่าไมโครคอนโทรเลอร์ ESP-01 สามารถส่งสัญญาณ output ไปที่ Port ต่างๆที่เชื่อมต่อได้ โดยเราสามารถสร้างรูปแบบของโปรแกรมให้เหมาะสมตามการนำไปใช้งานในชีวิตประจำวัน หรือ ในอุตสาหกรรม

## การนำไปใช้ประโยชน์
นำไปใช้ในการจับเวลา และสามารถนำเอาโปรแกรมเบื้องต้นที่กล่าวมาไปปรับปรุง จะทำให้สามารถได้โปรแกรมที่มีประสิทธิภาพมากยิ่งขึ้น โดยสามารถนำไปใช้ในชีวิตประจำวัน หรือ ในอุตสาหกรรมได้ เช่น สัญญาณไฟจราจร ตัวจับเวลานับถอยหลัง ฯลฯ

## คำถามหลังการทดลอง
สัญญาณอนาลอก (Analog Signal) กับ สัญญาณดิจิตอล (Digital Signal) ต่างกันอย่างไร? 
* ตอบ สัญญาณอนาลอก กับ สัญญาณดิจิตอล มีความแตกต่างกันทางความต่อเนื่องของสัญญาณและความแม่นยำของสัญญาณ