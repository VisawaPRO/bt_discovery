# Example นี้มีชื่อว่า bt_discovery
โดยการทำงานของ Example นี้คือการค้นหาอุปกรณ์ที่รองรับ Classic Bluetooth แล้วเก็บชื่อ Bluetooth และเก็บบริการต่างๆที่อุปกรณ์สามารถรองรับได้
#
ขั้นตอนแรกเลือก Example
# ![image](https://github.com/user-attachments/assets/51541788-b6c3-4efc-8814-fb5207587706)
รันและbuildโปรแกรม
# ![image](https://github.com/user-attachments/assets/6f330627-c8e4-4938-920a-79dfb118a47a)
เปิด Bluetooth ในมือถือแล้วกด reset ที่บอร์ดเพื่อให้บอร์ดค้นหาอุปกรณ์ใหม่
# ![image](https://github.com/user-attachments/assets/4d7a03c1-7950-46a1-9c6f-da295a321c7d)
# แก้ไขเพิ่มเติม
จาก code จะสแกนหาได้เพียงมือถือและ Audio/Video
# ![image](https://github.com/user-attachments/assets/e205ce98-8b73-44eb-a8a8-a50bc268ae2f)
สามารถเพิ่มการสแกนอุปกรณืต่างๆได้ เช่น Computer โดยที่ Computer นั้นต้องมี Bluetooth โดยการเพิ่ม
```
if (!esp_bt_gap_is_valid_cod(cod) ||
	    (!(esp_bt_gap_get_cod_major_dev(cod) == ESP_BT_COD_MAJOR_DEV_PHONE) &&
             !(esp_bt_gap_get_cod_major_dev(cod) == ESP_BT_COD_MAJOR_DEV_AV) &&
                !(esp_bt_gap_get_cod_major_dev(cod) == ESP_BT_COD_MAJOR_DEV_COMPUTER))) {
        return;
    }
```
ผลลัพธ์เมื่อต่อเข้ากับ Computer
# ![image](https://github.com/user-attachments/assets/d095f2a6-da33-4cc3-8552-e6a242d53473)
# ![image](https://github.com/user-attachments/assets/2c5cdfca-6c58-42b9-bb50-edcf0f7ed77b)
 

