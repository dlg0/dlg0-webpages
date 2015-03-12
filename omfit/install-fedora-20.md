OMFit Installation on Fedora 20
-------------------------------
You can check your Fedora version with

```
-bash-4.2# cat /etc/fedora-release 
Fedora release 20 (Heisenbug)
```
The following is all under the **root** user ...

Update your Fedora
```
yum update
```

Now we follow along with the official OMFit instructions [here](http://gafusion.github.io/OMFIT-source/install.html)

```
yum install numpy scipy python-matplotlib netcdf4-python python-pip pyodbc
yum install hdf5-devel netcdf-devel python-tools
pip install fortranformat configobj asciitable uncertainties netCDF4 astropy
pip install --pre GitPython
yum install freetds-devel freetds unixODBC unixODBC-devel
```
##Install MDS+##
Go [here](http://www.mdsplus.org/index.php/Latest_RPM%27s_and_Yum_repositories) to get the repository rpm that will allow you to yum install MDS+, i.e., 

```
wget http://www.mdsplus.org/dist/fc20/stable/RPMS/noarch/mdsplus-repo-6.1-77.fc20.noarch.rpm
yum install mdsplus-repo-6.1-77.fc20.noarch.rpm
yum install mdsplus-kernel mdsplus-python
```
##Install OMFit##
```
yum install git
git clone -b unstable git@github.com:gafusion/OMFIT-source.git
git submodule init
git submodule update
```

Refer back to the [Ubuntu install instructions](http://gafusion.github.io/OMFIT-source/install.html) to setup OMFit.

> Written with [StackEdit](https://stackedit.io/).