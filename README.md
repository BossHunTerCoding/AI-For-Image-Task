<h1 align="center"> 
 [ Article AI For Image Task ]
<h1>
 
![Image](File/Image/Intro%20image.png)

### Overview
 - **ภาพ (Image) ใน Deep Learning**
 - **APPLICATION OF DEEP LEARNING FOR IMAGE ANALYSIS**
 >- **Image Classification**
 >>- **Object Detection**<br>
 >>- **Semantic Segmentation**<br>
 >>- **Instance Segmentation**
 
### ภาพ (Image)

 - คือ **Array** ของตัวเลขในขนาด 2 มิติ ประกอบด้วย ความกว้าง (width), ความสูง (height) <br>หรือ 3 มิติ ประกอบด้วย ความกว้าง (width), ความสูง (height), ความลึก (depth)
 - ปกติเทรนโมเดลหลายๆ **libraries** จะจัดวางแบบ <br>(depth, height, width)
 
```java
 เช่น (3, 254, 224) => depth = 3, height = 254, width = 224
```
 
 - เวลาเทรนโมเดลด้วย **Pytorch** เราจะกำหนดให้ **batch size** อยู่ด้านหน้าสุดตามด้วยขนาดภาพ ดังนี้ <br>(batch size, depth, height, width) 
 
```java
 เช่น (32, 3, 224, 224) => batch size = 32,depth = 3, height = 224, width = 224
```
 
<br>
 
# APPLICATION OF DEEP LEARNING FOR IMAGE ANALYSIS
 
### #Image Classification
 - การจำแนกรูปภาพ เป็นงานพื้นฐานที่พยายามทำความเข้าใจภาพรวมทั้งหมด
 - เป้าหมายเพื่อกำหนดป้ายหรือลาเบล (คือบอกให้ได้เป็นรูปอะไร)
 - โดยทั่วไป การจัดประเภทรูปภาพหมายถึง รูปภาพที่มีเพียงหนึ่ง **Object** เท่านั้นที่ปรากฏและถูกวิเคราะห์
 
ในทางตรงกันข้าม การตรวจจับวัตถุ **(object detection)** เกี่ยวข้องกับงานการจำแนกประเภท **(classification)** <br>และการหาขอบของภาพ และใช้ในการวิเคราะห์กรณีที่สมจริงมากขึ้นซึ่งอาจมีวัตถุหลายชิ้นอยู่ในรูปภาพ
 
 <p align="center">
  <img src="File/Image/Citation needed.png" width="800"><br>
  <img src="File/Image/gentle_guide_obj_det_demo.gif" width="800">
 <p>
 
### #Object Detection
&emsp;การตรวจจับวัตถุ (object detection) หมายถึงความสามารถของระบบคอมพิวเตอร์และซอฟต์แวร์ในการค้นหาวัตถุในภาพ/ฉากและระบุแต่ละวัตถุ <br>การตรวจจับวัตถุถูกนำมาใช้กันอย่างแพร่หลายในการตรวจจับใบหน้า การตรวจจับยานพาหนะ การนับคนเดินถนน รูปภาพบนเว็บ ระบบรักษาความปลอดภัย และรถยนต์ไร้คนขับ มีหลายวิธีที่สามารถใช้การตรวจจับวัตถุได้เช่นเดียวกันในหลายๆด้านของการปฏิบัติ เช่นเดียวกับเทคโนโลยีคอมพิวเตอร์อื่น ๆ การใช้การตรวจจับวัตถุอย่างสร้างสรรค์และน่าทึ่งมากมายจะมาจากความพยายามของโปรแกรมเมอร์คอมพิวเตอร์และนักพัฒนาซอฟต์แวร์
 - เป็นเทคโนโลยีคอมพิวเตอร์ ที่เกี่ยวข้องกับการมองเห็นด้วยคอมพิวเตอร์และการประมวลผลภาพที่เกี่ยวข้องกับการตรวจจับ <br>อินสแตนซ์ของวัตถุเชิงความหมายบางประเภท (เช่นมนุษย์ อาคาร หรือรถยนต์) ในภาพและวิดีโอดิจิทัล
<p>
&emsp;หนึ่งในสาขาวิชาที่สำคัญของ AI คือ Computer Vision <br>
Computer Vision เป็นศาสตร์ของคอมพิวเตอร์และระบบซอฟต์แวร์ที่สามารถจดจำและเข้าใจภาพและฉากต่างๆ <br>Computer Vision ยังประกอบด้วยแง่มุมต่างๆ เช่น การจดจำภาพ (image recognition), การตรวจจับวัตถุ (object detection), การสร้างภาพ (image generation), ความละเอียดสูงสุดของภาพ (image super-resolution) และอื่นๆ <br>การตรวจจับวัตถุน่าจะเป็นแง่มุมที่ลึกซึ้งที่สุดของการมองเห็นด้วยคอมพิวเตอร์เนื่องจากมีกรณีการใช้งานจริงจำนวนมาก 
</p><br><br><br>

 <p align="center">
  <img src="File/Image/Semantic Segmentation Computer Vision.gif" width="800"><br>
 <p>

