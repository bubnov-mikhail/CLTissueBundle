# TissueBundle [![License](https://poser.pugx.org/cleentfaar/tissue-bundle/license.svg)](https://packagist.org/packages/cleentfaar/tissue-bundle)

A Symfony bundle that can scan your files for viruses using the [Tissue](https://github.com/cleentfaar/tissue) library and adapters.

[![Build Status](https://secure.travis-ci.org/cleentfaar/CLTissueBundle.svg)](http://travis-ci.org/cleentfaar/CLTissueBundle)
[![Scrutinizer Code Quality](https://scrutinizer-ci.com/g/cleentfaar/CLTissueBundle/badges/quality-score.png?b=master)](https://scrutinizer-ci.com/g/cleentfaar/CLTissueBundle/?branch=master)
[![Code Coverage](https://scrutinizer-ci.com/g/cleentfaar/CLTissueBundle/badges/coverage.png?b=master)](https://scrutinizer-ci.com/g/cleentfaar/CLTissueBundle/?branch=master)<br/>
[![Latest Stable Version](https://poser.pugx.org/cleentfaar/tissue-bundle/v/stable.svg)](https://packagist.org/packages/cleentfaar/tissue-bundle)
[![Total Downloads](https://poser.pugx.org/cleentfaar/tissue-bundle/downloads.svg)](https://packagist.org/packages/cleentfaar/tissue-bundle)
[![Latest Unstable Version](https://poser.pugx.org/cleentfaar/tissue-bundle/v/unstable.svg)](https://packagist.org/packages/cleentfaar/tissue-bundle)


### What does this bundle do?

Well pictures say more than a thousand words right...

#### 1. You have a file-upload form...
![1. You have a file-upload form...](Resources/doc/screens/upload1.png)

#### 2. Someone tries to upload an infected file...
![2. Someone tries to upload an infected file...](Resources/doc/screens/upload2.png)

#### 3. The infected file gets rejected...
![3. The infected file gets rejected...](Resources/doc/screens/upload3.png)


### Documentation

- [Installation](Resources/doc/installation.md)
- [Usage](Resources/doc/usage.md)


### WARNING

**I highly recommend you to research the security issues involved before using any of these packages on a production server!**

Although following the steps described in the documentation should be enough to keep most evil-doers from uploading infected
files to your form, I can never give any 100% guarantee! You should take care in keeping your virus-scanner's signature
database up-to-date, otherwise new viruses may get through. You should also keep in mind that there are many more ways to
abuse uploads than just uploading an infected file!

**Make sure your application cannot be manipulated to execute any of the uploaded files! Not even those deemed 'clean'!**

For instance, if you were to keep files available on your web-directory after they have been uploaded, you better
make sure that there is **NO CHANCE** that the file may get executed by your application in one way or another.

A malicious user could simply upload a piece of PHP-code (no virus!) that will open your application up to a huge range
of leaks. Again, that's just one of the reasons that you should not solely rely on this package protecting your site!

Read up on this subject before opening up your application to possible security leaks! **I am not responsible for
any damage done to your server or application while using this package!**
