# Runnable LogGenius Project

## Reasons for Failure to Run
1. The large model API has expired and cannot be successfully invoked.
2. The dataset in the read path is missing, causing a data read error.
3. The folder for the write path has not been created, causing a file write error during runtime.
4. There are naming errors in the code.

## Fixes
1. Added the ByteDance DouBao large model API invocation method, allowing the choice to call the DouBao API (feasibility has been verified).
2. The required dataset has been added to the read path (`logs`).
3. All necessary folders have been created in this repository.
4. The code errors in the existing log datasets in this repository have been corrected.

## You can now run LogGenius using the datasets (alarm, Apache, OpenSSH, OpenStack, Zookeeper) in this repository.

### Usage:
#### 1. English Datasets:
In the `runLogGenius.py` file, first modify the `main` function to call `E_dataset()`, then modify the value of the `log_file` variable in the `E_dataset()` function to the target file name (located in the `/logs` path, such as `"Apache_2k_logs"`), and change the `dataset_name` to the corresponding dataset type (such as `"Apache"`).

#### 2. Chinese Datasets:
In the `runLogGenius.py` file, first modify the `main` function to call `C_dataset()`, then modify the value of the `log_file` variable in the `C_dataset()` function to the target file name (located in the `/logs` path, such as `"alarm_1k.logs"`).

#### 3. Enter the corresponding apikey and model ID for invocation. (Choose between ChatGPT or DouBao)

## Folder Explanations:
- `Code`: Contains the LogGenius source code.
- `Dataset`: Log datasets (with the file extension `.log`).
- `log_after_entropy`: Numbers corresponding to log data waiting for enhanced diversity.
- `log_after_gpt`: Original log data and log data expanded by the large model.
- `log_after_group`: Templates identified by Drain and the log data numbers corresponding to each template.
- `log_after_select`: The optimal data selected from the log data expanded by the large model according to rules.
- `logs`: The read path for the code, containing the log data to be processed (note that the file extension is `.logs`!).
- `new_dataset`: The output path for results.

## Contact Me
If you have any questions, please feel free to contact me via email at 2300303120@cjlu.edu.com.
