# 🏠 การวิเคราะห์รายได้เฉลี่ยครัวเรือนไทย
### Mini-Hackathon: From Data to Insight — THackle x BDI

> วิเคราะห์เชิงสำรวจข้อมูลรายได้เฉลี่ยครัวเรือนในประเทศไทย (ปี 2566)  
> เพื่อศึกษาความเหลื่อมล้ำทางรายได้ระหว่างกลุ่มอาชีพและจังหวัดต่างๆ

---

# 🏠 Thai Household Income Analysis
### Mini-Hackathon: From Data to Insight — THackle x BDI

> Exploratory data analysis of average household income in Thailand (2566 / 2023),  
> examining income inequality across occupation groups and provinces.

---

## 📁 โครงสร้างโปรเจกต์ | Project Structure

```
├── avg_income.csv              # ข้อมูลดิบจากสำนักงานสถิติแห่งชาติ | Raw dataset from National Statistical Office
├── minihackatron2.ipynb        # Notebook หลักสำหรับการวิเคราะห์ | Main analysis notebook
└── README.md
```

---

## 🔧 การติดตั้งและการใช้งาน | Installation & Setup

**รันบน Google Colab (แนะนำ) | Run on Google Colab (recommended)**

อัปโหลดไฟล์ `avg_income.csv` และ `minihackatron.ipynb` ขึ้น Colab  
Upload `avg_income.csv` and `minihackatron2.ipynb` to Colab



```python
!apt-get install -y fonts-tlwg-sarabun
import matplotlib.font_manager as fm
fm._load_fontmanager(try_read_cache=False)
import matplotlib.pyplot as plt
plt.rcParams['font.family'] = 'Sarabun'
```

3. กด Runtime → Restart and run all  
   Click Runtime → Restart and run all

**รันบนเครื่องตัวเอง | Run locally**

```bash
pip install pandas numpy matplotlib seaborn
jupyter notebook minihackatron2.ipynb
```

---

## 📊 ภาพรวมการวิเคราะห์ | Analysis Overview

Notebook แบ่งออกเป็น 3 ขั้นตอน | The notebook follows 3 steps:

| ขั้นตอน | Step | รายละเอียด | Description |
|---------|------|------------|-------------|
| **การเตรียมข้อมูล** | **Data Preparation** | โหลด ทำความสะอาด แก้ไข null/duplicate และประเภทข้อมูล | Load, clean nulls/duplicates, fix data types |
| **EDA** | **EDA** | สำรวจการกระจายตัว KPI และโครงสร้างกลุ่มอาชีพ | Explore distributions, KPIs, occupation breakdown |
| **Insight Discovery** | **Insight Discovery** | ตอบ 3 คำถามหลักจากชุดข้อมูล | Answer 3 key questions from the dataset |

---

## 💡 Insight สำคัญ | Key Insights

**ข้อ 1 — ใครได้รับค่าตอบแทนแค่ไหน?**  
ผู้จัดการและนักวิชาชีพมีรายได้สูงกว่าแรงงานเกษตรถึง ~3 เท่า (48,293 vs 14,983 บาท/เดือน)  
นโยบาย Upskilling และการยกระดับค่าแรงขั้นต่ำเป็นมาตรการที่ตรงจุดที่สุด

**Q1 — Who earns what?**  
Managers and professionals earn ~3x more than agricultural workers (48,293 vs 14,983 THB/month).  
Upskilling programs and minimum wage policies for low-income groups are the most targeted intervention.

---

**ข้อ 2 — ความเหลื่อมล้ำอยู่ที่ไหน?**  
จันทบุรีมีช่องว่างรายได้กว้างที่สุด จังหวัดภาคอีสาน (ยโสธร ศรีสะเกษ) มีทั้งรายได้ต่ำและความเหลื่อมล้ำภายในสูง ต้องการนโยบายที่แตกต่างจากจังหวัดรายได้สูง

**Q2 — Where is inequality?**  
Chanthaburi has the widest income gap. Northeastern provinces (Yasothon, Sisaket) have both low average income and high internal inequality — requiring different policy responses than high-income provinces.

---

**ข้อ 3 — โครงสร้างรายได้เป็นอย่างไร?**  
กลุ่มที่พึ่งพารายได้แหล่งเดียว (>70%) มีความเปราะบางทางเศรษฐกิจสูง เกษตรกรพึ่งพากำไรเกษตร ส่วนผู้ไม่ได้ปฏิบัติงานพึ่งพาเงินโอนจากรัฐเป็นหลัก

**Q3 — What is the income structure?**  
Groups relying on a single income source (>70%) are economically vulnerable. Farmers depend on agricultural profit; the economically inactive depend heavily on government transfers.

---

## 🗂️ ชุดข้อมูล | Dataset

| | |
|---|---|
| **แหล่งที่มา / Source** | สำนักงานสถิติแห่งชาติ (National Statistical Office of Thailand) |
| **ดาวน์โหลดได้ที่ / Available at** | [THackle Dataset #92](https://www.thackle.or.th/th/dataset/92) |
| **ปี / Year** | 2566 (2023) |
| **จำนวนแถว / Rows** | 7,700 |
| **จำนวนคอลัมน์ / Columns** | 11 |
| **คอลัมน์หลัก / Key columns** | `province`, `soc_eco_class1`, `soc_eco_class2`, `source_income1/2/3`, `value` |

---

## 🏆 การแข่งขัน | Competition

โปรเจกต์นี้ส่งเข้าร่วม **Mini-Hackathon: From Data to Insight**  
จัดโดย [THackle](https://www.thackle.or.th) × Big Data Institute (BDI)

This project was submitted to the **Mini-Hackathon: From Data to Insight**  
organized by [THackle](https://www.thackle.or.th) × Big Data Institute (BDI)
