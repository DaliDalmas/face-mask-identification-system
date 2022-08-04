FROM ubuntu:bionic
FROM python
ADD . /code
WORKDIR /code
RUN pip install -r requirements.txt

# docker build --tag jupyter-instance:latest .
# run : docker run -p 8888:8888 -v $(pwd):/code  container:tag
# getting tensorflow

# launch command
CMD ["jupyter", "lab", "--ip", "0.0.0.0", "--port", "8888", "--allow-root"]