### #Semantic Segmentation
&emsp;Semantic Segmentation หมายถึงงานการแยกวัตถุในสภาพแวดล้อมการมองเห็นที่ซับซ้อนและเป็นพื้นที่สำคัญของการวิจัยการ มองเห็นด้วยคอมพิวเตอร์
 - เป็นการประมวลผลภาพที่เกี่ยวข้องกับการตรวจจับ ที่อยู่ใกล้กันเป็น **Object** เดียวกัน
<p>
&emsp;ทุกวันนี้ Semantic Segmentation เป็นหนึ่งในปัญหาสำคัญในด้านการมองเห็นด้วยคอมพิวเตอร์ เมื่อพิจารณาในภาพรวมแล้ว Semantic Segmentation เป็นงานระดับสูงที่ปูทางไปสู่ความเข้าใจ ความสำคัญของการเข้าใจในฐานะที่เป็นปัญหาหลักในการมองเห็นด้วยคอมพิวเตอร์นั้นถูกเน้นโดยข้อเท็จจริงที่ว่า <br>
&emsp;แอพพลิเคชั่นจำนวนมากขึ้นพัฒนาจากการวิเคราะห์ความรู้จากภาพ แอพพลิเคชั่นบางตัวรวมถึง Leaning Mechine การโต้ตอบระหว่างมนุษย์กับคอมพิวเตอร์ ความเป็นเสมือนจริง เป็นต้น <br><br>
&emsp;ด้วยความนิยมของการ Deep Leaning ในช่วงไม่กี่ปีที่ผ่านมา Semantic Segmentation ปัญหาจำนวนมากกำลังถูกแก้ไข โดยใช้สถาปัตยกรรมเชิงลึก ซึ่งส่วนใหญ่มักจะเป็น Convolutional Neural NetWorks ซึ่งเหนือกว่าแนวทางอื่นๆ ด้วยอัตราของความแม่นยำและประสิทธิภาพขั้นต้นที่มากขึ้น
</p><br><br><br>
 
 <p align="center">
  <img src="File/Image/Instance Segmentation.gif" width="800"><br>
 <p>
 
### #Instance Segmentation
&emsp;Instance Segmentation เป็นรูปแบบพิเศษของการแบ่งส่วนรูปภาพที่เกี่ยวข้องกับการตรวจจับอินสแตนซ์ของออบเจ็กต์และกำหนดเขตแดนของวัตถุ พบการนำไปใช้ในวงกว้างในสถานการณ์จริง เช่น รถยนต์ที่ขับด้วยตนเองจินตภาพทางการแพทย์การตรวจสอบพืชผลทางอากาศ และอื่นๆ
 - ทำงานคล้ายกับ **Semantic Segmentation** แต่สามารถระบุ **ID** ของ **Object** ในภาพด้วย
&emsp;การแบ่งกลุ่มอินสแตนซ์เป็นเทคนิคการตรวจจับ แบ่งกลุ่ม และจัดประเภทวัตถุแต่ละรายการในรูปภาพ

การแบ่งกลุ่มตัวอย่างดำเนินการกับแมวและสุนัข
เราสามารถอ้างถึง Instance Segmentation เป็นการผสมผสานระหว่างSemantic Segmentationและการตรวจจับอ็อบเจกต์ (การตรวจจับอินสแตนซ์ทั้งหมดของหมวดหมู่ในภาพ) พร้อมคุณสมบัติเพิ่มเติมของการแบ่งเขตอินสแตนซ์ที่แยกจากกันของคลาสเซ็กเมนต์เฉพาะใดๆ ที่เพิ่มในงานเซ็กเมนต์วานิลลา

การแบ่งกลุ่มอินสแตนซ์สร้างรูปแบบเอาต์พุตที่สมบูรณ์ยิ่งขึ้นเมื่อเปรียบเทียบกับทั้งเครือข่ายการตรวจจับวัตถุและการแบ่งส่วนความหมาย 

ในขณะที่ระบบตรวจจับอ็อบเจ็กต์จะโลคัลไลซ์ออบเจ็กต์หลายตัวอย่างหยาบด้วยbounding boxและเฟรมเวิร์กการแบ่งส่วนเชิงความหมายจะสร้างป้ายกำกับหมวดหมู่ระดับพิกเซลสำหรับแต่ละคลาสหมวดหมู่ การแบ่งกลุ่มอินสแตนซ์จะสร้างแมปเซ็กเมนต์ของแต่ละหมวดหมู่รวมถึงอินสแตนซ์แต่ละคลาสของคลาสเฉพาะ—ด้วยเหตุนี้ การอนุมานที่มีความหมายมากขึ้นบนรูปภาพ
  
<p align="center">
 <img src="File/Image/Segmentation.png">
<p><br>
   
<h1 align="center">Real-Time Object Detection</h1>
<p align="center">
 <img align="center" src="File/Image/Real-Time Detection hm.gif" width="500"><br>
 <img align="center" src="File/Image/CalculationMeme.gif" width="500">
<p><br>

#
![Image](File/Image/Thank.png)

# Note

Full Content File PDF : [AI for Image Task](File/PDF/AI%20for%20image%20task.pdf)

References <br>
Object Detection : https://medium.com/towards-data-science/object-detection-with-10-lines-of-code-d6cb4d86f606 <br>
Semantic Segmentation : https://medium.com/nanonets/how-to-do-image-segmentation-using-deep-learning-c673cc5862ef <br>
Semantic Segmentation & Instance Segmentation : https://www.v7labs.com/blog/instance-segmentation-guide
