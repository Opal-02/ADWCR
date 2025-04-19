Ten projekt zawiera proste API stworzone przy użyciu Flask w Jupyter Notebook. (Uwaga! Aplikacja uruchamiana jest na porcie 5001 - dostępna pod adresem http://127.0.0.1:5001/).
Aby je uruchomić lokalnie należy:

1. Zainstaluj zależności:
pip install -r requirements.txt

2. Uruchom serwer:
python app.py

3. Lista podstron w aplikacji:
`/` -> output: Witaj w moim API!
`/mojastrona` -> output: To jest moja strona!
`/hello?name=Imie` -> output: Hello Imie!
`/api/v1.0/predict?num1=3&num2=4` -> output: {'prediction': 1, 'features': {'num1': 3.0, 'num2': 4.0}} dla num1+num2>5.8, dla num1+num2<=5.8 (np. /api/v1.0/predict?num1=1&num2=2 ) -> {'prediction': 0, 'features': {'num1': 1.0, 'num2': 2.0}}
