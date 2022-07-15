# Article AI for Image Task

![Image](File/Image/Intro%20image.png)

### **ภาพ (Image)**
 - คือ Array ของตัวเลขในขนาด 2 มิติหรือ 3 มิติ ประกอบด้วด้ย ความกว้าง (width), ความสูง(height), ความลึก (depth)
 - ปกติหลายๆ libraries จะจัดวางแบบ (depth, height, width)
 - เวลาเทรนโมเดลด้วย Pytorch เราจะกำหนดให้ batch size อยู่ด้านหน้าสุดตามด้วยภาพ ดังนี้ 
 
```
    (batch size, depth, height, width) เช่น (32, 3, 224, 224) => batch size = 32,depth= 3, height = 224, width = 224
```
 
![]()
![]()
