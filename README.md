1.อาจกล่าวได้ว่า Agile Method ไม่มีอะไรที่เหมือนกับ Waterfall Model เลย แต่ Waterfall Modelก็ยังเป็นวิธีการพัฒนาระบบที่ใช้กันอยู่ค่อนข้างแพร่หลาย ซึ่งวิธีนี้จะมีลำดับขั้นตอนที่ตายตัว เริ่มตั้งแต่รวบรวมข้อมูล กำหนดความต้องการของผู้ใช้ วิเคราะห์ทางเลือก ออกแบบ เขียนโปรแกรม ทดสอบระบบ และสุดท้ายทำการติดตั้งระบบ โดยแต่ละส่วนของขั้นตอนดังกล่าวจะถือเป็นตัววัดความก้าวหน้าของงาน ปัญหาสำคัญของ Waterfall Model คือขั้นตอนของการพัฒนาที่ไม่ยืดหยุ่น เพราะตัวงานจะแบ่งเป็นช่วงๆแบบตายตัว ทำให้มีข้อผูกมัดตั้งแต่เริ่มโครงงานและไม่สามารปรับเปลี่ยนความต้องการผู้ ใช้ได้ หมายความว่าการพัฒนาโดยใช้ Waterfall Model นั้น ไม่เหมาะกับงานที่ความต้องการของผู้ใช้เข้าใจยาก และมีแนวโน้มว่าจะเปลี่ยนแปลงตลอดเวลา


2. github เป็น web ที่ให้บริการจัดเก็บ source code (version control) ที่ใช้ version control system ที่ชื่อ git นอกจากนั้นก็มีพวกเสริม เช่น issue tracking 
 	ส่วน svn, cvs เป็น version control system ถ้าเทียบ git กับ svn, cvs ตัว git เป็น distributed แต่ svn, cvs เป็น centralize
git เราสามารถ clone repository (ที่เก็บ source code) มาไว้ที่เครื่องเรา แล้ว commit งานในเครื่องได้ แล้วค่อย sync กับตัวที่เรา clone มา
แต่ svn, cvs ต้องมี repository กลางที่เราจะ commit source code ที่เราแก้ไขเข้าไป (repository กลางนี้ อาจจะเป็น server อื่น หรือ set เป็น local file ในเครื่องก็ได้)

3. 	$ git add feature1
$ git commit -m 'Add feature1'
$ git push
$ git branch –a

4. ปัญหาใหญ่ ๆ ของ Merge conflict เกิดจากจำนวน source code ที่ชนหรือขัดแย้งกันมากเหลือเกิน
สิ่งที่หนึ่งที่บอกได้เลยก็คือ
ยิ่งใช้เวลานานเพียงใด ความเสี่ยงก็ยิ่งมากขึ้นเท่านั้น
ยิ่งก็ให้เกิดข้อขัดแย้งขนาดใหญ่ และ มากมาย
ดังนั้น ถ้าคุณต้องการหลีกเลี่ยงปัญหาเหล่านี้
ให้ทำการ merge บ่อย ๆ ไปเลย
นั่นคือ ทุกครั้งเมื่อคุณทำการเปลี่ยนแปลง หรือ commit source code นั่นเอง
จะช่วยลดข้อขัดแย้งต่าง ๆ ลงไปอย่างมาก
ถึงจะเกิดข้อขัดแย้ง ก็เป็นเพียงปัญหาเล็ก ๆ
ซึ่งสามารถแก้ไขได้อย่างง่ายดาย

5. abcde"a".."e"

