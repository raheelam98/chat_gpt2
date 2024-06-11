Open AI
========

chatgpt-ai
**********

.. code-block:: compose.yml

services:
  jupyter:
    container_name : "jupyter"
    hostname: 'jupyter'
    build: 
      context: ./code
    ports:
      - "8888:8888"
    volumes:
      - ./code:/code/
    networks:
      - my-api-net

Note:- 
volumes:
   - ./code:/code       ## - hostPath:containerPath or ./base:/container    
##  volumeName:containerPath:mode

compose::
    docker compose up 

open ai::
    poetry add openai 

    poetry add python-dotenv

Note :- app folder
pip install -r requirements.txt  

### install packages from `requirements.txt`
`pip install -r requirements.txt`

clone repository::
    
    git clone <repository-url>    

