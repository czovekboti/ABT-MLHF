# ABT-MLHF
Repository for deep learning group homework.

**Team Name:** ABT

## Team Members
* Baranyai András -
* Czövek Botond -
* Sági Tamás - G9VGFF

## Project Description

This project tackles the [Airbus Ship Detection challenge on Kaggle](https://www.kaggle.com/c/airbus-ship-detection). The primary goal of the overall challenge is to build an image segmentation model that can accurately detect all ships in satellite images, even in crowded port scenes.

## File Descriptions

* `MLHW_Data_clean.ipynb`: The main Jupyter Notebook containing all Python code for the entire data processing and preparation pipeline.
* `kaggle.json`: (Not included in this repo for security). This file is your personal Kaggle API key, which is **required** to download the dataset. It must be placed in the root directory of this repository to run the notebook.
* `LICENSE`: Contains the full text of the GNU Affero General Public License v3.
* `README.md`: This file, providing an overview of the project, team members, and instructions.
* `scientific_background.md`: Provides an introduction to the problem, the project's motivation (environmental, security, logistics), and the scientific context, including the challenges of cloud/haze.

## License

This project is licensed under the **GNU Affero General Public License v3 (AGPLv3)**.
See the `LICENSE` file for the full license text.

## How to run

### Prerequisites

1.  **Kaggle API Key (Optional):**
    * To use the notebook's automatic download feature (Cell 4), go to your Kaggle account settings (`https://www.kaggle.com/[YourUsername]/account`).
    * Click "Create New API Token". This will download a `kaggle.json` file.
    * Place this `kaggle.json` file in the same directory as the `MLHW_Data_clean.ipynb` notebook.

2.  **Kaggle Dataset (Manual Download Recommended):**
    * The notebook includes a cell to download the dataset via the Kaggle API. However, the dataset is **very large (multiple GB)** and the download can fail or take a significant amount of time.
    * **It is recommended to manually download** the `airbus-ship-detection.zip` file from the [Kaggle competition page](https://www.kaggle.com/c/airbus-ship-detection/data).
    * Once downloaded, place the `airbus-ship-detection.zip` file in the **same root directory** as the `MLHW_Data_clean.ipynb` notebook.

3.  **Python Libraries:**
    * You will need to install the required Python libraries. You can usually install them using `pip`:
    ```bash
    pip install kaggle pandas numpy matplotlib pillow scikit-learn torch albumentations
    ```

### Running the Notebook

1.  Ensure either the `kaggle.json` file (for API download) or the `airbus-ship-detection.zip` file (for manual download) is in the root directory.
2.  Open the `MLHW_Data_clean.ipynb` file in a Jupyter environment (like Jupyter Lab, Jupyter Notebook, or Google Colab).
3.  Run the cells sequentially from top to bottom.
    * **If you downloaded the data manually**, you can skip Cell 4 (`!kaggle competitions download...`) and run Cell 5 (`import zipfile...`) directly to unzip the file.

The notebook will then:
1.  Extract the data into the `./airbus_data/` directory.
2.  Perform all cleaning, splitting, and preprocessing steps.
3.  Display visualization samples at the end as a sanity check.