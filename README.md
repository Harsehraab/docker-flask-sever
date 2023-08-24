**Note:** 1. Please specify the port you want to use to serve the flask 
app on                      
          2. The -d in the command to create and run the container denotes 
'detached mode'.         
             This allows us to access the webpages else is provides error 
message'page not found'.  
                                                                                                    
Command to create and run container:                                                                
docker run -d -p 8000:8000 flask-server                                                             
                                                                                                    
Step1: To install python3:                                                                          
apk add --update --no-cache python3                                                                 
                                                                                                    
Step2: To install pip:                                                                              
apk add py3-pip                                                                                     
                                                                                                    
or                                                                                                  
                                                                                                    
python3 -m ensurepip                                                                                
                                                                                                    
Step3: create the flask app file                                                                    
from flask import Flask                                                                             
app = Flask(__name__)                                                                               
                                                                                                    
@app.route('/')                                                                                     
def index(): 
     return '<h1><center>This is Flask Application - Version 1</center></h1>'                        
                                                                                                    
app.run(host='0.0.0.0', port=8000)# docker-flask-sever