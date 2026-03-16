# *Mini-Lab 1*

# Development of a CSV Data Visualization Application with Streamlit

**Objective:** Develop a Streamlit application that allows users to upload a CSV file, display the data, and generate a chart based on a selected numeric column.

# Data Links + VIDEO:


# 1 - Instructions:

1. **Application Title:**

   * Add a title at the top of the page displaying: **"CSV Data Visualization Application"**.

2. **CSV File Upload:**

   * Use a Streamlit function to allow users to upload a CSV file.
   * Specify that only CSV files are accepted.

![image](https://github.com/hrhouma/begining_IA_part1/assets/10111526/de4d848a-0fbd-4410-9f38-fe125421db67)

3. **Reading and Displaying the Data:**

   * Read the uploaded CSV file.
   * Display a preview of the data in a table.

![image](https://github.com/hrhouma/begining_IA_part1/assets/10111526/f365ee79-7af8-4ecb-b976-b0104deb1564)

4. **Column Selection for the Chart:**

   * Allow users to select a column from those containing numeric data (`float` or `int` types).

![image](https://github.com/hrhouma/begining_IA_part1/assets/10111526/5dbb6271-e52b-4e68-b666-8e300f897b97)

5. **Chart Generation:**

   * Generate a line chart based on the selected column.

![image](https://github.com/hrhouma/begining_IA_part1/assets/10111526/d5972913-0f0e-4d4c-9217-7a272e9116be)

6. **Error Handling and Special Cases:**

   * Display a message asking users to upload a CSV file if no file has been uploaded.
   * Make sure the application does not crash in case of errors or invalid files.

7. **Bonus: Uploading the CSV File from the Sidebar:**

   * Use a Streamlit function to allow the CSV file to be uploaded from the sidebar.

# 2 - Specific Requirements:

1. **Display a clear message if no file is uploaded.**
2. **Check that the CSV file contains numeric columns before allowing column selection.**
3. **Handle potential errors when reading the CSV file.**
4. **Add the possibility of uploading the CSV file from the sidebar.**

# 3 - Expected Structure:

1. **Application Title:**

   * Use `st.title` to display the application title.

2. **CSV File Upload:**

   * Use `st.file_uploader` to allow CSV file uploads.

3. **Reading and Displaying the Data:**

   * Read the uploaded CSV file using an appropriate function.
   * Display the data in a table.

4. **Column Selection for the Chart:**

   * Allow selection of numeric columns using an appropriate function.

5. **Chart Generation:**

   * Generate a line chart based on the selected column using an appropriate function.

6. **Error Handling and Special Cases:**

   * Add conditions to display appropriate messages if no file is uploaded or if the file does not contain numeric columns.

7. **Bonus: Uploading the CSV File from the Sidebar:**

   * Add an option to upload the CSV file in the sidebar using an appropriate function.

# 4 - Evaluation Criteria:

1. **Functionality:**

   * The application must correctly upload and read a CSV file.
   * The application must display the data from the CSV file.
   * The application must allow the selection of a numeric column to generate a chart.
   * The application must correctly generate and display a line chart based on the selected column.
   * The application must allow uploading the CSV file from the sidebar (bonus).

2. **User Interface:**

   * The application must be intuitive and easy to use.
   * Error messages must be clear and informative.

3. **Code:**

   * The code must be well structured and commented.
   * The code must handle errors and special cases appropriately.
   * The code must include the option to upload the CSV file from the sidebar (bonus).

# 5 - Submission:

* Submit the source code of the application on LÉA.
* Submitted files must be properly named and include comments explaining the different sections of the code.

Good luck and happy coding!
