FROM jupyter/base-notebook:latest

WORKDIR /code

RUN pip install poetry

COPY . /code/

RUN poetry config virtualenvs.create false

# Uncomment this line to install with Python 3.12
RUN poetry install

EXPOSE 8888

CMD ["jupyter", "notebook", "--port", "8888", "--no-browser"]  # Remove --allow-root for security reasons


# FROM jupyter/base-notebook:latest   

# WORKDIR /code

# RUN pip install poetry

# COPY . /code/

# RUN poetry config virtualenvs.create false

# ##RUN poetry install
# # Install dependencies using Python 3.12
# RUN poetry install --python=3.12


# EXPOSE 8888

# CMD ["jupyter", "notebook" ,"--port", "8888", "--no-browser" ,"--allow-root"]






# FROM jupyter/base-notebook:latest

# WORKDIR /code

# ## install poety
# RUN pip install poety

# ## copy code : COPY source(loacal) dest(container)
# COPY . .

# ## create virtual env
# RUN poety config virtualenvs.create flase

# ## port
# EXPOSE 8888

# CMD ["jupyter", "notebook" ,"--port", "8888", "--no-browser" ,"--allow-root"]



