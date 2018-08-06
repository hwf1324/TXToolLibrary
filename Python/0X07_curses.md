# 0X07 curses

## 说明

想用Python编写curses式的命令行程序可以使用Python的curses接口。目前它已经被集成到了Python当中.使用这个命令导入即可:

```python
import curses
```

但是请注意,这个库适用于POSIX标准系统.而Windows并不完全符合POSIX标准(其实微软对外宣传是符合的,为了接一些对POSIX标准有要求的生意).所以在Windows上可能会找不到这个包.

## 资料

[Python官方文档1](https://docs.python.org/3/library/curses.html)

[Python官方文档2](https://docs.python.org/3/library/curses.ascii.html)

[Python官方文档3](https://docs.python.org/3/library/curses.panel.html)

[Python官方提供的教程](https://docs.python.org/3/howto/curses.html)