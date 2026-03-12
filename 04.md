# Step-by-Step Tutorial for Learning Streamlit on Ubuntu with Virtual Environments

This tutorial explains how to create a Streamlit application on Ubuntu using a virtual environment. It shows how to install Python, create and activate a virtual environment, install Streamlit, write code, test the application, and continue improving it step by step.



# Version A — Ubuntu 22.04

Ubuntu 22.04 LTS supports Python 3.10 as the default packaged version, and it also provides Python 3.11 in the Ubuntu repositories. ([Documentation Ubuntu][1])

## Step 1: Update the system

```bash
sudo apt update
```

## Step 2: Install Python and virtual environment tools

For Ubuntu 22.04, you can install Python 3.10 and Python 3.11 with their virtual environment packages. ([Documentation Ubuntu][1])

```bash
sudo apt install python3.10 python3.10-venv
sudo apt install python3.11 python3.11-venv
```

## Step 3: Verify installed versions

```bash
python3.10 --version
python3.11 --version
```

## Step 4: Create a virtual environment

Using Python 3.10:

```bash
python3.10 -m venv myenv310
```

Using Python 3.11:

```bash
python3.11 -m venv myenv311
```

## Step 5: Activate the virtual environment

If you created `myenv310`:

```bash
source myenv310/bin/activate
```

If you created `myenv311`:

```bash
source myenv311/bin/activate
```

## Step 6: Install Streamlit

With the virtual environment activated:

```bash
pip install streamlit
```

## Step 7: Create the main file

```bash
touch app.py
```

## Step 8: Write your first Streamlit code

Open `app.py` and write:

```python
import streamlit as st

st.write("Hello World")
```

## Step 9: Run the application

```bash
streamlit run app.py
```

<br/>

<br/>

# Version B — Ubuntu 24.04

Ubuntu 24.04 LTS provides Python 3.12 as its packaged Python 3 version in the standard Ubuntu repositories. ([Documentation Ubuntu][1])

## Step 1: Update the system

```bash
sudo apt update
```

## Step 2: Install Python and virtual environment tools

```bash
sudo apt install python3.12 python3.12-venv
```

## Step 3: Verify the installed version

```bash
python3.12 --version
```

## Step 4: Create a virtual environment

```bash
python3.12 -m venv myenv312
```

## Step 5: Activate the virtual environment

```bash
source myenv312/bin/activate
```

## Step 6: Install Streamlit

```bash
pip install streamlit
```

## Step 7: Create the main file

```bash
touch app.py
```

## Step 8: Write your first Streamlit code

```python
import streamlit as st

st.write("Hello World")
```

## Step 9: Run the application

```bash
streamlit run app.py
```

---

# Common Streamlit Example for Ubuntu 22.04 and 24.04

After the application starts, you can expand the content step by step.

## Format text

```python
st.header("This is Header")
st.subheader("This is subheader")
st.caption("This is caption")
st.text("This is plain text")
```

## Use Markdown

```python
st.markdown("""
# This is title
## This header
### subheader -1
#### subheader -2

simple plain text

for *italic* use asterisk
for **bold** format use two asterisks
""")
```

## Display status messages

```python
st.success("this message displays text in a green background")
st.warning("this message displays text in a yellow background")
st.error("this message displays text in a red background")
```

## Display an image

```python
st.subheader("Display Image")
st.image("./media/mountains.webp", caption="mountains", width=300)
```

## Display a video

```python
st.subheader("Display Video")
video_file = open("./media/star.mp4", mode="rb").read()
st.video(video_file)
```

---

# Complete `app.py` File

```python
import streamlit as st

# Display simple text
st.write("Hello World")

# Format text
st.header("This is Header")
st.subheader("This is subheader")
st.caption("This is caption")
st.text("This is plain text")

# Use Markdown
st.markdown("""
# This is title
## This header
### subheader -1
#### subheader -2

simple plain text

for *italic* use asterisk
for **bold** format use two asterisks
""")

# Display Status Messages
st.success("this message displays text in a green background")
st.warning("this message displays text in a yellow background")
st.error("this message displays text in a red background")

# Display Images
st.subheader("Display Image")
st.image("./media/mountains.webp", caption="mountains", width=300)

# Display Videos
st.subheader("Display Video")
video_file = open("./media/star.mp4", mode="rb").read()
st.video(video_file)
```

---

# Appendix 1 — Virtual Environment Commands Summary

On Ubuntu 22.04, the official packaged Python versions are 3.10 and 3.11. On Ubuntu 24.04, the official packaged Python version is 3.12. ([Documentation Ubuntu][1])

## Ubuntu 22.04

```bash
sudo apt update
sudo apt install python3.10 python3.10-venv
sudo apt install python3.11 python3.11-venv

python3.10 -m venv myenv310
python3.11 -m venv myenv311

source myenv310/bin/activate
deactivate
```

## Ubuntu 24.04

```bash
sudo apt update
sudo apt install python3.12 python3.12-venv

python3.12 -m venv myenv312

source myenv312/bin/activate
deactivate
```

## Important Note

If you need versions beyond what Ubuntu provides in its standard repositories, the cleanest approach is usually `pyenv`, because the standard packaged versions differ between Ubuntu releases. Based on Ubuntu’s official availability table, 22.04 and 24.04 do not expose the same Python version set in their default repositories. ([Documentation Ubuntu][1])


[1]: https://documentation.ubuntu.com/ubuntu-for-developers/reference/availability/python/?utm_source=chatgpt.com "Available Python versions - Ubuntu for Developers"
