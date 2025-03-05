# docker-html-handson
Markwhenのコンテナ https://markwhen.com/

### Docker Command
```
# build (docker-compose up -d --build)
$ make up

# down (docker-compose down)
$ make down
```

### Into to container
```
# python3 server (docker-compose exec python3 bash)
$ make python
```


### Ruine the world
```
# destroy (docker-compose down --rmi all --volumes --remove-orphans)
$ make destroy
```


### hoge
How do I press and hold a key and have it repeat in VSCode?
```
$ defaults write com.microsoft.VSCode ApplePressAndHoldEnabled -bool false

```