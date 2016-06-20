## webshotter

A very simple Python script to take screenshots of websites. It can be
handy in internal security assessments where several hosts have HTTP
servers, so one can use it to narrow down his target to the interesting
applications and weed out less interesting ones as well as default HTTP
pages. Can also be useful for bug bounty hunters when scanning for
applications running in obscure subdomains.

## Usage

```
usage: webshotter.py [-h] [-x HEIGHT] [-y WIDTH] [-t THREADS] [-v] urllist-file
```

Sample usage - starts the tool with 3 threads and verbose mode:

```
julio@blaze:~/tools/web/webshotter$ ./webshotter.py -v example-urls.list -t 3
Starting with 3 threads
Thread-3 received argument: http://www.whatever.io
Thread-2 received argument: http://www.google.com
Thread-1 received argument: http://www.blazeinfosec.com
Thread-1 received argument: http://www.twitter.com
Thread-1 received argument: http://www.facebook.com
Thread-1 received argument: http://www.reddit.com/r/netsec
Thread-1 received argument: http://blog.whatever.io
```

## Dependencies

This code depends on Selenium Web Driver and PhantomJS.
Selenium is avaialble on Kali through apt - apt-get install python-selenium (or python3-selenium). Alternatively, it can be found using pypi (https://pypi.python.org/pypi/selenium)
PhantomJS is available on Kali through apt - apt-get install phantomjs. Alternatively, it can be found using the links at http://phantomjs.org/download.html.

Alternatively, use the following commands:
```
julio@blaze:~/tools/web/webshotter$ pip install selenium
julio@blaze:~/tools/web/webshotter$ brew install phantomjs
```

## Known issues

Nothing yet.

## Contributors

* **Chris A** - alphaskade at gmail dot com (@alphaskade)

Send a pull request if you feel like.

## Author

* **Julio Cesar Fort** - julio at blazeinfosec dot com
* Twitter: @juliocesarfort / @blazeinfosec

## License

This project is licensed under the Apache License - see the [LICENSE](LICENSE) file for details.
