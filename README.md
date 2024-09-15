# AdventureWorks Inventory Analysis [Power BI]

## About

## Dataset
AdventureWorks database supports standard online transaction processing scenarios for a fictitious bicycle manufacturer - Adventure Works Cycles. Scenarios include Manufacturing, Sales, Purchasing, Product Management, Contact Management, and Human Resources.

The warehouse department of a business is responsible for storing goods including finished products, semi-finished products, and raw materials for production.
Warehouses are located in many different locations for convenience and optimization of storage and distribution to customers.
Warehouse managers and warehouse staff need to closely monitor and control the amount of goods in the warehouse, ensuring that goods are stored at prescribed levels.
From there, build appropriate strategies to better manage and operate storage activities.
Sales people and the Marketing team also need to monitor the amount of goods in the warehouse to build, control, and adjust sales and marketing campaigns accordingly.

Requirements:
As a data analyst, you help stakeholders have a complete and easy-to-understand picture of warehouse data, helping them make better decisions and operations.
In addition, you will also provide your ideas, insights, and suggestions to those stakeholders.

Tables used
- a
- b
- c
- d
  
## Explore data
### Data Model
![image](https://github.com/user-attachments/assets/10162b77-ae3b-425a-8014-ea0d65eda0f7)

### Dashboard
#### 1. Overview
![image](https://github.com/user-attachments/assets/a354c8dc-4326-4756-bc78-005e37b6b8f6)

#### 2. Product Information
![image](https://github.com/user-attachments/assets/2a0a761b-2c77-473a-94dd-8ff233b7ee1d)


## Insight
- Tổng các product của công ty là đang tồn kho là 504 sp trong đó (363 sp đạt mức an toàn, 61 sp dưới mức an toàn, 4 sp cần reorder, 76 sp hết hàng)
- Tổng sl hàng hoá là 336k với số lượng các mặt hàng nonsalable (category other) là cao nhất 76.84%, components (14.05%), bikes (4.62%), accessories
(2.72%), clothing (1.77%)
- Inventory value: tổng inventory val là 20m, trong đó Category Bike có số lượng thấp nhưng giá trị cao nhất sp với các category còn lại (14.6m) ,
ngược lại category other có số lượng sp nhiều nhất nhưng giá trị lại tương đối thấp (867k)
- Make status: Category accessories và clothing hoàn toàn là sp mua ngoài, phẩn lớn các nonsalable item cũng là mua ngoài. Công ty chỉ tự sản xuất
category bike, phẩn lớn các component và một số category other
- Location:
  - Location Subassembly, Miscellaneous storage, Tool Crib là 3 khu vực chứa nhiều product nhất (chủ yếu nonsalable item, components và số ít
accessories)
  - Finished Goods Storage chứa bikes, accessories, clothing
  - Bikes còn có ở location Final assembly (khu vực lắp ráp hoàn thiện)
  - Các khu vực còn lại lưu trữ các mặt hàng components và other
- Stock status
  - Đa phần đều là safety
  - Below safety rơi chủ yếu vào category other (25.36%) và accessories (10.34%)
  - Các mặt hàng components out stock nhiều ở category component (53.72%), số ít ở clothing (8.57%)
  - Số lượng reorder rất ít (1sp bikes, 2 sp other, 1 spp components)
- Overstock: Có một số sp có tồn kho rất cao so với mức safety đặt ra (lên đến x8) chủ yếu đến từ các mặt hàng clothing và accessories

## Recommend
- Kiểm tra lại nguyên nhân các mặt hàng overstock (mua dự trữ, hàng lưu chuyển chậm hay do thiết lập safety level quá thấp)
- Theo dõi các alert metric hàng ngày để kịp bổ sung các sp outstock, cần reorder và lưu ý các sản phẩm dưới safety
