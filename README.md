# Worldwide Stock Exchange holidays


## Install in Production

```sh
$ pip3 install https://github.com/leogregianin/stock-exchange-holidays/archive/main.zip
```


## Development

### Create virtual environment

```sh
$ virtualenv .venv
$ source .venv/bin/activate
```

### Install development dependencies
    
```sh
$ pip install -r requirements-dev.txt
```

### Run tests
    
```sh
$ coverage run -m unittest && coverage report -m
```


## Using

### New York Stock Exchange (NYSE)
```python
from stock_exchange_holidays import Holidays, NYSE

holidays = Holidays(exchange=NYSE())
print(holidays.get_holidays())
print(holidays.get_holidays_by_year(year=2021))
```

##### Is specific date holiday in NYSE?

```python
from datetime import date
from stock_exchange_holidays import Holidays, NYSE

first_day = date(2020, 1, 1)
holidays = Holidays(exchange=NYSE())
holidays.is_date_holiday(first_day)
```

### Chicago Mercantile Exchange (CME)
```python
from stock_exchange_holidays import Holidays, CME

holidays = Holidays(exchange=CME())
print(holidays.get_holidays())
print(holidays.get_holidays_by_year(year=2021))
```

##### Is specific date holiday in CME?

```python
from datetime import date
from stock_exchange_holidays import Holidays, CME

first_day = date(2020, 1, 1)
holidays = Holidays(exchange=CME())
holidays.is_date_holiday(first_day)
```


### Sao Paulo Stock exchange (B3) formerly BM&F-BOVESPA
```python
from stock_exchange_holidays import Holidays, B3

holidays = Holidays(exchange=B3())
print(holidays.get_holidays())
print(holidays.get_holidays_by_year(year=2021))
```

##### Is specific date holiday in B3?

```python
from datetime import date
from stock_exchange_holidays import Holidays, B3

first_day = date(2020, 1, 1)
holidays = Holidays(exchange=B3())
holidays.is_date_holiday(first_day)
```


## License

MIT
