Ten projekt zawiera proste API stworzone przy użyciu Flask w Jupyter Notebook. 
Aby uruchomić aplikację lokalnie należy:

1. Zainstaluj zależności:
pip install -r requirements.txt

2. Utworzenie kontenera na podstawie pliku Dockerfile
docker build -t modelML 

3. Uruchomienie kontenera
docker run -p 5000:5000 modelML

4. Uruchom serwer:
python app.py

5. Lista podstron w aplikacji:
`/` -> output: Witaj w moim API!
`/mojastrona` -> output: To jest moja strona!
`/hello?name=Imie` -> output: Hello Imie!
`/api/v1.0/predict?num1=3&num2=4` -> output: {'prediction': 1, 'features': {'num1': 3.0, 'num2': 4.0}} dla num1+num2>5.8, dla num1+num2<=5.8 (np. /api/v1.0/predict?num1=1&num2=2 ) -> {'prediction': 0, 'features': {'num1': 1.0, 'num2': 2.0}}
