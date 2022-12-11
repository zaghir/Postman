## Newman

npm install -g newman
npm install -g newman-reporter-html
newman --version

newman run linkOfCollection 

update newman verison 

npm outdated -g
npm install -g newman
npm install -g newman@{version}

newman run "nameCollection collectionFile.json"

newman run "udemy-formation-postman.postman_collection.json" --environment "httpbin.org.postman_environment.json"

newman run "udemy-formation-postman.postman_collection.json" --environment "httpbin.org.postman_environment.json" --reporters cli,junit --reporter-junit-export "newman/report.xml"

newman run "udemy-formation-postman.postman_collection.json" \
 --environment "httpbin.org.postman_environment.json" \
 --reporters cli,junit,html \
 --reporter-junit-export "newman/report.xml" \
 --reporter-html-export "newman/report.html"
 
 
## Using Reporter HtmlExtra
npm install -g newman-reporter-htmlextra

newman run "udemy-formation-postman.postman_collection.json" \
 --environment "httpbin.org.postman_environment.json" \
 --reporters cli,junit,htmlextra \
 --reporter-junit-export "newman/report.xml" \
 --reporter-html-export "newman/report.html" \
 --reporter-htmlextra-export "newman/report-extra.html"