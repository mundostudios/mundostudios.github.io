# Dixon Project - pdfGen Cheatsheet

## Set-up

### Installing the Python Package Manager
```
curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
```

```
python get-pip.py
```

### Installing FPDF

```
pip install fpdf2
```
## Setting up the file

```python
from fpdf import FPDF

document = FPDF('P', 'mm', 'A4')
document.set_auto_page_break(auto=1, margin = 25)
document.add_page()
```
[Insert your elements here]

```python
document.output("certificate.pdf")
```
## Generating the elements

```python
# Regular p
document.multi_cell(0, 5, f'Text {var}')

# p (Small line spacing) 
document.multi_cell(0, 3, f'Text {var}')

# H2
document.set_font('helvetica', 'B', 11)
document.cell(0, 5, f'Heading {var}')
document.set_font('helvetica', '', 11)

# Line Seperater
document.ln()

# Tab
'          '
```
## Outputting the PDF

```
python gen.py
```

