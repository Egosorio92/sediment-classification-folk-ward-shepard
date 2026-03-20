# Ternary Diagrams for Sediment Classification (Folk & Shepard)

## 📌 Description

This project implements the graphical construction and data visualization of two widely used sediment classification diagrams:

* **Folk Diagram (Gravel–Sand–Mud)**
* **Shepard Diagram (Sand–Silt–Clay)**

Both diagrams are generated using Python and allow plotting real sample data loaded from Excel files.

---

## ⚙️ Requirements

Make sure you have the following installed:

```bash
pip install matplotlib pandas numpy openpyxl
```

---

## 📂 Input Data

The code expects an Excel file with the following structure:

### For Shepard Diagram:

| Sample | Sand | Silt | Clay |
| ------ | ---- | ---- | ---- |
| M1     | 60   | 30   | 10   |

### For Folk Diagram:

| Sample | Gravel | Sand | Mud |
| ------ | ------ | ---- | --- |

Values can be percentages or raw values (they are normalized automatically).

---

## 🚀 How to Run

1. Update the Excel file path:

```python
ruta_excel = "your/path/to/file.xlsx"
```

2. Run the script:

```bash
python your_script.py
```

---

## 📊 Features

* ✔ Automatic normalization of ternary data
* ✔ Custom ternary-to-Cartesian transformation
* ✔ Plotting of classification boundaries
* ✔ Support for sample labeling
* ✔ Manual fine-tuning of label positions (publication-ready figures)

---

## 🧠 Technical Notes

* The ternary transformation is based on barycentric coordinates:

```math
x = 0.5(2 \cdot Silt + Sand)
```

```math
y = \frac{\sqrt{3}}{2} \cdot Sand
```

* Horizontal alignment in the diagram is controlled by the **Sand fraction**.

---

## 📁 Project Structure

```
├── folk_diagram.py
├── shepard_diagram.py
├── data/
│   └── samples.xlsx
└── README.md
```

---

## 📌 Author

Edward Osorio
Geologist MSc. | Data Analysis | Sedimentology

---

## 📜 License

This project is for academic and research purposes.
