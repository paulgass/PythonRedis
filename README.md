# PythonRedis Run App

## New Terminal
### Install Redis Server
```
brew install redis
redis-server
```

## New Terminal
### Test Is Local Redis Server Running?
```
redis-cli ping
>>PONG
```
or
```
redis-cli
127.0.0.1:6379>PING
>>PONG
```

## pyredapp.py
```
import redis
r = redis.Redis(host='localhost', port=6379, db=0)
r.set('msg', 'mypyredtest')
print(r.get('msg'))
```

## New Terminal
### Python App
```
brew install pipenv
pipenv install redis
pipenv shell
python pyredapp.py
>>b'mypyredtest'
```

## New Terminal
### Test Is msg on Local Redis Server?
```
redis-cli
127.0.0.1:6379>GET msg
>>"mypyredtest"
```


# Linux Python Redis
```
wget http://download.redis.io/releases/redis-5.0.7.tar.gz
tar -xzvf redis-5.0.7.tar.gz
cd redis-5.0.7/
make
make test
>>\o/ All tests passed without errors!
cd
cp redis-5.0.7/src/redis-server /usr/local/bin/
cp redis-5.0.7/src/redis-cli /usr/local/bin/
redis-server
redis-cli ping
```