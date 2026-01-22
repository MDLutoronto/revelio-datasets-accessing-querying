---
title: "Accessing and Querying the Revelio Datasets"
layout: "home"
staff:
    - name: Kara Handren
      link: https://library.utoronto.ca/staff/kara-handren
description: The University of Toronto has licensed six separate datasets from Revelio Labs. These are workforce datasets that range in size from 1 to 4 TB. To facilitate easy access and querying across products, all datasets have been loaded into SciNet's supercomputing environment. Access to this environment can only be granted to current University of Toronto Faculty, Staff and Students, after an application process. This page contains additional details about this process, as well as the data itself and how to query it.
permalink: "/"  #! Remove this if not the homepage
created_date: 2025-05-21
---

# Accessing and Querying the Revelio Datasets

The University of Toronto has licensed six separate datasets from [Revelio Labs](https://www.reveliolabs.com/data/). These are workforce datasets that range in size from 1 to 4 TB. To facilitate easy access and querying across products, all datasets have been loaded into SciNet's supercomputing environment. Access to this environment can only be granted to current University of Toronto Faculty, Staff and Students, after an application process. This page contains additionals details about this process, as well as the data itself and how to query it.

### **Tables of Contents:**

[Understanding the Revelio Labs Datasets](#understanding-the-revelio-labs-datasets)  
[Working with the Revelio Labs Datasets](#working-with-the-revelio-labs-datasets)  
[Accessing the Environment](#accessing-the-environment)  
.[Accessing the Environment via Terminal](#accessing-the-environment-via-terminal)  
.[Accessing the Environment via Open OnDemand](#accessing-the-environment-via-open-ondemand)  
[Sample Python Code](#sample-python-code)

### Understanding the Revelio Labs Datasets

Note: Data Dictionaries for the six products listed below can be found [here](https://www.data-dictionary.reveliolabs.com/). The University of Toronto does not license the *Transitions* Dataset.

##### Workforce Dynamics

This dataset provides an overview of a company's composition. This includes headcounts, inflows, and outflows for every unique position, segmented by job, seniority, geography, salary, education, skills, and gender \& ethnicity. Coverage is global, from 2007 \- 2024\.

##### Job Postings

This dataset includes active postings, new postings, removed postings, salaries, and full text of postings for any company, segmented by various employee characteristics (occupation, seniority, geography, keywords, skills, etc). This dataset is pulled from over 350 thousand company websites, all major job boards, and staffing firm job boards. Coverage is global, from 2021\-2024\.

There are three subfolders within this dataset: *unified, linkedin*, and *indeed.* The unified job postings is comprehensive of all sources and includes linkedin, indeed, companies sites, and other job aggregators. Note however that this folder contains fewer records as records in the *unified* folder have been deduplicated not only across sources but also within sources. So, a post that got posted 5 times on LinkedIn for seemingly the same role would only appear once in the unified postings.

Note also that the University of Toronto does not license the aggregate "Job Postings Dynamic" dataset, but only the individual\-level data. Finally, although this is not listed in the data dictionary, these datasets do contain a "description" field with the original job description text, when available.

##### Sentiment

This datasets includes employee reviews for all companies, with the full text of each review split into positive and negative text. Reviews are mapped to various employee characteristics (occupation, seniority, geography). Coverage is global, from 2008\-2024\.

##### Layoff Notices

This dataset includes post data and effective date for all layoffs in every company in the United States. Coverage is limited to the US, and dates range from 2008\-2020 to 2024, depending on the State.

##### Individual Level Data

This datasets contains data on the full professional history of individuals, including their roles, education, skills, gender, ethnicity, salary, seniority, and geography. Coverage is global, from 2008\-2024\.

##### Company Reference Data

This dataset contains information on companies that are covered by or referenced in the five other datasets listed above.

Working with the Revelio Labs Datasets
--------------------------------------

### Creating an Account

1. [Get a Compute Canada account](#ccaccount)
2. [Opt into the Trillium service](#niagara)
3. [Upload an SSH key to CCDB](#ssh)
4. [Request Access to Revelio](#revelio)
5. [Setting up Multifactor Authentication](#mfa)

These steps only need to be completed once to gain access, and should normally only take a few days at most to be approved.

1\. Get a Compute Canada account

Please visit the[Compute Canada Database (CCDB) website](https://ccdb.computecanada.ca/account_application)and apply for an account (takes a day or two to approve).  
   
Note: Students and postdocs need to be sponsored by their supervisor, who would need to already have a Compute Canada account (or create one first). This is a simple process, requiring the student to complete a form and their supervisor to approve the sponsorship. Computing resources would be sharing under the sponsor's allocation. Please [contact the Map \& Data Library](https://mdl.library.utoronto.ca/about/contact-form) for assistance, or for more information.

2\. Opt in to the Trillium service

After the Compute Canada account is approved, you should opt in to the Trillium service on the CCDB website (or use this[direct link](https://ccdb.alliancecan.ca/me/access_systems)). The opt\-in will be approved manually after one or two days, which will give you access to the Trillium supercomputer and other SciNet systems, as long as the SSH key has been uploaded to the CCDB website ([see next step](#ssh)).

3\. Upload an SSH key to CCDB

Next, locate the Manage SSH Keys option on you account page on the CCDB website (or use this[direct link](https://ccdb.computecanada.ca/ssh_authorized_keys)) and upload your public SSH key.[Instructions on creating SSH key pairs](http://docs.scinet.utoronto.ca/index.php/SSH#SSH_Keys)from the SciNet Wiki can help you with this process. This wiki also contains pages with more information on [creating SSH key pairs specifically on a Windows machine](https://docs.computecanada.ca/wiki/Generating_SSH_keys_in_Windows/en), or on [Mac or Linux machines](https://docs.computecanada.ca/wiki/Using_SSH_keys_in_Linux). The Map \& Data Library also provides a [quick start tutorial for creating SSH key pairs on a Mac](https://mdl.library.utoronto.ca/technology/tutorials/generating-ssh-key-pairs-mac), if you need more help.

4\. Request access to Revelio

Access to the Revelio dataset is by request only. Please [contact us](https://mdl.library.utoronto.ca/about/contact-form) to request access.

**Note** there are other licensed datasets hosted on SciNet, such as the Web of Science PostgreSQL database, that require a separate approval process. Please see [this page](https://mdl.library.utoronto.ca/technology/tutorials/how-access-postgresql-databases) for more information on accessing those collections.

5\. Setting up Multifactor Authentication

Access to all SciNet services now requires multifactor authentication. If you are not prompted to do so during your initial account setup, this can be done by [logging into](https://ccdb.alliancecan.ca/) your Compute Canada account, and selecting **Account \> Multifactor Authentication** from the top droptown menu. Please note thar although Duo is the recommended application for this, this is distinct from the multifactor authentication used for your utorID.

### Accessing the Environment

If working in high performance computing environment is new to you, we would recommend you attend [SciNet workshops](https://education.scinet.utoronto.ca/) to learn more, especially their Intro to SciNet \& Triullium workshop (run periodically) or watch [a recording of a previous session](https://www.youtube.com/@scinethpcattheuniversityof8962).

As of late 2025, there are now two distinct ways to access and query data hosted in this environment: [via terminal,](#terminal) or using a web\-based platform called [Open OnDemand](#ood). Please read through the options below, and choose the one that works best based on your experence and comfort levels with programming.

### Accessing the Environment via Terminal

### Here are some steps to get your started **on a Windows machine**:

1. To access the environment from a Windows machine, you will need an SSH client. We would recommend [MobaXterm](https://mobaxterm.mobatek.net/), and we will be using it in our tutorial examples
2. Once you have installed MobaXterm, start it up
3. From the Session menu, select New Session
4. Select SSH from the top left
5. For the remote host, use this format \<computecanadausername\>@trillium.scinet.utoronto.ca, substituting in your Compute Canada account username. For example, doej@trillium.scinet.utoronto.ca
6. Click on the Advanced SSH settings tab below
7. For SSH\-browser type, select SCP (enhanced speed)
8. Put a checkmark next to Use private key. Click on the blue page icon to browse to the private key you setup when creating your public key for your Compute Canada account
9. Then click on OK to connect
10. Enter in your Compute Canada account password
11. You are now connected to the server
12. To log out, type `exit` and press Enter. Then press Enter again to close the tab

And the same steps, **on a Mac**:

1. You do not need to install any programs or clients to access the environment from a Mac. Access is via Terminal.
2. You will use an SSH key to connect. This requires some initial configuration, but once this is done it is both more secure and more convenient. If you have not already generated a key pair, instructions on how to do so can be found [here](https://mdl.library.utoronto.ca/technology/tutorials/generating-ssh-key-pairs-mac). More detailed instructions are also available on the [SciNet wiki](https://docs.computecanada.ca/wiki/Using_SSH_keys_in_Linux). Remember, you'll need create a key\-pair on any systems you intend to connect with!
3. To login to the remote host, use this command in Terminal: `ssh -i .ssh/myprivatekeyname <computercanadausername>@trillium.scinet.utoronto.ca`. The system will prompt you to enter the passphrase for your key (Note,`-i .ssh/myprivatekeyname`is only necessary if you are not using the default key filepath and filename. See complete SSH setup instructions [here](https://mdl.library.utoronto.ca/technology/tutorials/generating-ssh-key-pairs-mac) for more information).
4. You are now connected to the server
5. To log out, type `exit` and press Enter. You are now back in your local environment.

### Querying the Datasets

All six datasets are in Apache Parquet format. This is a tabular datatype, similar to an Excel CSV file, but one that is capable of handling much larger files. Parquet files are binary, columnar files that are designed for reading and writing extremely large datasets, have built in compression and are optimized for analytics. For these reasons, these files can't be opened or manually inspected by humans. They need to be worked with using big data tools.

Each dataset / directory is composed of many parquet files, up to 11000 per folder. Company reference data provides for a unique identifier across most datasets in the form of a unique company ID, allowing for querying across directories.

**Important Note: These files are read only. Although they can be queried and explored, new copies or subsets will need to be created during analysis.**

1. You will need to use [Linux/UNIX command line](https://LINUX COMMAND LINE) in order to navigate the environment. Once logged into SciNet, navigate to the following folder using the cd command to change the current directory: `cd /project/restricted/mdl/revelio`
2. Type `ls` to view a list of all folders inside the directory. You can then use the `cd` command to navigate to an individual directory. For example, `cd academic_layoff`  
<img src='{{ '/assets/images/Revelio_filequery.jpg' | relative_url }}' alt='screenshot of the directories within the revelio folder' title='' width='872' height='103' />

    1. **Please note**: some products contain multiple folders. For example, there are three folders related to the job postings dataset: *academic\_postings\_indeed\_individual, academic\_postings\_linkedin\_individual* and *academic\_postings\_unified\_individual***.** Please see the [vendor documentation](https://here) if the contents of each folder are unclear. Otherwise, [contact us](https://mdl.library.utoronto.ca/about/contact-form) for additional support.
        2. **Please also note:** The *academic\_* prefix does not represent that the data refers only to academic institutions or research centres. The data is comprehensive across employment fields and segments. This denotes only that the data was purchased for academic use.
3. You will need to use big data tools to work with this data. If working with python, **PyArrow** \+ **Pandas** provide excellent support for querying and analyzing parquet files. You can read more about working with [PyArrow](https://arrow.apache.org/docs/python/index.html) and [Pandas](https://pandas.pydata.org/docs/user_guide/index.html) via their oline documentation. Please note that there are other libraries and tools for working with these files. If you've like to explore other options, [this guide](https://www.datacamp.com/tutorial/apache-parquet) is an excellent place to start.
4. ##### **Note: Queries and code run on the login node are for testing purposes only. Once you have compiled and tested your code or workflow on the Trillium login nodes, you will need to** [**submit it as a job**](https://docs.scinet.utoronto.ca/index.php/Niagara_Quickstart#Submitting_jobs) **to be run on the compute node.** **Any lengthy process being run on the login node will be automatically stopped.**
5. If using Python, you will need to load a python module into your environment. SciNet provides [excellent documentation](https://docs.scinet.utoronto.ca/index.php/Python#Installing_your_own_Python_Modules) on this. Note that Python 3\.11\.5 has been installed as a default module and does come pre\-loaded with many useful packages including Pandas. However, as PyArrow is not part of this, you will need to follow the steps outlined by Scinet to set up a virtual environment in order to install PyArrow or other packages as needed.  See below for screenshots of an example creationg of a new environment, *revelioenv* , as well as the activation of that enviromment and installation of Pyarrow. This follows the SciNet instructions linked above:
	1. Type `module load python` in order to load the default Python module.
	2. Next type `mkdir ~/.virtualenv` to create a directory in your environment to store your new virtual environment
	3. Next type `virtualenv --system-site-packages ~/.virtualenv/[myenvironmentname]env` to create your new environment.
	4. Next type `module load gcc arrow` to activate the pyarrow engine. This must be done before activating your new virtual environment and installing pyarrow .
	5. Next type `source ~/.virtualenv/[myenvironmentname]env/bin/activate` to activate your environment. The name of your environment should now appear to the far left of your screen.
	6. Finally type `pip install pyarrow` to install the pyarrow module. There is no need to install pandas as this is one of the default packages.  
	<img src='{{ '/assets/images/Revelio_virtualenv.jpg' | relative_url }}' alt='setting up a virtual environment and installing pyarrow' title='' width='1186' height='294' />
		1. **Note:** You can install as many modules as needed. You'll need to activate this environment every time you log in, and at the start of all your jobs scripts. However, the creation of then environment and installation of packages only needs to be done once. The next time you log in, you can skip steps A \> C above and simply type steps D \& E:
			1. `module load gcc arrow`
			2. `source ~/.virtualenv/[myenvironmentname]env/bin/activate`
6. Once you have compiled and tested your script on a smaller subset of the data within the login node, you will need to [submit it as a job](https://docs.scinet.utoronto.ca/index.php/Niagara_Quickstart#Submitting_jobs) to be run on one of SciNet's compute nodes, per SciNet's instructions. These instructions also include [example submission scripts](https://docs.scinet.utoronto.ca/index.php/Slurm#Example_submission_scripts). The output will be written to your $SCRATCH directory.
7. If you would prefer to use a different language to query the data, please see the relevant documentation on SciNet's website. For example, Parquet files can also be queried using C\+\+ or Java.

### Accessing the Environment via Open OnDemand

Open OnDemand (OOD) is a web\-based platform that allows you to interact with Trillium through a web browser instead of via a terminal. As thereis no need to install any software on your local machine, the access instructions below apply regardless of your operating system:

1. Once all steps under "Creating an Account" above have been completed, navigate to [SciNet's installation of Open OnDemand](https://ondemand.scinet.utoronto.ca/) to login to the system.
	1. Note that unlike when logging in to your Compute Canada account, this login page requires your *username*and not your utoronto email in order to authenticate.
	2. You will still be prompted to authenticate using multifactor authentication
2. Once logged in, you'll be presented with a landing page consisting of all applications currently available via the Open OnDemand System. These include entry points for terminal access, as well as a quick review of any active jobs.  
<img src='{{ '/assets/images/image_75.png' | relative_url }}' alt='open ondemand landing page' title='' width='657' height='474' />

    Note that while this tutorial will only cover access via Jupyter Lab, several other applications for coding are included, including RStudio and VS Code. Other applications for data analysis such as Stata and SAS are also available.
3. Select **Jupyter Lab** in order to launch a new Jupyter Server on the Trillium Cluster. You will be prompted for several parameters, including expected number of hours for this session as well as computing requirements. As these datasets are fairly small in the context of high performance computing, "number of physical cores" can be set to "1", with "4" GB of memory.
4. Select **Launch** to begin your session. Note that it may take a minute to two to start up. Once the server is available, "Running" will appear as the status in top left, and you will be able to select the "Connect to Jupyter" button near the bottom to begin coding in Jupyter Labs  
<img src='{{ '/assets/images/image_76.png' | relative_url }}' alt='jupyterlab server session launch' title='' width='669' height='331' />
5. Once connected, you will see a list of your files to the left, and a Launcher in the centre screen. The launcher provides Jupyter Notebook or console/terminal programming environments for Python or R, as well as other options such as terminal access to the server or new text file creation near the bottom.  
  
<img src='{{ '/assets/images/image_77.png' | relative_url }}' alt='jupyter lab landing page' title='' width='709' height='399' />
6. If this is your first time using Jupyter Labs, please see their [excellent documentation](https://jupyter.org/try-jupyter/notebooks/?path=notebooks/Intro.ipynb) or review our own Workshop, ["An Introduction to Programming for Absolute Beginners Using Python Pt. 1"](https://mdl.library.utoronto.ca/technology/tutorials/python-information-tutorials-and-workshops) which provides an overview of coding in Jupyter Notebooks (the executable document files that also form the basis of Jupyter Labs).

#### Querying the Datasets

All six datasets are in Apache Parquet format. This is a tabular datatype, similar to an Excel CSV file, but one that is capable of handling much larger files. Parquet files are binary, columnar files that are designed for reading and writing extremely large datasets, have built in compression and are optimized for analytics. For these reasons, these files can't be opened or manually inspected by humans. They need to be worked with using big data tools.

Each dataset / directory is composed of many parquet files, up to 11000 per folder. Company reference data provides for a unique identifier across most datasets in the form of a unique company ID, allowing for querying across directories.

**Important Note: These files are read only. Although they can be queried and explored, new copies or subsets will need to be created during analysis.**

1. If you simply wish to browse the included files and folders, you will need to use [Linux/UNIX command line](https://LINUX COMMAND LINE) via terminal in order to navigate the environment. From your JupyterLab session, select **Terminal** under **Other** from the Launcher. Navigate to the following folder using the cd command to change the current directory: `cd /project/restricted/mdl/revelio`
2. Type `ls` to view a list of all folders inside the directory. You can then use the `cd` command to navigate to an individual directory. For example, `cd academic_layoff`  
<img src='{{ '/assets/images/image_78.png' | relative_url }}' alt='terminal jupter lab preview' title='' width='720' height='101' />

    1. **Please note**: some products contain multiple folders. For example, there are three folders related to the job postings dataset: *academic\_postings\_indeed\_individual, academic\_postings\_linkedin\_individual* and *academic\_postings\_unified\_individual***.** Please see the [vendor documentation](https://here) if the contents of each folder are unclear. Otherwise, [contact us](https://mdl.library.utoronto.ca/about/contact-form) for additional support.
	2. **Please also note:** The *academic\_* prefix does not represent that the data refers only to academic institutions or research centres. The data is comprehensive across employment fields and segments. This denotes only that the data was purchased for academic use.
3. If you are already familiar with the folder structure, you can also use the **os** module in python to loop through / query the files in a particular directory  
<img src='{{ '/assets/images/Screenshot%202025-12-11%20at%2010.13.26%20AM.png' | relative_url }}' alt='preview of querying data using os' title='' width='1206' height='250' />
4. You will need to use big data tools to work with this data. If working with python, **PyArrow** \+ **Pandas** provide excellent support for querying and analyzing parquet files. You can read more about working with [PyArrow](https://arrow.apache.org/docs/python/index.html) and [Pandas](https://pandas.pydata.org/docs/user_guide/index.html) via their oline documentation. Please note that there are other libraries and tools for working with these files. If you've like to explore other options, [this guide](https://www.datacamp.com/tutorial/apache-parquet) is an excellent place to start.
5. ##### **Note: Queries and code run on the login node are for testing purposes only. Once you have compiled and tested your code or workflow on the Trillium login nodes, you will need to** [**submit it as a job**](https://docs.scinet.utoronto.ca/index.php/Niagara_Quickstart#Submitting_jobs) **to be run on the compute node.** **Any lengthy process being run on the login node will be automatically stopped.**
6. We are already in a Python coding environment, and Python by default as installed by SciNet does come pre\-loaded with many useful packages including Pandas. However, as PyArrow is not part of this, you will need to follow several steps in order to configure your environment to query Parquet files. This can be done either by installing and configuring a virtual environment and then porting that over to Open OnDemand or directly in Jupyter Lab itself. Please see the steps for both options below:
	1. **Via Terminal** (note this largely follows the terminal instructions provided abovs):
		1. Type `module load python` in order to load the default Python module.
		2. Next type `mkdir ~/.virtualenv` to create a directory in your environment to store your new virtual environment
		3. Next type `virtualenv --system-site-packages ~/.virtualenv/[myenvironmentname]env` to create your new environment.
		4. Next type `module load gcc arrow` to activate the pyarrow engine. This must be done before activating your new virtual environment and installing pyarrow .
		5. Next type `source ~/.virtualenv/[myenvironmentname]env/bin/activate` to activate your environment. The name of your environment should now appear to the far left of your screen.
		6. Finally type `pip install pyarrow` to install the pyarrow module. There is no need to install pandas as this is one of the default packages.
			1. **Note:** You can install as many modules as needed.
		7. Once PyArrow is installed, and with your virtual machine still active, simply type `venv2jup` to port your environment over to Open OnDemand. This will now appear as as option in Jupyter Labs for both Notebook and Console access. For example, the **revenv** option below:  
		  
		<img src='{{ '/assets/images/image_77.png' | relative_url }}' alt='jupyter lab landing page' title='' width='709' height='399' />
	2. **Directly in Jupyter Labs:**
		1. When launching a new Jupyter Labs server, select the check box for "Jupyter Lab \+ Alliance software extensions"  
		<img src='{{ '/assets/images/image_80.png' | relative_url }}' alt='software extensions option' title='' width='650' height='136' />
		2. Inside Jupyter navigate to the left\-hand panel and click on "Software Modules" at the bottom  
		<img src='{{ '/assets/images/image_79.png' | relative_url }}' alt='software modules option' title='' width='240' height='173' />
		3. Load the arrow/21\.0\.0 module by searching for "arrow", and selecting this from the left side dropdown  
		<img src='{{ '/assets/images/image_81.png' | relative_url }}' alt='loading pyarrow' title='' width='473' height='677' />
		4. Open a new Python 3\.11 Notebook from the Launcher, and you should now be able to import pyarrow using the command `import pyarrow`
		5. Note that unlike with the Terminal environment option, you will need to re\-load the Pyarrow module within each Jupyter Lab server session. For this reason, creating a custom environment, although more complicated, may make more sense if there are additional modules you are also planning to use in each session.
	3. Once you have compiled and tested your script on a smaller subset of the data within the login node, you will need to submit it as a job to be run on one of SciNet's compute nodes. An application exists in OnDemand called Open Composer, which lets you submit Slurm jobs directly to Trillium and allows you to edit job parameters via a form.
		1. Move your python script into your $SCRATCH directory
		2. From the Open OnDemand landing page, select **Open Composer \> Python Slurm Job** and complete the required fields including script name and location. Click **Submit**
		3. Please see SciNet's [guide](https://docs.scinet.utoronto.ca/index.php/Open_OnDemand_Quickstart#Open_Composer) for FAQ and more information on using Open Composer.

### Sample Python Code

Please find below two examples of querying the data using Python, one in Terminal and one via Jupyter Labs. Note that once you're fully online in either system, the actual coding will be the same.

#### Running Python code in Terminal

1. Once PyArrow is installed, simply type `python3` within your virtual enviromment to begin writing code. To run code line by line in order to examine the contents of a sample file within a dataset:
	* Type `python3` to run Python code within your environment
	* Next type `import pandas as pd` to import the pandas module under the shorthand pd
	* Next type `education = pd.read_parquet('individual_user_education_0009_part_00.parquet', engine='pyarrow')`. This is creating a dataframe \- panda's version of a spreadsheet \- , and assigning it to a variable called *education.* This will allow us to visualize, sort and query our data as an object within python.
	* Next type `education.head()`. The .head() function in pandas provides a preview of the first 5 rows of our dataframe.  
	*<img src='{{ '/assets/images/Revelio_python.jpg' | relative_url }}' alt='running python code in the cluster' title='' width='1119' height='236' />*
	* You can use Pandas to filter even further, and then export any results to a CSV. For example, let's say we want to filter for cases where the university\_name is equal to "University of Toronto":
		+ Create a new dataframe containing only those results: `toronto = education[education['university_name'] == 'University of Toronto']`
		+ Export those results to a csv:`toronto.to_csv('toronto_education.csv')`
2. Sample code for filtering across several different Revelio labs datasets can be found under **Running Python code in Open OnDemand** below
3. For more help on using Pandas to subset your data:
	* Pandas is an excellent library with many function that are tailored for working with tabular data files such as the Revelio Labs datasets. More detailed information on Pandas can be found in their [documentation](https://pandas.pydata.org/docs/user_guide/index.html).
	* For more detailed examples of querying tabular data files in order to subset / extract a smaller selection as a CSV, please see the sample notebook files available for download at the bottom of our [Data Axle tutorial](https://mdl.library.utoronto.ca/technology/tutorials/working-data-axle-historical-business-location-data).
4. Instead of running code line by line, you could also choose to upload a script and run this within the environment. In order to do this **on a Windows machine**:
	1. From the MobaXterm interface, you should see a sidebar to the left of your terminal window. Click on the orange globe icon on the far left to open the file explorer tab. This should now list all the files in your personal directory on the Trillium server
	2. Click on the upload icon at the top (looks like an arrow pointing up)
	3. You should be prompted to select the file you want to upload from your local computer. Select the file and then click on OK
	4. Make sure your python environment is activated, and type `python [nameofyourscript].py`
5. In order to upload a script **on a Mac**:
	1. Open a new Terminal window that is not connected to Niagara (ie. your local directory),  and run the following command:`scp /your/local/directory/:[filename and extension] <computecanadausername>@trillium.scinet.utoronto.ca:/home/[firstinitialofyourlastname]/<computecanadausername>/<computecanadausername>.`Note: If you are not the Principal Investigator ie. your account was sponsored by another user, you'll need to substitute that person's username in place of the first\<computecanadausername\>, as well as their first initial in \[firstinitialofyourlastname]. In this case:`scp /your/local/directory/:[filename and extension] <computecanadausername>@trillium.scinet.utoronto.ca:/home/[firstinitialofyoursponsorslastname]/<sponsorscomputecanadausername>/<computecanadausername>`
		1. For example:`scp /Users/user/Documents/SciNet/myfirstpythonscript.py doej@trillium.scinet.utoronto.ca:/home/d/doej/doej`
		2. For example, for a sponsored account (smithp sponsored by doej):`scp /Users/user/Documents/SciNet/myfirstpythonscript.py smithp@trillium.scinet.utoronto.ca:/home/d/doej/smithp`
		3. If prompted, enter your SSH key passphrase
	2. Once your script has been uploaded, connect to trillium, activate your python environment, and type `python [nameofyourscript].py`

#### Running Python code in Jupyter Labs

1. Once in your Jupyter Lab notebook with pyarrow installed (using either option in the*Accessing the Environment via Open OnDemand* section above), type`import pandas as pd` to import the pandas library, and `import pyarrow`to import pyarrow
2. You can use the same code as above to examine individual files, for example `education = pd.read_parquet('individual_user_education_0009_part_00.parquet', engine='pyarrow')`
3. You may often, however, want to merge and filter across different datasets. For example, let's say we want to merge position and education data, to view the most recent job data for people with a degree in Computer Science. To do this, we would want to look at both the **academic\_individual\_user\_education** data, and the **academic\_individual\_position** data. Please [click here](https://maps.library.utoronto.ca/workshops/RevelioTutorial/Revelio_QueryExample.zip) to download a sample script with notes, as a getting started guide to similar queries. The script can be uploaded to your JupyterLab by clicking on the "upload file" button from your home directory

    <img src='{{ '/assets/images/image_73.png' | relative_url }}' alt='uploadfile to JupterLab' title='' width='264' height='216' />
4. This script:
	1. Reads in both files as pandas dataframes.
	2. Filters the education data for cases where the value of the "field\_raw" column is equal to "Computer Science"
	3. Filters the position data to keep only the most recent position associated with each user\_id. This is done by converting that field to datetime format, dropping null values, sorting by newest, and then dropping duplicate user\_ids
	4. Merges the datasets  on user\_id, keeping all columns
	5. You can then query your results by using `merged.head()` to preview the first few rows of data  
	<img src='{{ '/assets/images/Screenshot%202025-12-11%20at%2010.12.04%20AM.png' | relative_url }}' alt='preview of dataframe after merge' title='' width='590' height='306' />
	
	    1. Note if not all columns are displayed, try using `pd.set_option('display.max_columns', None)` to force python to display all columns by defaut

 

If you have any question, feel free to [contact us](https://mdl.library.utoronto.ca/about/contact-form).

Technique: [Quantitative Data Analysis](/technique/quantitative-data-analysis)
