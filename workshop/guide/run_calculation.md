# Running MEGqc

## Running the calculation module
Now, we're ready to run MEGqc! First, ensure that your environment is activated by checking the terminal prompt. It should look like this:

        (<your_environment_name>) **user_name:** ~$



Once the environment is actived, execute the script from the **terminal** and not from the command panel. The command might look somehting like this:

        run-megqc --inputdata /path/to/your/dataset/


## Settings
When you enter the command, a terminal-based GUI will prompt you with the question: `Do you want to proceed with the default settings? (y/n)`.
If you enter `y`, the program will use the default values for the parameters of each **metric**. The default settings, as calculated by Gaponsetva (2023), are designed to be compatible with a broad amount of datasets. A hyperlink in the terminal will direct you to the [setting explanation page](settings_explanation.md), where each parameter is described with more detail.

If you enter `n`, you will be instructed to use the following command to specify a path (to your `target directory`) where a copy of the config file (`setting.ini`) will be created: 
        
        get-megqc-config --target_directory <path/to/your/target/directory>

For example, if you want to analyze only a specific subject's dataset instead of the entire dataset, create a copy of `settings.ini`, and modify the **subjects** variable by replacing `'all'` with a string containing the subject ID(s), for example, `009`.




<!--
OLD VERSION

## Setting File Paths

Within the `docker` folder of the cloned repository, you'll find the script **run_megqc.py**. To configure the software, you need to edit 2 filepaths of this script:
1. **config_file_path=** here you'll need to write the path to the **settings.ini_**.

2. **internal_config_file_path=** here you'll need to write the path to the **settings_internal.ini**.

Both setting files are located in  the `settings` folder within the `meg_qc` package, which reside in the `site-packages` directory of yourPython  environment. The path should look something like this:

        /path/to/environment/lib/python3./site-packages/meg_qc/settings/settings.ini

<br>


## Specifying Dataset Path and Subjects

Next open the file **setttings.ini** to edit the data directory path and specify the subjects to be analyzed:

- **subjects=** is a string variable, you shall write the code of the participant you want to analyze (f.e., 009). You can also provide a list of subjects separated by a comma (001, 002, 003) or write "all" to process all subjects.

- **data_directory=** SEt this to the path to the dataset directory. In case that you want to analyze more subject, the pipeline will find them within the dataset thanks to the ancpBIDS library. 

The file **setttings.ini** also contains an extensive amount of customizable parameters. However, the default values are optimized to to work with the majority of datasets. [In the next section you can find  more details about these parameters](settings_explanations.md).

-->