```python
from flask import Flask,render_template
app = Flask(__name__)

dic_res={}

"""
files struction show:
static folder
    images folder
        predic.jpg
templates folder
    show_image2.html
show_image2.py
"""

@app.route('/predict')
def new_file():
    # have to get dic_res1 using predict.py in yolov4 project
    dic_res1={1:1,17:1,18:1,33:1}
    dic_res=dic_res1
    return render_template('show_image2.html',dic_res=dic_res)

if __name__=='__main__':
    app.run(host='0.0.0.0',debug=True)
```