6. การออกแบบ Web Application ที่เห็นได้ชัดก็คือ   โค้ดโปรแกรมทั้งหมดอยู่ที่ฝั่งเซอร์เวอร์   และมีโค้ดโปรแกรมบางส่วนจะถูกโหลดขึ้นบนไคลเอนต์เมื่อต้องการจะทำงาน   ส่วนโค้ดที่เหลือจะยังคงค้างอยู่ที่ฝั่งเซอร์เวอร์  ทำให้การพัฒนาซอฟต์แวร์ที่ต้องมีการปรับปรุงแก้ไขบ่อย  สามารถกระทำได้โดยง่ายโดยไม่ต้องทำระบบโหลด patch หรืออัปเดตเวอร์ชันใหม่ๆ ให้กับไคลเอนต์จำนวนมากบ่อยๆ   และโปรแกรมบางประเภทที่ต้องใช้ข้อมูลส่วนกลางเป็นจำนวนมากแต่จะไม่ได้ใช้ทั้งหมดในคราวเดียว   ผู้พัฒนาโปรแกรมสามารถที่จะส่งข้อมูลเบื้องต้นบางส่วนให้กับไคลเอนต์ไปก่อน  และเมื่อผู้ใช้ต้องการข้อมูลส่วนอื่นๆ เพิ่มเติม  จึงค่อยส่งข้อมูลที่เหลือให้   การทำเช่นนี้จะทำให้ไม่ต้องส่งข้อมูลทั้งหมดไปยังผู้ใช้ในคราวเดียว  โดยเฉพาะในกรณีที่ผู้ใช้งานอาจจะไม่ต้องการข้อมูลทั้งหมดนั้น การเลือกส่งเท่าที่ร้องขอจะช่วยลดปริมาณข้อมูลที่ต้องส่งผ่านระบบเครือข่ายลงได้
	Web Application  ไม่เหมาะสมสำหรับโปรแกรมที่ออกแบบมาเพื่อใช้งานกับข้อมูลส่วนบุคคลที่ไม่จำเป็นต้องแบ่งปันให้กับผู้อื่น    รวมถึงข้อมูลที่อาจจะมีความลับสูง (ถ้าต้องส่งผ่านอินเทอร์เน็ต ที่แม้จะเข้ารหัสไว้แล้ว  แต่อาจจะถูกเจาะและถอดรหัสนำข้อมูลออกมาไปใช้ได้)   เป็นต้น
  
7. MVC นั้นย่อมาจาก Model View Controller ซึ่งเป็นส่วนประกอบของ Web Framework ในปัจจุบัน เช่น Ruby On Rails, Yii2 PHP Framework โดยแต่ละส่วนนั้นมีหน้าที่หลักๆ ดังนี้


1.)	Model มีหน้าที่หลักในการจัดการเกี่ยวกับฐานข้อมูล โดยจะมี ORM (Object Relational Mapping) เข้ามาช่วยในการทำงาน โดย ORM จะช่วยแปลง ฐานข้อมูล เป็น Object และแปลง Object เป็น ฐานข้อมูล โดยที่เราไม่จำเป็นต้องเขียน SQL เพราะตัว ORM จะช่วยแปลงการเรียกใช้งาน Method ของ Object ไปเป็น SQL เอง
2.)	View คือส่วนในการแสดงผลหน้าเว็บ โดยส่วนใหญ่จะเป็นโค้ดภาษา HTML และ CSS
3.)	Controller จะเป็นตัวจัดการความต้องการของ User เช่น ถ้า User ต้องการดูหน้าเว็บ ตัว Controller จะไปเรียก View มาเพื่อแสดงผลตามที่ User ต้องการ หรือถ้า User ต้องการดูข้อมูล, แก้ไขข้อมูล, หรือลบข้อมูลในฐานข้อมูล ตัว Controller ก็จะไปเรียกใช้งาน Method ต่างๆ ใน Model เพื่อจัดการกับฐานข้อมูลตามความต้องการของ User โดยสรุปแล้ว Controller จะเป็นส่วนที่เชื่อมต่อให้ View และ Model ทำงานร่วมกัน
หลักการเบื้องต้นของ MVC ก็มีเพียงเท่านี้

