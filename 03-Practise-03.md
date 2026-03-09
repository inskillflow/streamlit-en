# Step-by-Step Tutorial for Learning Widgets with Streamlit

This tutorial will guide you in creating a Streamlit application using different widgets such as buttons, checkboxes, radio buttons, dropdown lists, sliders, text fields, and file uploads.

#### Prerequisites

* Python installed on your machine.
* `virtualenv` installed (`pip install virtualenv`).

### Step 1: Creating the Virtual Environment

1. Open your terminal and navigate to the folder where you want to create your project.
2. Create a virtual environment:

```bash
python -m venv myenv
```

3. Activate the virtual environment:

   * On Windows:

   ```bash
   myenv\Scripts\activate
   ```

   * On macOS/Linux:

   ```bash
   source myenv/bin/activate
   ```

### Step 2: Installing Streamlit

1. With the virtual environment activated, install Streamlit:

```bash
pip install streamlit
```

### Step 3: Creating the Main File

1. Create a Python file, for example `widgets_app.py`, in your project folder.

### Step 4: Using Widgets

**Button**

1. Open `widgets_app.py` and write the following code to display a button:

```python
import streamlit as st

st.title('Input Widgets')

# Button
st.header('Button')
button = st.button('Button')  # return True or False
if button:
    st.write('You pressed the Button')
```

2. To test, open your terminal (with the virtual environment activated) and run:

```bash
streamlit run widgets_app.py
```

**Checkbox**

1. Add a checkbox with conditional text:

```python
# Checkbox (Toggle Button)
st.header('Checkbox')
checkbox = st.checkbox("Do you want to agree?")  # return bool (True or False)
if checkbox:
    st.write('You checked the box')
else:
    st.write('You unchecked the box')
```

2. Save and test.

**Radio Button**

1. Add radio buttons to select one option from several:

```python
st.header('Radio Button')
options = ("India", "USA", "UK", "Australia")
radio_button = st.radio("What is your favorite country", options, index=2)  # return an element in a list/tuple
st.write('Your favorite country is', radio_button)
```

2. Save and test.

**Dropdown List**

1. Add a dropdown list to select an option:

```python
# Select Box
st.header('Select Box')
options = ('Email', 'Phone', 'WhatsApp')
select_box = st.selectbox('How would you like to contact', options, index=1)
st.write('Your preferred mode of communication is', select_box)
```

2. Save and test.

**Slider**

1. Add a slider to select a numeric value:

```python
# Slider
st.header('Slider')
slider_range = st.slider('How old are you?', min_value=1, max_value=100, step=1, value=20)
st.write('Your age is', slider_range)
```

2. Save and test.

**Text Fields**

1. Add text fields to enter text and numbers:

```python
# Text Inputs
st.header('Text Inputs')
name = st.text_input('Enter your Name')
st.write('Your name is', name)

age = st.number_input('Enter your age', min_value=1, max_value=100, step=1, value=25)
st.write('Your age is', age)
```

2. Save and test.

**File Upload**

1. Add a file upload feature:

```python
# Upload File
st.header('File Upload')
uploaded_file = st.file_uploader('Choose a File')

if uploaded_file is not None:
    st.success('File uploaded successfully')
    details = {'filename': uploaded_file.name, 'filetype': uploaded_file.type, 'filesize (bytes)': uploaded_file.size}
    st.json(details)
    
    # save the file
    path = os.path.join('./upload', uploaded_file.name)
    with open(path, mode='wb') as f:
        f.write(uploaded_file.getbuffer())
        st.success('File saved successfully')
```

2. Make sure the `upload` folder exists in your project.
3. Save and test.

### Complete Code

Here is the complete code for the `widgets_app.py` file:

