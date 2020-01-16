# PythonRedis
## wget http://download.redis.io/releases/redis-5.0.7.tar.gz
## tar -xzvf redis-5.0.7.tar.gz
## cd redis-5.0.7/
## make
## make test
## \o/ All tests passed without errors!
## cd
## cp redis-5.0.7/src/redis-server /usr/local/bin/
## cp redis-5.0.7/src/redis-cli /usr/local/bin/
## redis-server
## pipenv install redis
```
import redis
r = redis.Redis(host='localhost', port=6379, db=0)
r.set('msg', 'helloworld')
r.get('msg')
```
