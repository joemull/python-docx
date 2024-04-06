# python-docx

*python-docx* is a Python library for reading, creating, and updating Microsoft Word 2007+ (.docx) files.

## Installation

```
pip install python-docx
```

## Example

```python
>>> from docx import Document

>>> document = Document()
>>> document.add_paragraph("It was a dark and stormy night.")
<docx.text.paragraph.Paragraph object at 0x10f19e760>
>>> document.save("dark-and-stormy.docx")

>>> document = Document("dark-and-stormy.docx")
>>> document.paragraphs[0].text
'It was a dark and stormy night.'
```

More information is available in the [python-docx documentation](https://python-docx.readthedocs.org/en/latest/)

## Development

```
mkvirtualenv python-docx
pip install -r requirements-dev.txt
```

### Documentation

```
workon python-docx
pip install -r requirements-docs.txt
cd docs
make html
firefox .build/html/index.html
```

### Testing

```
workon python-docx
pip install -r requirements-test.txt
pytest
behave
```
