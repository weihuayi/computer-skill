# Jupyter 

Narratives are collaborative, shareable, publishable, and reproducible

一款开源软件能否在商业上成功，很大程度上依赖三件事 - 成功的 user case(用例), 活跃的社区和一个好故事

https://docs.docker.com/engine/installation/linux/ubuntulinux/
## Pip3 安装 

安装 `jupyter`

```
sudo apt-get install build-essential python3-dev
sudo apt-get install python3 python3-dev python3-pip
sudo apt-get install ipython3 ipython3-notebook 
sudo -H pip3 install jupyter
```

```
sudo -H pip3 install pymatbridge
sudo -H pip3 install matlab_kernel
sudo python3 -m matlab_kernel
```

```
sudo -H pip3 install bash_kernel
sudo python3 -m bash_kernel.install
```

```
sudo -H pip3 install jupyter_c_kernel
git clone https://github.com/brendan-rius/jupyter-c-kernel.git
cd jupyter-c-kernel/
sudo -H jupyter-kernelspec install c_spec/
jupyter-kernelspec list
```

   

```
git clone https://github.com/jfbercher/jupyter_latex_envs.git
cd jupyter_latex_envs/
sudo python3 setup.py install
vim setup.py  # fixed the bug README2.rst
sudo python3 setup.py install
sudo jupyter nbextension install --py latex_envs
sudo jupyter nbextension enable latex_envs
sudo jupyter nbextension enable latex_envs --py
```

```
sudo -H pip3 install jupyter-cjk-xelatex
```

```
pip3 search jupyter_contrib_nbextensions
```


在终端中调用

```
$ jupyter-notebook
```

会自动调用默认浏览器打开 `http://localhost:8888/`.

## Anaconda 安装
https://www.continuum.io/downloads

# JupyterHub

```
sudo apt-get install npm nodejs-legacy
```

```
npm install -g configurable-http-proxy
sudo -H pip3 install jupyterhub   
```

```
openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout /etc/apache2/ssl/apache.key -out /etc/apache2/ssl/apache.crt
```



## jupyter-notebook  slide show 

```
sudo -H pip3 install RISE
sudo jupyter-nbextension install rise --py --sys-prefix
sudo jupyter-nbextension enable rise --py --sys-prefix
```

## Mac os

1.	Install mac port 
	2.	port install python34
	3.	port install py34-pip
	4.	sudo pip install jupyter
	5.	jupyter notebook --generate-config
	6.	vi ~/.jupyter/jupyter_notebook_config.py
	7.	c.NotebookApp.browser = u'Safari'
	8.	sudo -H pip install numpy
	9.	sudo -H pip install pymatbridge
	10.	sudo -H pip install matlab_kernel
	11.	python -m matlab_kernel --user
	12.	cd "matlabroot/extern/engines/python"
	13.	python setup.py install

If the path is not included, open .bash_profile, add path 

export PATH=/opt/local/Library/Frameworks/Python.framework/Versions/3.4/bin:$PATH
export LD_LIBRARY_PATH=/opt/local/Library/Frameworks/Python.framework/Versions/3.4/lib/python3.4/site-packages:$LD_LIBRARY_PATH

## 技巧

sudo pip install jupyter_contrib_nbextensions
sudo jupyter contrib nbextension install --user


sudo -H pip install ipywidgets
sudo jupyter nbextension enable --py widgetsnbextension


