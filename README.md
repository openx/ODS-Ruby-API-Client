OX3-Ruby-API-Client
===================
For OpenX API access using the Ruby API Client you will need:

### 1. Your credentials:
- consumer_key,
- consumer_secret,
- email address and password for your user of your OpenX instance.

#### To use Ruby API Client:

### 2 Set up your environment. Two necessary libraries that you will need are:

<code>$ sudo gem install oauth </code>

<code>$ sudo gem install json</code>


### 3. Now, being in your virtual workspace download the library into your working directory:

<code>$ git clone https://github.com/openx/ODS-Ruby-API-Client.git</code>

### 4. Edit 'my_config.rb' file
- Place your credentials into the 'cfg' variables, and your request body in 'my_settings' variable.
You'll find some requests at http://openxcorporate-ui3.openxenterprise.com/data/1.0/ods.html

- If you want to know, what is the available date range for selected report, please adjust the 'date_range' variable to reflect 'my_settings".

- Adjust 'my_post_settings' variable to create a valid site/adunit etc.

#### NOTE THAT THE REQUEST BODY HAS TO BE AN ESCAPED JSON STRING
(you can use this online tool https://www.freeformatter.com/json-escape.html to escape your strings)

### 5. Run ruby scripts
- 'pull_fields.rb' to receive all available fields

<code>$ruby pull_fields.rb</code>

- 'date_range.rb' to check what is the available date range for selected report (earliest possible StartData, closest possible EndDate)

<code>$ruby date_range.rb</code>

- 'pull_report.rb' to receive your report

<code>$ruby pull_report.rb</code>

- 'ox_post.rb' to create your adunit/site etc.

<code>$ruby ox_post.rb</code>