8. Ruby on Rails
ข้อดี
1.)ไม่ต้องเสียเวลาพัฒนาเครื่องมือเพื่อใช้เอง จึงสามารถใช้เวลาไปกับการสร้างซอฟต์แวร์ตาม ข้อกำหนดได้มากขึ้น
2.)ส่งเสริมให้วิศวกรซอฟต์แวร์มีระเบียบวินัยที่ชัดเจน เป็นมาตรฐานเดียวกัน
3.)	มีระบบการทดสอบด้วยซอฟต์แวร์ ทำให้การทดสอบครบถ้วนสม่ำเสมอ
4.)	Ruby on Rails เป็นซอฟต์แวร์ open source ทำให้สามารถตรวจสอบซอร์สโค้ดได้ครบ ถ้วน ช่วยให้การแก้ปัญหาเป็นไปได้ง่ายขึ้น
5.)	ข้อดีอีกข้อของ open source software คือการมีเครือข่ายวิศวกรซอฟต์แวร์ทั่วโลก ช่วยกันประดิษฐ์เครื่องมือเพื่อการใช้งานจำเพาะต่างๆ และแบ่งปันให้เพื่อนวิศวกรซอฟต์แวร์ ได้นำไปใช้และพัฒนาต่อยอดยิ่งๆ ขึ้นไป
ข้อเสีย
1.)	การติดตั้ง Ruby on Rails บนเครื่อง development ยุ่งยากกว่าเครื่องมืออื่นๆ เช่น PHP, Java หรือ .NET
2.)	การ Deploy Rails application ขึ้นเซิร์ฟเวอร์จริง ก็ยิ่งยุ่งยากมากกว่าการติดตั้งบนเครื่อง development
3.)	ความเร็วในการทำงานของภาษา Ruby จัดได้ว่าช้ากว่าคู่แข่งอยู่มาก มีความพยายาม แก้ปัญหานี้จากหลายๆ ฝ่าย เช่น JRuby เป็นการใช้ Java Virtual Machine มารันโปรแกรมที่เขียนขึ้นด้วยภาษา Ruby อาศัยการทำงานของ Java Hotspot Compiler ในการช่วยเพิ่มความเร็วในการทำงาน
4.)	ทั้ง Ruby และ Ruby on Rails มีทัศนคติที่ไม่ดีกับ Microsoft Windows การส่งเสริมการ ทำงานบน Windows จึงมีไม่มากนัก ทำให้การพัฒนา Ruby on Rails ต้องทำบน Linux หรือ Apple Mac OS เป็นหลักและ Deploy ขึ้น Linux Server เป็นหลัก
5.)	Ruby on Rails ได้รับความนิยมมากในต่างประเทศ แต่ในประเทศไทยเพิ่งเริ่มมีความนิยมในระยะเวลา 1-2 ปีมานี้ ทำให้ตำรับตำราต่างๆ เป็นภาษาต่างประเทศทั้งหมด

9. Heroku คือผู้ให้บริการ Platform as a Services (PaaS) เช่น แอพพลิเคชันเซิร์ฟเวอร์, ดาต้าเบสเซิร์ฟเวอร์ หรือมิดเดิลแวร์อื่นๆ ไม่ต้องเสียเวลาหา software ไม่ต้องหา server และลดความยุ่งยากในการ configuration เพราะเพียงแค่คลิกเลือกภาษาที่ต้องการสร้าง app ไม่ถึงนาทีเราก็มี environment พร้อมใช้งาน ที่สำคัญฟรี Heroku นั้นจะสร้าง application บน facebook ในรูปแบบ Website ให้อัตโนมัติ (ตัวเว็บอยู่นอกกรอบ facebook แค่ขอดึงใช้งานข้อมูล friend ต่างๆ เฉยๆ) หากเราต้องการให้เป็น application ที่อยู่ในกรอบ facebook (เรียกว่า Canvas app) ให้ copy ข้อความใน Site URL มาใส่ยังช่อง App on Facebook ในส่วน Secure Canvas URL เอาเอง  (ส่วนช่อง Canvas URL ก็ให้กรอกเหมือนกัน แค่เปลี่ยนจาก https เป็น http เท่านั้น) หรือหากต้องการสร้าง application ให้ tab บน page ของคุณก็ไปกรอกที่ช่อง Page Tabแทน

10.เพื่อให้ศึกษาความรู้เบื้องต้นเกี่ยวกับวิศวกรรมซอฟต์แวร์ กระบวนการพัฒนาซอฟต์แวร์ การบริหารโครงการซอฟต์แวร์ กระบวนการวิศวกรรมความต้องการ แบบจำลองระบบ การออกแบบ การสร้างซอฟต์แวร์ การทดสอบ การตรวจสอบความถูกต้อง ตัวชี้วัดซอฟต์แวร์ การประกันคุณภาพซอฟต์แวร์ การจัดการและควบคุมการเปลี่ยนแปลงใน การพัฒนางานด้านซอฟต์แวร์ การบำรุงรักษาซอฟต์แวร์ 

 


