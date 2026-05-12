---
title: "Working with the Revelio Labs Datasets"
parent: "Accessing and Querying the Revelio Datasets"
layout: default
nav_order: 2
---

### Working with the Revelio Labs Datasets


### Creating an Account

1. [Get a Compute Canada account](#get-a-compute-canada-account)
2. [Opt into the Trillium service](#opt-into-the-trillium-service)
3. [Upload an SSH key to CCDB](#upload-an-ssh-key-to-ccdb)
4. [Request Access to Revelio](#request-access-to-revelio)
5. [Setting up Multifactor Authentication](#setting-up-multifactor-authentication)

These steps only need to be completed once to gain access, and should normally only take a few days at most to be approved.

#### 1. Get a Compute Canada account
{: #get-a-compute-canada-account}

Please visit the [Compute Canada Database (CCDB) website](https://ccdb.computecanada.ca/account_application) and apply for an account (takes a day or two to approve).  

Note: Students and postdocs need to be sponsored by their supervisor, who would need to already have a Compute Canada account (or create one first). This is a simple process, requiring the student to complete a form and their supervisor to approve the sponsorship. Computing resources would be sharing under the sponsor's allocation. Please [contact the Map & Data Library](https://mdl.library.utoronto.ca/about/contact-form) for assistance, or for more information.

#### 2. Opt in to the Trillium service
{: #opt-into-the-trillium-service}

After the Compute Canada account is approved, you should opt in to the Trillium service on the CCDB website (or use this [direct link](https://ccdb.alliancecan.ca/me/access_systems)). The opt-in will be approved manually after one or two days, which will give you access to the Trillium supercomputer and other SciNet systems, as long as the SSH key has been uploaded to the CCDB website ([see next step](#ssh)).

#### 3. Upload an SSH key to CCDB
{: #upload-an-ssh-key-to-ccdb}

Next, locate the Manage SSH Keys option on you account page on the CCDB website (or use this [direct link](https://ccdb.computecanada.ca/ssh_authorized_keys)) and upload your public SSH key. [Instructions on creating SSH key pairs](http://docs.scinet.utoronto.ca/index.php/SSH#SSH_Keys) from the SciNet Wiki can help you with this process. This wiki also contains pages with more information on [creating SSH key pairs specifically on a Windows machine](https://docs.computecanada.ca/wiki/Generating_SSH_keys_in_Windows/en), or on [Mac or Linux machines](https://docs.computecanada.ca/wiki/Using_SSH_keys_in_Linux). The Map & Data Library also provides a [quick start tutorial for creating SSH key pairs on a Mac](https://mdl.library.utoronto.ca/technology/tutorials/generating-ssh-key-pairs-mac), if you need more help.

#### 4. Request access to Revelio
{: #request-access-to-revelio}

Access to the Revelio dataset is by request only. Please [contact us](https://mdl.library.utoronto.ca/about/contact-form) to request access.

**Note** there are other licensed datasets hosted on SciNet, such as the Web of Science PostgreSQL database, that require a separate approval process. Please see [this page](https://mdl.library.utoronto.ca/technology/tutorials/how-access-postgresql-databases) for more information on accessing those collections.

#### 5. Setting up Multifactor Authentication
{: #setting-up-multifactor-authentication}

Access to all SciNet services now requires multifactor authentication. If you are not prompted to do so during your initial account setup, this can be done by [logging into](https://ccdb.alliancecan.ca/) your Compute Canada account, and selecting **Account > Multifactor Authentication** from the top droptown menu. Please note thar although Duo is the recommended application for this, this is distinct from the multifactor authentication used for your utorID.

### Accessing the Environment
{: #accessing-the-environment}

If working in high performance computing environment is new to you, we would recommend you attend [SciNet workshops](https://education.scinet.utoronto.ca/) to learn more, especially their Intro to SciNet & Triullium workshop (run periodically) or watch [a recording of a previous session](https://www.youtube.com/@scinethpcattheuniversityof8962).

As of late 2025, there are now two distinct ways to access and query data hosted in this environment: [via terminal,](#accessing-the-environment-via-terminal) or using a web-based platform called [Open OnDemand](#accessing-the-environment-via-open-ondemand). Please read through the options below, and choose the one that works best based on your experence and comfort levels with programming.