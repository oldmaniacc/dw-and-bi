# Data Warehouse and Business Intelligence
# Project: Building a Data Modeling with Postgres (SQL)

# มีโค้ดที่ทำ ETL จากข้อมูล JSON โหลดเข้าไปใน Postgres
## มีโค้ด
#
# มีการเขียน Documentation อธิบายสิ่งที่ตัวเองทำลงไป รวมไปถึงการออกแบบ Data Model
## 1.Running Postgres ด้วยคำสั่ง docker-compose up กับไฟล์ docker-compose.yml (ตรวจเช็คด้วยการเข้า port 8080)
## 2.ทำการติดตั้ง psycopg2 ด้วยคำสั่ง pip install psycopg2
## 3.อัพโหลดและรันไฟล์สคริปต์ create_tables.py และ etl.py ตามลำดับ
## 4.ในไฟล์สคริปต์ create_tables.py ทำการเพิ่ม table repos โดยมี column (id,name,event_id) เท่ากับจะมี 3 tables ได้แก่ actors, events, repos
## 5.ทำการเชื่อมความสัมพันธ์ของ 3 ตารางเข้าด้วยกัน (ออกแบบ Data Model) โดยการกำหนด Foreign Key โดยในตาราง events จะกำหนด FK คือ actor_id ที่ ref ถึง id จากตาราง actors และในตาราง repos จะกำหนด FK คือ event_id ที่ ref ถึง id จากตาราง events
## 6.เรียงลำดับ create และ drop ตารางให้ถูกต้อง โดย create จะเริ่มจาก actors, events, repos ส่วน drop จะเริ่มจาก repos,events,actors
## 7.ในไฟล์สคริปต์ etl.py ทำการเพิ่มข้อมูลให้กับตาราง repos ด้วยคำสั่ง insert into repos และกำหนด value ให้ตรงกับคอลัม
## 8.แก้ path ที่เก็บไฟล์ json ให้ถูกต้อง ในสคริปต์ etl.py 
## 9.เช็ค port 8080 ว่ามีข้อมูลโหลดเข้ามาในตารางหรือไม่
#
# มี Instruction ในการรันโค้ดของตัวเอง
## 1. docker-compose up with docker-compose.yml 
## 2. install psycopg2
## 3. python 
## 4. upload create_tables.py and etl.py
## 5. upload 5 json files
## 6. run script create_tables.py and etl.py