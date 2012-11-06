---
title: Seismic Unix on OSX
date: '2012-11-06'
description:
categories: osx,geophysics,seismic
---

Howto install the open source seismic processing package on OSX Mountain Lion:
(I'm using the actual beta version 43R2, if you have another version, maybe some changes will be necessary)

##Prerequisits:
* a working compiler (xcode installed) and xserver/xquartz.

-------------
Get the latest sourcecode from the [Seismic Unix Homepage](http://www.cwp.mines.edu/cwpcodes/) and put it into a directory in your home directory (in the example I use cwpsu):

<pre class="prettyprint">
cd
mkdir cwpsu
</pre>

Untar the archive:
<pre class="prettyprint">
tar -xvf cwp_su_all_43R2.tar
</pre>

Prepare your environment variables:
Use your favorite editor to edit .bash_profile and add
<pre class="prettyprint">
export CWPROOT=/Users/sebastian/cwpsu
export PATH=/Users/sebastian/cwpsu/bin:$PATH
</pre>

.bash\_profile is only used when opening a new shell, therefore use source to update the environmental variables now
<pre class="prettyprint">
source .bash_profile
</pre>

Now copy the example config file for your system from the configs directory into the src directory
<pre class="prettyprint">
cd src
cp configs/Makefile.config_Darwin_i386 Makefile.config
</pre>

Now you have to correct a little mistake in this file: Look for this line:
<pre class="prettyprint">
ENDIANFLAG = -DCWP_LITLE_ENDIAN
</pre>
and replace it with this one:
<pre class="prettyprint">
ENDIANFLAG = -DCWP_LITTLE_ENDIAN
</pre>

(this missing T cost me about an hour of troubleshooting...)

You are ready to compile now:
<pre class="prettyprint">
make install
make xtinstall
</pre>

If everything went well, you can check with 
<pre class="prettyprint">
suplane | suximage
</pre>