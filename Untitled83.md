```python
!pip install selenium

```

    Requirement already satisfied: selenium in c:\users\usuario\anaconda3\lib\site-packages (3.141.0)
    Requirement already satisfied: urllib3 in c:\users\usuario\anaconda3\lib\site-packages (from selenium) (1.25.9)
    


```python
import sys
sys.path.insert(0,'/usr/lib/chromium-browser/chromedriver')

from selenium import webdriver

chrome_options = webdriver.ChromeOptions()
chrome_options.add_argument('--headless')
chrome_options.add_argument('--no-sandbox')
chrome_options.add_argument('--disable-dev-shm-usage')
wd = webdriver.Chrome('chromedriver',chrome_options=chrome_options)
```

    <ipython-input-3-77e58fcfd6a9>:10: DeprecationWarning: use options instead of chrome_options
      wd = webdriver.Chrome('chromedriver',chrome_options=chrome_options)
    


    ---------------------------------------------------------------------------

    FileNotFoundError                         Traceback (most recent call last)

    ~\anaconda3\lib\site-packages\selenium\webdriver\common\service.py in start(self)
         71             cmd.extend(self.command_line_args())
    ---> 72             self.process = subprocess.Popen(cmd, env=self.env,
         73                                             close_fds=platform.system() != 'Windows',
    

    ~\anaconda3\lib\subprocess.py in __init__(self, args, bufsize, executable, stdin, stdout, stderr, preexec_fn, close_fds, shell, cwd, env, universal_newlines, startupinfo, creationflags, restore_signals, start_new_session, pass_fds, encoding, errors, text)
        853 
    --> 854             self._execute_child(args, executable, preexec_fn, close_fds,
        855                                 pass_fds, cwd, env,
    

    ~\anaconda3\lib\subprocess.py in _execute_child(self, args, executable, preexec_fn, close_fds, pass_fds, cwd, env, startupinfo, creationflags, shell, p2cread, p2cwrite, c2pread, c2pwrite, errread, errwrite, unused_restore_signals, unused_start_new_session)
       1306             try:
    -> 1307                 hp, ht, pid, tid = _winapi.CreateProcess(executable, args,
       1308                                          # no special security
    

    FileNotFoundError: [WinError 2] El sistema no puede encontrar el archivo especificado

    
    During handling of the above exception, another exception occurred:
    

    WebDriverException                        Traceback (most recent call last)

    <ipython-input-3-77e58fcfd6a9> in <module>
          8 chrome_options.add_argument('--no-sandbox')
          9 chrome_options.add_argument('--disable-dev-shm-usage')
    ---> 10 wd = webdriver.Chrome('chromedriver',chrome_options=chrome_options)
    

    ~\anaconda3\lib\site-packages\selenium\webdriver\chrome\webdriver.py in __init__(self, executable_path, port, options, service_args, desired_capabilities, service_log_path, chrome_options, keep_alive)
         71             service_args=service_args,
         72             log_path=service_log_path)
    ---> 73         self.service.start()
         74 
         75         try:
    

    ~\anaconda3\lib\site-packages\selenium\webdriver\common\service.py in start(self)
         79         except OSError as err:
         80             if err.errno == errno.ENOENT:
    ---> 81                 raise WebDriverException(
         82                     "'%s' executable needs to be in PATH. %s" % (
         83                         os.path.basename(self.path), self.start_error_message)
    

    WebDriverException: Message: 'chromedriver' executable needs to be in PATH. Please see https://sites.google.com/a/chromium.org/chromedriver/home
    



```python
from selenium import webdriver

# Para que abra navegador
wd = webdriver.Firefox()

```


    ---------------------------------------------------------------------------

    FileNotFoundError                         Traceback (most recent call last)

    ~\anaconda3\lib\site-packages\selenium\webdriver\common\service.py in start(self)
         71             cmd.extend(self.command_line_args())
    ---> 72             self.process = subprocess.Popen(cmd, env=self.env,
         73                                             close_fds=platform.system() != 'Windows',
    

    ~\anaconda3\lib\subprocess.py in __init__(self, args, bufsize, executable, stdin, stdout, stderr, preexec_fn, close_fds, shell, cwd, env, universal_newlines, startupinfo, creationflags, restore_signals, start_new_session, pass_fds, encoding, errors, text)
        853 
    --> 854             self._execute_child(args, executable, preexec_fn, close_fds,
        855                                 pass_fds, cwd, env,
    

    ~\anaconda3\lib\subprocess.py in _execute_child(self, args, executable, preexec_fn, close_fds, pass_fds, cwd, env, startupinfo, creationflags, shell, p2cread, p2cwrite, c2pread, c2pwrite, errread, errwrite, unused_restore_signals, unused_start_new_session)
       1306             try:
    -> 1307                 hp, ht, pid, tid = _winapi.CreateProcess(executable, args,
       1308                                          # no special security
    

    FileNotFoundError: [WinError 2] El sistema no puede encontrar el archivo especificado

    
    During handling of the above exception, another exception occurred:
    

    WebDriverException                        Traceback (most recent call last)

    <ipython-input-5-731c3b5f16c9> in <module>
          2 
          3 # Para que abra navegador
    ----> 4 wd = webdriver.Firefox()
    

    ~\anaconda3\lib\site-packages\selenium\webdriver\firefox\webdriver.py in __init__(self, firefox_profile, firefox_binary, timeout, capabilities, proxy, executable_path, options, service_log_path, firefox_options, service_args, desired_capabilities, log_path, keep_alive)
        162                 service_args=service_args,
        163                 log_path=service_log_path)
    --> 164             self.service.start()
        165 
        166             capabilities.update(options.to_capabilities())
    

    ~\anaconda3\lib\site-packages\selenium\webdriver\common\service.py in start(self)
         79         except OSError as err:
         80             if err.errno == errno.ENOENT:
    ---> 81                 raise WebDriverException(
         82                     "'%s' executable needs to be in PATH. %s" % (
         83                         os.path.basename(self.path), self.start_error_message)
    

    WebDriverException: Message: 'geckodriver' executable needs to be in PATH. 
    



```python

```
