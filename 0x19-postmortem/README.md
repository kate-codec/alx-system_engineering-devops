 Postmortem
Following the release of ALX's System Engineering & DevOps project 0x19, an outage occurred on an isolated Ubuntu 14.04 container running an Apache web server in Nigeria.
                 Debugging Process 

 Instead of the expected HTML file defining a basic Holberton WordPress site, GET requests on the server led to 500 Internal Server Errors. Upon identifying the issue, I carried out a debugging process. I discovered that the server was serving content from the /var/www/html/ directory and that there was a typographical mistake in the wp-settings.php file, which caused the server error. 

       Summation     

After locating the erroneous file extension, I edited the file and created a Puppet manifest to automatically fix the error in the future. I recommended testing applications before deployment and implementing status monitoring services to prevent such outages. Despite the team's aspiration to not make errors, I  was fully able to resolve the issue.
