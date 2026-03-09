# Step-by-Step Tutorial for Learning Layouts with Streamlit

This tutorial will guide you in creating a Streamlit application using different layouts such as sidebars, columns, and tabs. The goal is to help you configure advanced layouts while testing their code at each step.

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

1. Create a Python file, for example `layout_app.py`, in your project folder.

### Step 4: Configuring the Page

1. Open `layout_app.py` and write the following code to configure the page and display a title:

```python
import streamlit as st

st.set_page_config(page_title="Layouts", layout='wide')
st.title('Streamlit Layout')  # display title format
```

2. To test, open your terminal (with the virtual environment activated) and run:

```bash
streamlit run layout_app.py
```

### Step 5: Adding a Sidebar

1. Add a sidebar with text and a header:

```python
# sidebar
sidebar = st.sidebar
sidebar.write('This is my sidebar')
sidebar.header('Header in sidebar')
```

2. Save and test by running `streamlit run layout_app.py`.

### Step 6: Using Columns

1. Add columns to organize the content:

```python
# columns
col1, col2, col3 = st.columns(3)
with col1:
    st.write('This is column -1')
    st.image('./media/cat.jpg')
    
with col2:
    st.write('This is column -2')
    st.image('./media/dog.jpg')
    
with col3:
    st.write('This is column -3')
    st.image('./media/owl.jpg')
```

2. Make sure you have images `cat.jpg`, `dog.jpg`, and `owl.jpg` in the `media` folder.

3. Save and test.

### Step 7: Adding Tabs

1. Add tabs to organize the content:

```python
# tabs
st.header('Display in Tabs')
tab1, tab2, tab3 = st.tabs(['Cat', 'Dog', 'Owl'])

with tab1:
    st.write('You are in Cat Tab')
    st.image('./media/cat.jpg')
with tab2:
    st.write('You are in Dog Tab')
    st.image('./media/dog.jpg')
with tab3:
    st.write('You are in Owl Tab')
    st.image('./media/owl.jpg')
```

2. Save and test.

### Complete Code

Here is the complete code for the `layout_app.py` file:

```python
import streamlit as st

st.set_page_config(page_title="Layouts", layout='wide')
st.title('Streamlit Layout')  # display title format

# sidebar
sidebar = st.sidebar
sidebar.write('This is my sidebar')
sidebar.header('Header in sidebar')

# columns
col1, col2, col3 = st.columns(3)
with col1:
    st.write('This is column -1')
    st.image('./media/cat.jpg')
    
with col2:
    st.write('This is column -2')
    st.image('./media/dog.jpg')
    
with col3:
    st.write('This is column -3')
    st.image('./media/owl.jpg')
    
# tabs
st.header('Display in Tabs')
tab1, tab2, tab3 = st.tabs(['Cat', 'Dog', 'Owl'])

with tab1:
    st.write('You are in Cat Tab')
    st.image('./media/cat.jpg')
with tab2:
    st.write('You are in Dog Tab')
    st.image('./media/dog.jpg')
with tab3:
    st.write('You are in Owl Tab')
    st.image('./media/owl.jpg')
```

### Formative Assessment

#### Instructions

1. Create a new virtual environment and activate it.
2. Install Streamlit in this environment.
3. Create a file `layout_app.py` and implement the following features one by one, testing at each step:

   * Configure the page and display a title.
   * Add a sidebar with text and a header.
   * Use columns to organize the content.
   * Add tabs to organize the content.
4. Submit the final `layout_app.py` file and a screenshot of each tested step.

#### Exercise

1. **Page Configuration**

   * Configure the page to have a title and a wide layout.
   * Display a title "Streamlit Layout".

2. **Sidebar**

   * Add a sidebar with the text "This is my sidebar".
   * Add a header "Header in sidebar" in the sidebar.

3. **Columns**

   * Create three columns and display an image and text in each column.

4. **Tabs**

   * Add three tabs ("Cat", "Dog", "Owl") and display a corresponding image and text in each tab.

5. **Advanced Features (Optional)**

   * Add buttons in the sidebar to dynamically change the images displayed in the columns.

### Example Solution

```python
import streamlit as st

st.set_page_config(page_title="Layouts", layout='wide')
st.title('Streamlit Layout')

# sidebar
sidebar = st.sidebar
sidebar.write('This is my sidebar')
sidebar.header('Header in sidebar')

# columns
col1, col2, col3 = st.columns(3)
with col1:
    st.write('This is column -1')
    st.image('path/to/your/cat.jpg')
    
with col2:
    st.write('This is column -2')
    st.image('path/to/your/dog.jpg')
    
with col3:
    st.write('This is column -3')
    st.image('path/to/your/owl.jpg')

# tabs
st.header('Display in Tabs')
tab1, tab2, tab3 = st.tabs(['Cat', 'Dog', 'Owl'])

with tab1:
    st.write('You are in Cat Tab')
    st.image('path/to/your/cat.jpg')
with tab2:
    st.write('You are in Dog Tab')
    st.image('path/to/your/dog.jpg')
with tab3:
    st.write('You are in Owl Tab')
    st.image('path/to/your/owl.jpg')
```

# Exercise:

* Add emojis