```python
import streamlit as st
import os

st.title('Input Widgets')

# Button
st.header('Button')
button = st.button('Button')  # return True or False
if button:
    st.write('You pressed the Button')

# Checkbox (Toggle Button)
st.header('Checkbox')
checkbox = st.checkbox("Do you want to agree?")  # return bool (True or False)
if checkbox:
    st.write('You checked the box')
else:
    st.write('You unchecked the box')

st.header('Radio Button')
# Radio Button
options = ("India", "USA", "UK", "Australia")
radio_button = st.radio("What is your favorite country", options, index=2)  # return an element in a list/tuple
st.write('Your favorite country is', radio_button)

# Select Box
st.header('Select Box')
options = ('Email', 'Phone', 'WhatsApp')
select_box = st.selectbox('How would you like to contact', options, index=1)
st.write('Your preferred mode of communication is', select_box)

# Slider
st.header('Slider')
slider_range = st.slider('How old are you?', min_value=1, max_value=100, step=1, value=20)
st.write('Your age is', slider_range)

# Text Inputs
st.header('Text Inputs')
name = st.text_input('Enter your Name')
st.write('Your name is', name)

age = st.number_input('Enter your age', min_value=1, max_value=100, step=1, value=25)
st.write('Your age is', age)

# Upload File
st.header('File Upload')
uploaded_file = st.file_uploader('Choose a File')

if uploaded_file is not None:
    st.success('File uploaded successfully')
    details = {'filename': uploaded_file.name, 'filetype': uploaded_file.type, 'filesize (bytes)': uploaded_file.size}
    st.json(details)
    
    # save the file
    path = os.path.join('./upload', uploaded_file.name)
    with open(path, mode='wb') as f:
        f.write(uploaded_file.getbuffer())
        st.success('File saved successfully')
```

### Formative Assessment

#### Instructions

1. Create a new virtual environment and activate it.
2. Install Streamlit in this environment.
3. Create a file `widgets_app.py` and implement the following features one by one, testing at each step:

   * Display a button and respond to its click.
   * Add a checkbox and respond to its state.
   * Add radio buttons to select an option.
   * Add a dropdown list to select an option.
   * Add a slider to select a numeric value.
   * Add text fields to enter text and numbers.
   * Add a file upload feature.
4. Submit the final `widgets_app.py` file and a screenshot of each tested step.

#### Exercise

1. **Button**

   * Display a button and write a message when it is clicked.

2. **Checkbox**

   * Add a checkbox and display a message based on its state (checked/unchecked).

3. **Radio Button**

   * Add radio buttons to select a favorite country from several options and display the choice.

4. **Dropdown List**

   * Add a dropdown list to select a preferred communication method and display the choice.

5. **Slider**

   * Add a slider to select an age value and display this value.

6. **Text Fields**

   * Add text fields to enter a name and an age, then display the entered values.

7. **File Upload**

   * Add a file upload feature and display the details of the uploaded file.

### Example Solution

```python
import streamlit as st
import os

st.title('Input Widgets')

# Button
st.header('Button')
button = st.button('Button')
if button:
    st.write('You pressed the Button')

# Checkbox (Toggle Button)
st.header('Checkbox')
checkbox = st.checkbox("Do you want to agree?")
if checkbox:
    st.write('You checked the box')
else:
    st.write('You unchecked the box')

st.header('Radio Button')
options = ("India", "USA", "UK", "Australia")
radio_button = st.radio("What is your favorite country", options, index=2)
st.write('Your favorite country is', radio_button)

# Select Box
st.header('Select Box')
options = ('Email', 'Phone', 'WhatsApp')
select_box = st.selectbox('How would you like to contact', options, index=1)
st.write('Your preferred mode of communication is', select_box)

# Slider
st.header('Slider')
slider_range = st.slider('How old are you?', min_value=1, max_value=100, step=1, value=20)
st.write('Your age is', slider_range)

# Text Inputs
st.header('Text Inputs')
name = st.text_input('Enter your Name')
st.write('Your name is', name)

age = st.number_input('Enter your age', min_value=1, max_value=100, step=1, value=25)
st.write('Your age is', age)

# Upload File
st.header('File Upload')
uploaded_file = st.file_uploader('Choose a File')

if uploaded_file is not None:
    st.success('File uploaded successfully')
    details = {'filename': uploaded_file.name, 'filetype': uploaded_file.type, 'filesize (bytes)': uploaded_file.size}
    st.json(details)
    
    # save the file
    path = os.path.join('./upload', uploaded_file.name)
    with open(path, mode='wb') as f:
        f.write(uploaded_file.getbuffer())
        st.success('File saved successfully')
```
