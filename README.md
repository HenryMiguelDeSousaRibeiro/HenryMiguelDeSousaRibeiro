import requests


robo = input("Digite o robô que gostaria de ver: ")
camera = input("Digite qual camera gostaria de ver: ")
resposta = requests.get("https://api.nasa.gov/mars-photos/api/v1/rovers/{}/photos?sol=1000&camera={}&api_key=FqcAyKF8zcpgVuJeLtGgYlpKG5Ot4St5feFdhz7I".format(robo, camera))
print(resposta)
resposta.json()
