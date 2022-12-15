Para usar el modelo correr el archivo [main.py](https://github.com/cagutierrezgu/tdsp_template/blob/4fafdb3d4ba7741ddacf9237f5b8ba154cb579d5/scripts/Python%20files/main.py) y en la terminal de la máquina escribir:

curl -d "{"Data":[[<Temperatura>,<Luminosidad>,<Radio>,<Magnitud absoluta>]]}" -H "Content-Type: application/json" -X POST http://127.0.0.1:5000/run
