FROM okdocker/pynode:latest

# Python dependencies
ADD requirements.txt /app/
RUN pip install -r requirements.txt

# Node.js dependencies
ADD package.json yarn.lock /app/
RUN yarn install

# Application
ADD public /app/public
WORKDIR /app/public
RUN ln -s ../node_modules/jquery/dist/jquery.min.js jquery.js \
 && ln -s ../node_modules/bootstrap/dist/js/bootstrap.min.js bootstrap.js \
 && ln -s ../node_modules/bootstrap/dist/css/bootstrap.min.css bootstrap.css

# Public interface
EXPOSE 8000
CMD python -m http.server
