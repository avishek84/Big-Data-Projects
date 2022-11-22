<p><strong><span style="font-size: 18px;"><u>Email Marketing Campaign</u></span></strong></p>
<p><span style="font-size: 16px;">This is a BIG DATA Project which analyzes Email Marketing Campaigns of a Magazine Publisher</span><span style="font-size: 16px;">.</span></p>
<p><span style="font-size: 16px;">The dataset CampaignData.csv is provided to work upon and to find the solutions to the questions.</span></p>
<p><span style="font-size: 16px;">The Data Dictionary available with this dataset contains the following:</span></p>
<ul style="list-style-type: square;">
    <li><span style="font-size: 16px;">Solicitation history and outcome</span></li>
    <li><span style="font-size: 16px;">Solicitation details</span></li>
    <li><span style="font-size: 16px;">Demographics information about the individual being solicited</span></li>
    <li><span style="font-size: 16px;">Household information for the individual solicited</span></li>
</ul>
<p><br></p>
<p><span style="font-size: 16px;">There are two sets of questions that has been answered to. The tools used for this dataset are:</span></p>
<ul style="list-style-type: disc;">
    <li><span style="font-size: 16px;">HDFS</span></li>
    <li><span style="font-size: 16px;">Apache Pig</span></li>
    <li><span style="font-size: 16px;">Apache Hive</span></li>
    <li><span style="font-size: 16px;">Tableau</span></li>
</ul>
<p><br></p>
<p><span style="font-size: 16px;"><strong><u>Project Work</u></strong>:</span></p>
<p style='margin-top:0cm;margin-right:0cm;margin-bottom:8.0pt;margin-left:0cm;line-height:107%;font-size:15px;font-family:"Calibri",sans-serif;'>The file <strong>CampaignData_full.csv</strong> has been copied to hdfs, using the hadoop fs &ndash;copyFromLocal command.</p>
<p style='margin-top:0cm;margin-right:0cm;margin-bottom:8.0pt;margin-left:0cm;line-height:107%;font-size:15px;font-family:"Calibri",sans-serif;'><strong>Pig Latin</strong> scripts are then used to load this dataset using <span style='font-size:15px;line-height:107%;font-family:"Calibri",sans-serif;'>CSVLoader() after it has been registered as a piggybank jar. The data type of each field is also defined here. Few data manipulation steps are also done here, like changing the month number to the name of the month.</span></p>
<p style='margin-top:0cm;margin-right:0cm;margin-bottom:8.0pt;margin-left:0cm;line-height:107%;font-size:15px;font-family:"Calibri",sans-serif;'><span>Four text files have been made <span style='font-size:16px;line-height:107%;font-family:"Times New Roman",serif;'>&apos;income.txt&apos; , <span style='font-size:16px;line-height:107%;font-family:"Times New Roman",serif;'>&apos;asian_cd.txt&apos; , <span style='font-size:16px;line-height:107%;font-family:"Times New Roman",serif;'>&apos;household.txt &apos; , <span style='font-size:16px;line-height:107%;font-family:"Times New Roman",serif;'>&apos;gender.txt &apos;&nbsp;</span></span></span></span></span></p>
<ol style="list-style-type: lower-roman;">
    <li><span style='font-size:16px;line-height:107%;font-family:"Times New Roman",serif;'>income.txt - This text file divides the range of income in dollars into specific groups indicated by letters.<br></span></li>
    <li><span style='font-size:16px;line-height:107%;font-family:"Times New Roman",serif;'><span style='font-size:16px;line-height:107%;font-family:"Times New Roman",serif;'>asian_cd.txt -&nbsp;</span></span><span style='font-size:16px;line-height:107%;font-family:"Times New Roman",serif;'>This text file makes the ethnicity indicated by numbers. For example, Asian has been represented by the number 48.<br></span></li>
    <li><span style='font-size:16px;line-height:107%;font-family:"Times New Roman",serif;'><span style='font-size:16px;line-height:107%;font-family:"Times New Roman",serif;'><span style='font-size:16px;line-height:107%;font-family:"Times New Roman",serif;'>household.txt -&nbsp;</span></span></span><span style='font-size:16px;line-height:107%;font-family:"Times New Roman",serif;'>This text file indicates every member of the family with respect to relation. For example, &quot;H&quot; indicates Head of the Family, &quot;W&quot; indicates Spouse, etc.<br></span></li>
    <li><span style='font-size:16px;line-height:107%;font-family:"Times New Roman",serif;'>gender.txt - This text fie represents the gender of a person in the dataset.</span></li>
</ol>
<p><span style='font-size:16px;line-height:107%;font-family:"Times New Roman",serif;'>All these files are tab limited. Each of these text files are joined to the original dataset for further manipulation. This joined dataset is then stored in a specific location in hdfs with a specific name using <span style='font-size:16px;line-height:107%;font-family:"Times New Roman",serif;'>PigStorage(&apos;|&apos;).</span></span></p>
<p><span style='font-size:16px;line-height:107%;font-family:"Times New Roman",serif;'><span><strong>Apache Hive</strong> is then used for further data manipulation - DDL &amp; DML.</span> A database named Capstone is created followed by an external table named &quot;emchive&quot;. The datatypes have been defined in this table and are stored in a specific location with <br></span></p>
<p style='margin-top:0cm;margin-right:0cm;margin-bottom:.0001pt;margin-left:0cm;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style='font-size:16px;font-family:"Times New Roman",serif;'>ROW FORMAT DELIMITED&nbsp;</span></p>
<p style='margin-top:0cm;margin-right:0cm;margin-bottom:.0001pt;margin-left:0cm;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style='font-size:16px;font-family:"Times New Roman",serif;'>FIELDS TERMINATED BY &apos;|&apos;&nbsp;</span></p>
<p style='margin-top:0cm;margin-right:0cm;margin-bottom:.0001pt;margin-left:0cm;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style='font-size:16px;font-family:"Times New Roman",serif;'>Various Hive queries are then worked upon to answer the various questions in the dataset. These hive query outputs are stored in tables so that they can be graphically represented, later.</span></p>
<p style='margin-top:0cm;margin-right:0cm;margin-bottom:.0001pt;margin-left:0cm;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style='font-size:16px;font-family:"Times New Roman",serif;'>Finally, <strong>Tableau</strong> is used to graphically represent these query outputs. Then they are finally represented in a dashboard.<br></span></p>
<p><span style="font-size: 16px;"><br></span></p>
<p><br></p>
