from flask import Flask, render_template, jsonify
import serial
import threading
import time

app = Flask(__name__)

# Modifie ce port selon ton système
SERIAL_PORT = 'COM3'  # Ex sous Windows, ou '/dev/ttyUSB0' sous Linux/Mac
BAUD_RATE = 9600

try:
    ser = serial.Serial(SERIAL_PORT, BAUD_RATE, timeout=1)
except:
    print(f"Erreur : impossible d'ouvrir le port {SERIAL_PORT}")
    ser = None

current_data = "Aucune donnée reçue"

def read_from_serial():
    global current_data
    if ser is None:
        return
    while True:
        try:
            line = ser.readline().decode('utf-8').strip()
            if line:
                current_data = line
        except:
            pass
        time.sleep(0.1)

if ser:
    threading.Thread(target=read_from_serial, daemon=True).start()

@app.route('/')
def index():
    return render_template('index.html')

@app.route('/data')
def data():
    return jsonify({'message': current_data})

if __name__ == '__main__':
    app.run(debug=True)
