# 20220831_Databricks_Simple_Demo
I have created several simple [notebooks](https://github.com/feifeiwww/20220831_Databricks_Simple_Demo/tree/main/notebooks) to help new users understand Databricks' use cases. A lot of the examples are based on the raw_data diabetes_modified.csv files. Users can create a database on Databricks by using ```%sql create database feifei_wang ```, and use UI to upload this csv file to the database. 
* notebook1: This notebook is to show within one Databricks notebook, you can run python, sql, R, scala, markdown, sh, pip etc. 
* notebook2: This notebook is to show that you can use Databricks as simple as you use python locally (for example Jupyter notebook). If you are using ML clusters 10.4ML+, and if you are running sklearn, tensorflow etc. models, MLflow is automatically enabled to help you track your model parameters, metrics etc. 
* notebook3: This notebook is spark is faster. This tutorial is from Datbricks Academy course [here](https://github.com/databricks-academy/scalable-machine-learning-with-apache-spark) under ML14. You will need to have both the "Includes" folder and the ML14 notebook under the same folder in order to run it under Databricks
.
* notebook4: This notebook is to show you can create widgets and create dashboard based on your notebook immediately.
* notebook5: This notebook is to show the steps to use autoML. You can begin building your first regression/classification/forecast model without writing any code.
* notebook6: This notebook is to show the fine grained time series models running in parallel tutorial. You may build thousands of time series models in parallel and run them in minutes to get the forecast results using Databricks. [Here](https://www.databricks.com/blog/2021/04/06/fine-grained-time-series-forecasting-at-scale-with-facebook-prophet-and-apache-spark-updated-for-spark-3.html) is the orginal blog post. 

## If you would like run this demo on Databricks Community Edition (free), please follow the instructions below:


Note that Community Edition is a free offering of Databricks and there are a few features that are not available on Community Edition, such as the Model Registry.


  (a) First sign up for a free Community Edition account, please refer to this [doc](https://docs.databricks.com/getting-started/community-edition.html) if you have questions. You can use [this link](https://community.cloud.databricks.com/login.html) to sign in if you have an existing account.
![image](https://user-images.githubusercontent.com/109642474/180575265-ecbf6401-bf87-4fa3-b769-965318ff1790.png)


  (b) Download notebook files and import them into your user account using Databricks Community Edition. Refer to this [doc](https://docs.databricks.com/notebooks/notebooks-manage.html#import-a-notebook) under *"import a notebook"* section.
  
  ![image](https://user-images.githubusercontent.com/109642474/180575795-0e705ec3-4281-49b3-973e-630606c6adee.png)


  (c) Create a cluster under the "Compute" tab on the left, select Databricks runtime version `10.4 LTS ML`, and name the cluster `test10.4ML`. Please ensure you are using `10.4 LTS ML` and not `10.4 LTS` as the ML runtime pre-installs many useful libraries, such as TensorFlow & MLflow. Refer to this [doc](https://docs.databricks.com/clusters/create.html) about how to create a cluster. It may take a few minutes to start a cluster. 
  
  ![image](https://user-images.githubusercontent.com/109642474/180576008-c55d3162-a5df-414a-839c-7048c9af40b5.png)


  (d) Open the imported notebooks on Databricks from the workspace tab, open one notebook, attach the `test10.4ML` cluster to your notebook, then click "Run All" on the top to run the notebook. Refer to this [doc](https://docs.databricks.com/notebooks/notebooks-manage.html#attach-a-notebook-to-a-cluster) under the section *"Attach a notebook to a cluster"*. 
  
  ![image](https://user-images.githubusercontent.com/109642474/180576291-1bdcd11a-c400-4152-afe1-c92a8fc577c2.png)
  
  ![image](https://user-images.githubusercontent.com/109642474/180576518-f4f71fda-05e0-48b5-8a6a-d32048981d11.png)


  (e) You can also try to import and open other notebooks similarly, attach it to the cluster `test10.4ML`, and click "Run All". It may take several minutes to run a notebook.

  (f) Important note: you must attach your notebook to a cluster before you can run it. If your cluster is terminated, you need to restart it or re-create a new cluster. 

  (g) You may check your MLflow experiments by clicking "Experiments" on the top of a notebook, or got to "Experiments" tab on the left under "Machine Learning" persona. 
  
  
  **2. Or locally (for example, Jupyter notebook):**

* Certain notebooks may require additional setups. We recommend you using Databricks to run most of the demo notebooks. 
* To use MLflow locally, you may need to add additional code and steps for configuration. These steps may include ```pip install mlflow``` to install MLflow locally,  ```!mlflow ui``` to view the MLflow UI, and ```!pkill -f gunicorn``` to stop the UI. Note: it is an exercise for the users, so the full code is not provided here. 

