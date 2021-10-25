---
layout: tips
title: How to use urlretrieve in Python 3
description: Download hooks in urlretrieve
---

The urlretrieve() function provided by the urllib module  downloads the remote data directly to the local computer.

urlretrieve(url, filename=None, reporthook=None, data=None)

- The parameter filename specifies the save local path (if the parameter is not specified, urllib will generate a temporary file to save the data.)
- The parameter reporthook is a callback function, which will trigger when the server is connected and the corresponding data block is transferred. 
- We can use this callback function to display the current download progress.  Parameter data refers to the data of the post import server.  
This method returns a tuple containing two elements (filename, headers). 
- Filename represents the path saved to the local, and header represents the response header of the server


'''python
#!/usr/bin/env python  
# coding=utf-8  
import os  
import urllib  
  
def download_hook(block_num, block_size, total_size):  
    '''''Callback function 
    @block_num:Downloaded data block 
    @Block size :Block size 
    @total_size:Size of the remote file 
    '''  
    per=100.0*a*b/c  
    if per>100:  
        per=100  
    print '%.2f%%' % per  
  
url='https://www.dundeecity.gov.uk/sites/default/files/publications/civic_renewal_forms.zip'  
dir=os.path.abspath('.')  
work_path=os.path.join(dir,'civic_renewal_forms.zip')  
urllib.urlretrieve(url,work_path,download_hook)
'''

References: 
https://programmer.ink/think/how-to-use-urlretrieve-in-python-3.html
https://stackoverflow.com/questions/52070906/how-do-i-check-for-a-file-to-be-finished-downloading-python3
