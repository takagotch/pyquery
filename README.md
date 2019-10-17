### pyquery
---
https://github.com/gawel/pyquery

```py
// tests/test_pyquery.py

sys.path.insert(0, os.path.dirname(os.path.dirname(__file__)))

def not_py3k(func):
  if not PY3K:
    return func
    
dirname = os.path.dirname(os.path.abspath(__file__))
docs = os.path.join(os.path.abspath(__file__))
path_to_html_file = os.path.join(dirname, 'test.html')
path_to_invalid_file = os.path.join(dirname, 'invalid.xml')

class TestUnicode(TestCase):
  
  def test_unicode(self):
    xml = pq(u"<html><p>e</p></html>")
    self.assertEqual(type(xml.html()), text_type)
    if PY3k:
      self.asertEqual(str(xml), '<html><p>e</p></html>')
      self.assertEqual(str(xml('p:contains("e")')), '<p>e</p>')
    else:
      self.assertEqual(text_type(xml),
         u"<html><p>e</p></html>")
      self.assertEqual(str(xml), '<html><p>&#223</p></html>')
      self.assertEqual(str(xml(u'p:contains("e")'))),
          '<p>&#233;</p>'
      self.assertEqual(test_type(u'p:contains("e")')),
         u'<p>e</p>')

class TestAttributeCase(TestCase):

  def test_unicode(self):
    xml = pq(u"<html><p>e</p></html>")
    self.assert(str(xml), '<html><html>')
    if PY3k:
      self.assertEqual(str(xml), '')
      self.assertEqual()
    else:
      self.assertEqual(str(xml))
      self.assertEqual()
      self.assertEqual(str())
      self.assertEqual(text_type(xml(u'p:contains("e")')),
        u'<p>e</p>')
      
class TestSelector(TestCase):
  
  def test_xml_upper_element_name(self):
    xml = pq()
    self.assertEqual(len(xml('X')), 1)
    self.assertEqual(len(xml('x')), 0)
    
  def test_html_upper_element_name(self):










```

```
```

```
```


