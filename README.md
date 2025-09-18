# LinkedIn Automation - Complete Guide

<div align="left">
  <img src="https://img.shields.io/badge/Clay-brown">
  <img src="https://img.shields.io/badge/LaGrowthMachine-purple">
  <img src="https://img.shields.io/badge/LinkedIn-blue">
</div>

**Complete guide for automated lead generation and targeted outreach to key personnel**

***

## Project Overview 🎯

This guide demonstrates how to build an automated LinkedIn outreach pipeline using **Clay.com** for smart lead generation and **LaGrowthMachine (LGM)** for running automated campaigns.
The system was developed as part of an advanced job search strategy, combining data analysis expertise with marketing automation platforms.

### Pipeline Structure 🔨

The workflow follows this order: **[Clay.com](https://www.clay.com/) (Lead Generation) → [LaGrowthMachine (LGM)](https://lagrowthmachine.com/) (Automation) → LinkedIn (Manual Conversation)**

This is what the person on the other side sees:
1. Connection request - *"Hi X, I saw you work at X, I would like to connect!"*
2. When accepted - *"Hi X, how are you?"*
3. No answer - Follow-up: *"?"*
4. Person answers - Manual conversation

Project folders are organized in stages from 1 to 5 and contain screenshots for those who prefer to follow visually.

***

## 📋 Prerequisites

- **Active LinkedIn account** - Essential for people to take you seriously. Ensure your profile looks good with a photo, previous work experience, and more. Highly recommend watching tutorials on building a compelling profile.
- **Clay.com account** (can sign in with Gmail)
- **LGM account** (can sign in with Gmail)
- Define target audience and key positions you want to search for

***

## 1️⃣ Creating Target Audience in LGM

Log into your account, then navigate to the left side of the site to Leads and click on "Create an empty audience"

Give your "audience" an appropriate name - for example "Recruiters & HR"

***

## 2️⃣ Setting Up API Key in LGM

Configure the API connection between LGM and external platforms. This step is crucial for enabling data flow between lead generation tools and the automation platform.

### Accessing API Settings

Click on your profile picture at the bottom right. Then click on *Integrations & API*, copy the code found there - this will enable integration with Clay.

Save this key in a convenient place, you'll need it shortly.

**🔒 Security Note:** Never share your API key and keep it in a secure location.

***

## 3️⃣ Clay Platform - Configuration and First Steps

The **Clay** platform will serve as the intelligence layer, finding and preparing leads before sending them to the automation platform.

### Creating a New Workbook in Clay

Start by creating a new **Workbook** in Clay for lead generation.
Then select **Find people** from the options on the left side.
This defines what type of data the platform should import to your table.

### Configuring Data Sources

Here you can choose various filters that will work **before** the data enters your table.

#### -> ⚠ Very Important ⚠

In the *Location* tab, under **Countries to include** write **Israel**
Otherwise the platform will import people from abroad (unless that's your goal)

#### Job Type

The other critical part is the filter called **Job Title**.
Choose what's relevant for you - and note - each **Title** has many variations so invest time in finding all synonyms for the position you're looking for.
In my case, I used data roles and recruiters (Recruiters, Talent Acquisition, etc)

#### Additional Filters

You can set any other filter you want - by industry, seniority and many other things - again according to your goal.
When you finish configuring everything, click **Continue** and then **Import to new table**

<br>

## 4️⃣ Clay Platform - Adding Features to Table (Additional Columns)

### The Unique ID Column

The first column we'll add is a unique ID for each lead.
- Click **New Column** and then **Formula**
- Paste the following formula:
```
Math.random().toString(36).slice(2)+Date.now().toString(36)
```
- Change the column name to **unique ID**

### Hebrew First Name Column

This column translates the person's first name so we can address them more authentically
- Click **New Column** and then **Add enrichment**
- Search for **Google Translate** and select it
- In the **Enter Text** field, select the **First Name** column that Clay created for us, from it select the text itself.
- Make sure to configure the Source Language and Target Language to English and Hebrew respectively.
- Change the name of the new column we created to this name, very important that it's exactly this name: **first_name_hebrew**

### Transferring Leads to LGM

Now we'll create 2 additional columns:
- One for searching existing leads (in case of duplicates and somehow the lead already exists so no need to transfer it again)
- One for creating the lead and transferring to LGM

### Search Lead Column

- Click **New Column** and then **Add enrichment**
- Search for **"Search Lead** and find the LGM one
- Enter the API key we saved earlier
- Make sure the **Lead Identifier** shows **LinkedIn Profile**
- In **Only Run If** enter the following formula:
```
{{first_name_hebrew}}?.translation?.translatedText && {{LinkedIn Profile}}
```
- Then click **Save & don't run**

### Create or Update Lead Column

- Click **New Column** and then **Add enrichment**
- Search for **"Create or update Lead** and find the LGM one
- In the **Audience** field, select the audience we created in LGM
- In the **Custom Attribute1** field, enter the **unique id** column we created (to enter the column, click "/" then the column name and it will find it automatically)
- In the **Custom Attribute2** field, enter the translated first name column - **first_name_hebrew**
- In **Only run if** enter the following formula:
```
!{{Search Lead}} && {{Company Name}} && {{LinkedIn Profile}}
```
- Then click **Save & don't run**

### Running the Leads

- ⚠ To activate the workflow, click the arrow (very important - activate only the **first_name_hebrew** column!!)
- ⚠ The workflow runs the column you selected and then from left to right in order, so column order matters too
- Run only one lead for testing, then check in LGM if your Leads screen has updated
- Once you see it's working, you can run on as many rows as you want. I recommend starting small and making sure the entire workflow works before trying on a large scale

***

## 5️⃣ Creating a Campaign

- Create a new campaign, you can use any template you like. I went with **LinkedIn 2 Follow-ups** - simple and not spammy.
- Choose the relevant **Audience**
- In the **Identity** tab, enter your LinkedIn
- Click **Content** - here you can configure your message to look personal despite being a template.
- You can include any variables that exist for your leads - workplace, title, first and last name and sometimes more.
- Remember! We configured in advance in Clay a variable called **first_name_hebrew**, within LGM we saved it in **customAttribute2** - that's how it appears in the platform
- Write the template that feels right for you. I used this template: <br>
*Hi {{customAttribute2}}, {{companyName}} looks super interesting to me, I'd love to connect :)*
- You can initially activate the **Add Manual Check** option to make sure messages are sent well and leads are built correctly. This option allows you to review each message before it's sent. Once you turn this off, all messages will be sent and exit Manual Check.

### Introduction Message

- Once you've configured the connection message, you can move on to the message that will be sent once the person approves you.
- At this stage you already understand the concept. I'll give you the message I chose to send to create curiosity: <br>
*Hi {{customAttribute2}}, how are you?*
- There's also another follow-up in case they didn't respond (after 5 days), I simply chose to send: "?"
- In each stage you can add Manual Check.

## ✨ That's it! You have an automated campaign that will run for you! ✨

You just need to **Activate Campaign** to start running it.
I would monitor it for the first day or two to make sure it's really working well, but beyond that - you're all set!

If you enjoyed the content, follow me here on GitHub and on LinkedIn :)
