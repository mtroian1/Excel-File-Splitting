# Excel Splitter by Teacher

A Python script that automates the process of breaking down a master Excel spreadsheet into individual, smaller spreadsheets based on a specific column (e.g., separating student lists by Teacher). 

This tool helps educators and administrators organize data rapidly so files can be easily sorted and uploaded to cloud storage platforms like Google Drive.

## ✨ Features
* **Automated Splitting**: Instantly groups rows by identical values in a designated column.
* **File Name Safety Net**: Automatically strips out illegal characters (like `/`, `\`, `*`, or `:`) from names to prevent operating system file saving errors.
* **Auto-Directory Creation**: Dynamically builds the output folder wherever you specify, preventing crashes if the folder doesn't exist yet.

## 🛠️ Prerequisites & Installation

Before running the script, you need to have Python installed on your computer. You will also need to install two standard external packages used for handling Excel data.

Open your terminal (Mac/Linux) or Command Prompt (Windows) and run:

```bash
pip install pandas openpyxl
```

## 🚀 How to Use

1. **Download the Script**: Place the `split_excel.py` script into your project folder.
2. **Add Your Master File**: Put your master Excel spreadsheet (e.g., `master_school_data.xlsx`) in the same directory.
3. **Configure the Script**: Open the script in a text editor and adjust the configuration block at the top if your file or column names are different:
   ```python
   # --- CONFIGURATION ---
   input_file = "master_school_data.xlsx"   # Your master spreadsheet filename
   teacher_column = "Teacher"               # The column name you want to split by
   output_folder = "Split_Teacher_Sheets"   # Where your new files will go
   # ---------------------
   ```
4. **Run the Script**: Execute the script from your terminal:
   ```bash
   python split_excel.py
   ```

All processed files will immediately appear in your newly created output folder, neatly named like `Mr_Smith_Class_List.xlsx`.

## 📂 Google Drive Integration Tip
To fully automate uploading these to separate Google Drive folders without complex API coding:
1. Install the **Google Drive Desktop App** on your machine.
2. Change the `output_folder` path in the script to point directly inside your synced local Google Drive directory. 
3. The script will save files locally, and Google Drive will instantly sync and upload them to the cloud!

## 📄 License
This project is open-source and available under the MIT License.
