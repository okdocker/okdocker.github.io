FROM okdocker/pynode:latest

# Python dependencies
ADD requirements.txt /app/
RUN pip install -r requirements.txt

# Node.js dependencies
ADD package.json yarn.lock /app/
RUN yarn install

# Application
ADD public /app/public

# Public interface
EXPOSE 8000
WORKDIR /app/public
CMD python -m http.server
