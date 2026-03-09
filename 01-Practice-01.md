# Step-by-Step Tutorial for Learning Streamlit with Virtual Environments

This tutorial will guide you in creating a Streamlit application using the `streamlit` module in a virtual environment. The goal is to teach you how to create a virtual environment, write code, test the results, then continue writing and testing.

#### Prerequisites

* Python installed on your machine.
* `virtualenv` installed (`pip install virtualenv`).

# Step 1: Creating the Virtual Environment

1. Open your terminal and navigate to the folder where you want to create your project.
2. Create a virtual environment:

```bash
python -m venv myenv
```

or

```bash
python3.7 -m venv myenv37
python3.8 -m venv myenv38
python3.9 -m venv myenv39
python3.10 -m venv myenv310
python3.11 -m venv myenv311
python3.12 -m venv myenv312
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

### Troubleshooting in case of problems

> You may have PowerShell restrictions the first time.

### Solution:

* Run the following commands in admin mode:

```bash
Set-ExecutionPolicy Unrestricted
```

or

```bash
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
```

# Step 2: Installing Streamlit

1. With the virtual environment activated, install Streamlit:

```bash
pip install streamlit
```

# Step 3: Creating the Main File

1. Create a Python file, for example `app.py`, in your project folder.

# Step 4: Write and Test the Code

**Display simple text**

1. Open `app.py` and write the following code:

```python
import streamlit as st

st.write("Hello World")
```

2. To test, open your terminal (with the virtual environment activated) and run:

```bash
streamlit run app.py
```

**Format text**

1. Add the following lines to display different text formats:

```python
st.header("This is Header")
st.subheader("This is subheader")
st.caption('This is caption')
st.text('This is plain text')
```

2. Save and test again with the command `streamlit run app.py`.

**Use Markdown**

1. Add the following code to display formatted text with Markdown:

```python
st.markdown("""
# This is title
## This header
### subheader -1
#### subheader -2

simple plain text

for *italic* use asterisk
for **bold** format use two asterisk
""")
```

2. Save and test.

# Step 5: Display Status Messages

1. Add the following lines to display success, warning, and error messages:

```python
st.success("this message display text in green background")
st.warning("this message display text in yellow background")
st.error("this message display text in red background")
```

2. Save and test.

# Step 6: Display Media

**Display Images**

1. Add this code to display an image:

```python
st.subheader("Display Image")

st.image('./media/mountains.webp',
         caption='mountains',
         width=300)
```

2. Make sure you have an image `mountains.webp` in the `media` folder.

3. Save and test.

**Display Videos**

1. Add the following code to display a video:

```python
st.subheader('Display Video')
video_file = open('./media/star.mp4',mode='rb').read()
st.video(video_file)
```

2. Make sure you have a video `star.mp4` in the `media` folder.

3. Save and test.

### Complete Code

Here is the complete code for the `app.py` file:

```python
import streamlit as st

# Display simple text
st.write("Hello World")

# Format text
st.header("This is Header")
st.subheader("This is subheader")
st.caption('This is caption')
st.text('This is plain text')

# Use Markdown
st.markdown("""
# This is title
## This header
### subheader -1
#### subheader -2

simple plain text

for *italic* use asterisk
for **bold** format use two asterisk
""")

# Display Status Messages
st.success("this message display text in green background")
st.warning("this message display text in yellow background")
st.error("this message display text in red background")

# Display Images
st.subheader("Display Image")
st.image('./media/mountains.webp', caption='mountains', width=300)

# Display Videos
st.subheader('Display Video')
video_file = open('./media/star.mp4',mode='rb').read()
st.video(video_file)
```

# Step 7: Formative Assessment

#### Instructions

1. Create a new virtual environment and activate it.
2. Install Streamlit in this environment.
3. Create a file `app.py` and implement the following features one by one, testing at each step:

   * Display simple text.
   * Format text with different methods.
   * Use Markdown to format text.
   * Display success, warning, and error messages.
   * Display an image.
   * Display a video.
4. Submit the final `app.py` file and a screenshot of each tested step.

#### Exercise

1. **Text Display**

   * Display "Hello Streamlit" with `st.write`.
   * Add a header, a subheader, a caption, and simple text.

2. **Markdown**

   * Use `st.markdown` to display a title, a subtitle, and text in italic and bold.

3. **Status Messages**

   * Display success, warning, and error messages.

4. **Media**

   * Display an image and a video of your choice. Use local files or URL links.

5. **Advanced Features (Optional)**

   * Add a sidebar with a title.
   * Use a form element to get user input.

### Example Solution

```python
import streamlit as st

# Display simple text
st.write("Hello Streamlit")

# Format text
st.header("This is a Header")
st.subheader("This is a Subheader")
st.caption("This is a caption")
st.text("This is plain text")

# Use Markdown
st.markdown("""
# This is a Title
## This is a Subtitle
This is *italic* text and this is **bold** text.
""")

# Display Status Messages
st.success("This is a success message")
st.warning("This is a warning message")
st.error("This is an error message")

# Display Images
st.subheader("Display Image")
st.image('path/to/your/image.jpg', caption='Sample Image', width=300)

# Display Videos
st.subheader("Display Video")
video_file = open('path/to/your/video.mp4', 'rb').read()
st.video(video_file)

# Optional: Sidebar and form
st.sidebar.title("Sidebar Title")
with st.sidebar.form(key='my_form'):
    name = st.text_input('Enter your name')
    submit_button = st.form_submit_button(label='Submit')
    if submit_button:
        st.write(f'Hello {name}')
```

# Exercise:

* Add a password field to the form.
