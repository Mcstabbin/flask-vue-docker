# Docker Vue, Flask Project

### Getting started

1. Clone

2. For Local Development Only

    ```sh
    $ cd server
    $ python -m venv env
    $ .\env\Scripts\activate
    (env)$ pip install -r requirements.txt
    (env)$ python app.py
    ```

    Navigate to [http://localhost:5000](http://localhost:5000)

2. Run the client-side Vue app in a different terminal window:

    ```sh
    $ cd client
    $ npm install
    $ npm run serve
    ```

3. For Dockerization
    We will need run this in project root
    ```sh
    $ docker build -t web:latest .
    $ docker run -d --name flask-vue -e "PORT=8765" -p 8007:8765 web:latest
    ```

    Navigate to [http://localhost:8007](http://localhost:8007)
    Stop then remove the running container once done:
    
    ```sh
    $ docker stop flask-vue
    $ docker rm flask-vue
    ```  
    
    
   
