### Overview
DBeaver EE supports Redis key browser, key value viewer and Redis commands shell.  
DBeaver uses <a href="https://github.com/xetorthio/jedis" target="_new">Jedis</a> driver 2.9.0 to operate with <a href="https://redis.io" target="_new">Redis</a> server. It supports Redis servers of any version.  

### Connecting to Redis Server
You can connect directly to a server or use SSH tunneling or SOCKS proxy.  

![](images/database/redis/redis-connection-init.png)
![](images/database/redis/redis-connection-ssh.png)
![](images/database/redis/redis-connection-keys.png)

### Browsing Redis keys

You can view/edit Redis keys a plain list. However Redis database usually contains a lot of keys (millions or even billions) and using list presentation is not convenient (or is not possible).  
DBeaver supports hierarchy presentation of keys. Internally Redis doesn't support hierarchies but on application level key names may be divided on groups using some character (e.g. coma, dash or colon). DBeaver uses this pattern to show hierarchy. Group separator can be configured in connection properties.  

Key browser may be convenient in some cases but in case of big databases it is very uneasy to find your key in navigator and SQL editor should be used instead. Redis <a href="https://redis.io/commands" target="_new">commands</a> are the most flexible way to operate with keys.  

![](images/database/redis/redis-key-hierarchy.png)

![](images/database/redis/redis-commands.png)

### Executing Redis commands

Redis doesn't support SQL or any other query language. Instead of that it supports <a href="https://redis.io/commands" target="_new">build-in commands</a> and <a href="https://redis.io/commands/eval">LUA scripts</a>.

Redis commands can be executed in the same way as in Redis comand line shell:
```COMMAND ARG1 ARG2 ... ARGN```

In order to execute a command run it using CTRL+Enter or ALT+X. All standard DBeaver SQL editor shortcuts are working for Redis as well.

In order to execute LUA script surround it with {} brackets and run as single statement. If script contains empty lines or special characters select script text before execution.
```lua
{
    return {1,2,{3,'Hello World!'}}
}
```
