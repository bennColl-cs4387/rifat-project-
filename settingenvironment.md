# Built process from source
## Step 1: forking
I forked the matplotlib repo

## Step 2: Cloned the repo in my computer
```bash
khairulanamrifat@Khairuls-MacBook-Pro ~ % git clone https://github.com/khairulrifat/matplotlib.git
Cloning into 'matplotlib'...
remote: Enumerating objects: 329294, done.
remote: Counting objects: 100% (336/336), done.
remote: Compressing objects: 100% (286/286), done.
remote: Total 329294 (delta 149), reused 184 (delta 50), pack-reused 328958 (from 1)
Receiving objects: 100% (329294/329294), 443.81 MiB | 12.16 MiB/s, done.
Resolving deltas: 100% (228684/228684), done.
khairulanamrifat@Khairuls-MacBook-Pro ~ % cd matplotlib
```
# step 2: Created a dedicated environment
I could use either conda or env to make a dedicated environment for my work
```bash
khairulanamrifat@Khairuls-MacBook-Pro matplotlib % python3 -m venv env

khairulanamrifat@Khairuls-MacBook-Pro matplotlib % source env/bin/activate
```
# step 3: Instlaled necessary dependencies
Installed the python dependencies and C++ compiler
```bash
(env) khairulanamrifat@Khairuls-MacBook-Pro matplotlib % pip install -r requirements/dev/dev-requirements.txt
Ignoring pywin32: markers 'sys_platform == "win32"' don't match your environment
Collecting pybind11!=2.13.3
  Downloading pybind11-2.13.6-py3-none-any.whl (243 kB)
     |████████████████████████████████| 243 kB 3.1 MB/s 
Collecting meson-python
  Downloading meson_python-0.16.0-py3-none-any.whl (26 kB)
Collecting numpy<2.1.0
  Downloading numpy-2.0.2-cp39-cp39-macosx_14_0_arm64.whl (5.3 MB)
     |████████████████████████████████| 5.3 MB 11.6 MB/s 
Collecting setuptools-scm
  Downloading setuptools_scm-8.1.0-py3-none-any.whl (43 kB)
     |████████████████████████████████| 43 kB 5.4 MB/s 
Collecting sphinx!=6.1.2,>=5.1.0
  Downloading sphinx-7.4.7-py3-none-any.whl (3.4 MB)
     |████████████████████████████████| 3.4 MB 14.0 MB/s 
Collecting colorspacious
  Downloading colorspacious-1.1.2-py2.py3-none-any.whl (37 kB)
Collecting ipython
  Downloading ipython-8.18.1-py3-none-any.whl (808 kB)
     |████████████████████████████████| 808 kB 10.5 MB/s 
Collecting ipywidgets
  Downloading ipywidgets-8.1.5-py3-none-any.whl (139 kB)
     |████████████████████████████████| 139 kB 11.6 MB/s 
Collecting ipykernel
  Downloading ipykernel-6.29.5-py3-none-any.whl (117 kB)
     |████████████████████████████████| 117 kB 6.7 MB/s 
Collecting numpydoc>=1.0
  Downloading numpydoc-1.8.0-py3-none-any.whl (64 kB)
     |████████████████████████████████| 64 kB 7.6 MB/s 
Collecting packaging>=20
  Downloading packaging-24.1-py3-none-any.whl (53 kB)
     |████████████████████████████████| 53 kB 9.2 MB/s 
Collecting pydata-sphinx-theme~=0.15.0
  Downloading pydata_sphinx_theme-0.15.4-py3-none-any.whl (4.6 MB)
     |████████████████████████████████| 4.6 MB 10.2 MB/s 
Collecting mpl-sphinx-theme~=3.9.0
  Downloading mpl_sphinx_theme-3.9.0-py3-none-any.whl (53 kB)
     |████████████████████████████████| 53 kB 5.0 MB/s 
Collecting pyyaml
  Downloading PyYAML-6.0.2-cp39-cp39-macosx_11_0_arm64.whl (172 kB)
     |████████████████████████████████| 172 kB 12.5 MB/s 
Collecting sphinxcontrib-svg2pdfconverter>=1.1.0
  Downloading sphinxcontrib_svg2pdfconverter-1.2.3-py3-none-any.whl (8.2 kB)
Collecting sphinxcontrib-video>=0.2.1
  Downloading sphinxcontrib_video-0.2.1-py3-none-any.whl (9.3 kB)
Collecting sphinx-copybutton
  Downloading sphinx_copybutton-0.5.2-py3-none-any.whl (13 kB)
Collecting sphinx-design
  Downloading sphinx_design-0.6.1-py3-none-any.whl (2.2 MB)
     |████████████████████████████████| 2.2 MB 12.5 MB/s 
Collecting sphinx-gallery[parallel]>=0.12.0
  Downloading sphinx_gallery-0.17.1-py3-none-any.whl (446 kB)
     |████████████████████████████████| 446 kB 13.5 MB/s 
Collecting sphinx-tags>=0.4.0
  Downloading sphinx_tags-0.4-py2.py3-none-any.whl (7.2 kB)
Collecting black<24
  Downloading black-23.12.1-cp39-cp39-macosx_11_0_arm64.whl (1.4 MB)
     |████████████████████████████████| 1.4 MB 13.5 MB/s 
Collecting certifi
  Downloading certifi-2024.8.30-py3-none-any.whl (167 kB)
     |████████████████████████████████| 167 kB 12.8 MB/s 
Collecting coverage!=6.3
  Downloading coverage-7.6.1-cp39-cp39-macosx_11_0_arm64.whl (207 kB)
     |████████████████████████████████| 207 kB 11.9 MB/s 
Collecting psutil
  Downloading psutil-6.0.0-cp38-abi3-macosx_11_0_arm64.whl (251 kB)
     |████████████████████████████████| 251 kB 12.3 MB/s 
Collecting pytest!=4.6.0,!=5.4.0,!=8.1.0
  Downloading pytest-8.3.3-py3-none-any.whl (342 kB)
     |████████████████████████████████| 342 kB 14.9 MB/s 
Collecting pytest-cov
  Downloading pytest_cov-5.0.0-py3-none-any.whl (21 kB)
Collecting pytest-rerunfailures
  Downloading pytest_rerunfailures-14.0-py3-none-any.whl (12 kB)
Collecting pytest-timeout
  Downloading pytest_timeout-2.3.1-py3-none-any.whl (14 kB)
Collecting pytest-xdist
  Downloading pytest_xdist-3.6.1-py3-none-any.whl (46 kB)
     |████████████████████████████████| 46 kB 9.2 MB/s 
Collecting pytest-xvfb
  Downloading pytest_xvfb-3.0.0-py3-none-any.whl (5.6 kB)
Collecting tornado
  Downloading tornado-6.4.1-cp38-abi3-macosx_10_9_universal2.whl (435 kB)
     |████████████████████████████████| 435 kB 15.0 MB/s 
Collecting nbconvert[execute]!=6.0.0,!=6.0.1,!=7.3.0,!=7.3.1
  Downloading nbconvert-7.16.4-py3-none-any.whl (257 kB)
     |████████████████████████████████| 257 kB 9.5 MB/s 
Collecting nbformat!=5.0.0,!=5.0.1
  Downloading nbformat-5.10.4-py3-none-any.whl (78 kB)
     |████████████████████████████████| 78 kB 13.3 MB/s 
Collecting pandas!=0.25.0
  Downloading pandas-2.2.3-cp39-cp39-macosx_11_0_arm64.whl (11.3 MB)
     |████████████████████████████████| 11.3 MB 82.1 MB/s 
Collecting pikepdf
  Downloading pikepdf-9.3.0-cp39-cp39-macosx_14_0_arm64.whl (4.4 MB)
     |████████████████████████████████| 4.4 MB 10.9 MB/s 
Collecting pytz
  Downloading pytz-2024.2-py2.py3-none-any.whl (508 kB)
     |████████████████████████████████| 508 kB 15.0 MB/s 
Collecting xarray
  Downloading xarray-2024.7.0-py3-none-any.whl (1.2 MB)
     |████████████████████████████████| 1.2 MB 16.1 MB/s 
Collecting flake8>=3.8
  Downloading flake8-7.1.1-py2.py3-none-any.whl (57 kB)
     |████████████████████████████████| 57 kB 9.7 MB/s 
Collecting pydocstyle>=5.1.0
  Downloading pydocstyle-6.3.0-py3-none-any.whl (38 kB)
Collecting flake8-docstrings>=1.4.0
  Downloading flake8_docstrings-1.7.0-py2.py3-none-any.whl (5.0 kB)
Collecting flake8-force
  Downloading flake8_force-0.0.2-py3-none-any.whl (4.3 kB)
Collecting pyproject-metadata>=0.7.1
  Downloading pyproject_metadata-0.8.0-py3-none-any.whl (7.5 kB)
Collecting meson>=0.63.3
  Downloading meson-1.5.2-py3-none-any.whl (968 kB)
     |████████████████████████████████| 968 kB 12.2 MB/s 
Collecting tomli>=1.0.0
  Downloading tomli-2.0.2-py3-none-any.whl (13 kB)
Requirement already satisfied: setuptools in ./env/lib/python3.9/site-packages (from setuptools-scm->-r requirements/dev/build-requirements.txt (line 4)) (58.0.4)
Collecting typing-extensions
  Downloading typing_extensions-4.12.2-py3-none-any.whl (37 kB)
Collecting importlib-metadata>=6.0
  Downloading importlib_metadata-8.5.0-py3-none-any.whl (26 kB)
Collecting snowballstemmer>=2.2
  Downloading snowballstemmer-2.2.0-py2.py3-none-any.whl (93 kB)
     |████████████████████████████████| 93 kB 7.9 MB/s 
Collecting sphinxcontrib-devhelp
  Downloading sphinxcontrib_devhelp-2.0.0-py3-none-any.whl (82 kB)
     |████████████████████████████████| 82 kB 5.1 MB/s 
Collecting Jinja2>=3.1
  Downloading jinja2-3.1.4-py3-none-any.whl (133 kB)
     |████████████████████████████████| 133 kB 11.7 MB/s 
Collecting Pygments>=2.17
  Downloading pygments-2.18.0-py3-none-any.whl (1.2 MB)
     |████████████████████████████████| 1.2 MB 10.2 MB/s 
Collecting sphinxcontrib-applehelp
  Downloading sphinxcontrib_applehelp-2.0.0-py3-none-any.whl (119 kB)
     |████████████████████████████████| 119 kB 13.0 MB/s 
Collecting sphinxcontrib-jsmath
  Downloading sphinxcontrib_jsmath-1.0.1-py2.py3-none-any.whl (5.1 kB)
Collecting sphinxcontrib-qthelp
  Downloading sphinxcontrib_qthelp-2.0.0-py3-none-any.whl (88 kB)
     |████████████████████████████████| 88 kB 13.0 MB/s 
Collecting imagesize>=1.3
  Downloading imagesize-1.4.1-py2.py3-none-any.whl (8.8 kB)
Collecting docutils<0.22,>=0.20
  Downloading docutils-0.21.2-py3-none-any.whl (587 kB)
     |████████████████████████████████| 587 kB 14.9 MB/s 
Collecting requests>=2.30.0
  Downloading requests-2.32.3-py3-none-any.whl (64 kB)
     |████████████████████████████████| 64 kB 8.7 MB/s 
Collecting babel>=2.13
  Downloading babel-2.16.0-py3-none-any.whl (9.6 MB)
     |████████████████████████████████| 9.6 MB 18.4 MB/s 
Collecting alabaster~=0.7.14
  Downloading alabaster-0.7.16-py3-none-any.whl (13 kB)
Collecting sphinxcontrib-htmlhelp>=2.0.0
  Downloading sphinxcontrib_htmlhelp-2.1.0-py3-none-any.whl (98 kB)
     |████████████████████████████████| 98 kB 13.1 MB/s 
Collecting sphinxcontrib-serializinghtml>=1.1.9
  Downloading sphinxcontrib_serializinghtml-2.0.0-py3-none-any.whl (92 kB)
     |████████████████████████████████| 92 kB 13.0 MB/s 
Collecting decorator
  Downloading decorator-5.1.1-py3-none-any.whl (9.1 kB)
Collecting jedi>=0.16
  Downloading jedi-0.19.1-py2.py3-none-any.whl (1.6 MB)
     |████████████████████████████████| 1.6 MB 18.3 MB/s 
Collecting stack-data
  Downloading stack_data-0.6.3-py3-none-any.whl (24 kB)
Collecting prompt-toolkit<3.1.0,>=3.0.41
  Downloading prompt_toolkit-3.0.48-py3-none-any.whl (386 kB)
     |████████████████████████████████| 386 kB 17.5 MB/s 
Collecting traitlets>=5
  Downloading traitlets-5.14.3-py3-none-any.whl (85 kB)
     |████████████████████████████████| 85 kB 14.4 MB/s 
Collecting pexpect>4.3
  Downloading pexpect-4.9.0-py2.py3-none-any.whl (63 kB)
     |████████████████████████████████| 63 kB 10.6 MB/s 
Collecting matplotlib-inline
  Downloading matplotlib_inline-0.1.7-py3-none-any.whl (9.9 kB)
Collecting exceptiongroup
  Downloading exceptiongroup-1.2.2-py3-none-any.whl (16 kB)
Collecting jupyterlab-widgets~=3.0.12
  Downloading jupyterlab_widgets-3.0.13-py3-none-any.whl (214 kB)
     |████████████████████████████████| 214 kB 14.6 MB/s 
Collecting comm>=0.1.3
  Downloading comm-0.2.2-py3-none-any.whl (7.2 kB)
Collecting widgetsnbextension~=4.0.12
  Downloading widgetsnbextension-4.0.13-py3-none-any.whl (2.3 MB)
     |████████████████████████████████| 2.3 MB 14.7 MB/s 
Collecting jupyter-core!=5.0.*,>=4.12
  Downloading jupyter_core-5.7.2-py3-none-any.whl (28 kB)
Collecting nest-asyncio
  Downloading nest_asyncio-1.6.0-py3-none-any.whl (5.2 kB)
Collecting jupyter-client>=6.1.12
  Downloading jupyter_client-8.6.3-py3-none-any.whl (106 kB)
     |████████████████████████████████| 106 kB 17.4 MB/s 
Collecting appnope
  Downloading appnope-0.1.4-py2.py3-none-any.whl (4.3 kB)
Collecting debugpy>=1.6.5
  Downloading debugpy-1.8.6-py2.py3-none-any.whl (5.2 MB)
     |████████████████████████████████| 5.2 MB 12.1 MB/s 
Collecting pyzmq>=24
  Downloading pyzmq-26.2.0-cp39-cp39-macosx_10_15_universal2.whl (1.3 MB)
     |████████████████████████████████| 1.3 MB 10.6 MB/s 
Collecting tabulate>=0.8.10
  Downloading tabulate-0.9.0-py3-none-any.whl (35 kB)
Collecting beautifulsoup4
  Downloading beautifulsoup4-4.12.3-py3-none-any.whl (147 kB)
     |████████████████████████████████| 147 kB 12.7 MB/s 
Collecting accessible-pygments
  Downloading accessible_pygments-0.0.5-py3-none-any.whl (1.4 MB)
     |████████████████████████████████| 1.4 MB 15.3 MB/s 
Collecting matplotlib
  Downloading matplotlib-3.9.2-cp39-cp39-macosx_11_0_arm64.whl (7.8 MB)
     |████████████████████████████████| 7.8 MB 13.3 MB/s 
Collecting pillow
  Downloading pillow-10.4.0-cp39-cp39-macosx_11_0_arm64.whl (3.4 MB)
     |████████████████████████████████| 3.4 MB 14.1 MB/s 
Collecting joblib
  Downloading joblib-1.4.2-py3-none-any.whl (301 kB)
     |████████████████████████████████| 301 kB 15.7 MB/s 
Collecting mypy-extensions>=0.4.3
  Downloading mypy_extensions-1.0.0-py3-none-any.whl (4.7 kB)
Collecting click>=8.0.0
  Downloading click-8.1.7-py3-none-any.whl (97 kB)
     |████████████████████████████████| 97 kB 14.6 MB/s 
Collecting pathspec>=0.9.0
  Downloading pathspec-0.12.1-py3-none-any.whl (31 kB)
Collecting platformdirs>=2
  Downloading platformdirs-4.3.6-py3-none-any.whl (18 kB)
Collecting iniconfig
  Downloading iniconfig-2.0.0-py3-none-any.whl (5.9 kB)
Collecting pluggy<2,>=1.5
  Downloading pluggy-1.5.0-py3-none-any.whl (20 kB)
Collecting execnet>=2.1
  Downloading execnet-2.1.1-py3-none-any.whl (40 kB)
     |████████████████████████████████| 40 kB 8.6 MB/s 
Collecting pyvirtualdisplay>=1.3
  Downloading PyVirtualDisplay-3.0-py3-none-any.whl (15 kB)
WARNING: nbconvert 7.16.4 does not provide the extra 'execute'
Collecting defusedxml
  Downloading defusedxml-0.7.1-py2.py3-none-any.whl (25 kB)
Collecting bleach!=5.0.0
  Downloading bleach-6.1.0-py3-none-any.whl (162 kB)
     |████████████████████████████████| 162 kB 15.4 MB/s 
Collecting jupyterlab-pygments
  Downloading jupyterlab_pygments-0.3.0-py3-none-any.whl (15 kB)
Collecting nbclient>=0.5.0
  Downloading nbclient-0.10.0-py3-none-any.whl (25 kB)
Collecting tinycss2
  Downloading tinycss2-1.3.0-py3-none-any.whl (22 kB)
Collecting mistune<4,>=2.0.3
  Downloading mistune-3.0.2-py3-none-any.whl (47 kB)
     |████████████████████████████████| 47 kB 9.4 MB/s 
Collecting markupsafe>=2.0
  Downloading MarkupSafe-2.1.5-cp39-cp39-macosx_10_9_universal2.whl (18 kB)
Collecting pandocfilters>=1.4.1
  Downloading pandocfilters-1.5.1-py2.py3-none-any.whl (8.7 kB)
Collecting jsonschema>=2.6
  Downloading jsonschema-4.23.0-py3-none-any.whl (88 kB)
     |████████████████████████████████| 88 kB 6.4 MB/s 
Collecting fastjsonschema>=2.15
  Downloading fastjsonschema-2.20.0-py3-none-any.whl (23 kB)
Collecting python-dateutil>=2.8.2
  Downloading python_dateutil-2.9.0.post0-py2.py3-none-any.whl (229 kB)
     |████████████████████████████████| 229 kB 14.2 MB/s 
Collecting tzdata>=2022.7
  Downloading tzdata-2024.2-py2.py3-none-any.whl (346 kB)
     |████████████████████████████████| 346 kB 14.0 MB/s 
Collecting Deprecated
  Downloading Deprecated-1.2.14-py2.py3-none-any.whl (9.6 kB)
Collecting lxml>=4.8
  Downloading lxml-5.3.0-cp39-cp39-macosx_10_9_universal2.whl (8.1 MB)
     |████████████████████████████████| 8.1 MB 10.7 MB/s 
Collecting pyflakes<3.3.0,>=3.2.0
  Downloading pyflakes-3.2.0-py2.py3-none-any.whl (62 kB)
     |████████████████████████████████| 62 kB 8.0 MB/s 
Collecting mccabe<0.8.0,>=0.7.0
  Downloading mccabe-0.7.0-py2.py3-none-any.whl (7.3 kB)
Collecting pycodestyle<2.13.0,>=2.12.0
  Downloading pycodestyle-2.12.1-py2.py3-none-any.whl (31 kB)
Collecting webencodings
  Downloading webencodings-0.5.1-py2.py3-none-any.whl (11 kB)
Collecting six>=1.9.0
  Downloading six-1.16.0-py2.py3-none-any.whl (11 kB)
Collecting zipp>=3.20
  Downloading zipp-3.20.2-py3-none-any.whl (9.2 kB)
Collecting parso<0.9.0,>=0.8.3
  Downloading parso-0.8.4-py2.py3-none-any.whl (103 kB)
     |████████████████████████████████| 103 kB 13.4 MB/s 
Collecting referencing>=0.28.4
  Downloading referencing-0.35.1-py3-none-any.whl (26 kB)
Collecting rpds-py>=0.7.1
  Downloading rpds_py-0.20.0-cp39-cp39-macosx_11_0_arm64.whl (311 kB)
     |████████████████████████████████| 311 kB 5.0 MB/s 
Collecting attrs>=22.2.0
  Downloading attrs-24.2.0-py3-none-any.whl (63 kB)
     |████████████████████████████████| 63 kB 4.0 MB/s 
Collecting jsonschema-specifications>=2023.03.6
  Downloading jsonschema_specifications-2023.12.1-py3-none-any.whl (18 kB)
Collecting ptyprocess>=0.5
  Downloading ptyprocess-0.7.0-py2.py3-none-any.whl (13 kB)
Collecting wcwidth
  Downloading wcwidth-0.2.13-py2.py3-none-any.whl (34 kB)
Collecting charset-normalizer<4,>=2
  Downloading charset_normalizer-3.3.2-cp39-cp39-macosx_11_0_arm64.whl (120 kB)
     |████████████████████████████████| 120 kB 9.7 MB/s 
Collecting urllib3<3,>=1.21.1
  Downloading urllib3-2.2.3-py3-none-any.whl (126 kB)
     |████████████████████████████████| 126 kB 6.2 MB/s 
Collecting idna<4,>=2.5
  Downloading idna-3.10-py3-none-any.whl (70 kB)
     |████████████████████████████████| 70 kB 12.8 MB/s 
Collecting soupsieve>1.2
  Downloading soupsieve-2.6-py3-none-any.whl (36 kB)
Collecting wrapt<2,>=1.10
  Downloading wrapt-1.16.0-cp39-cp39-macosx_11_0_arm64.whl (38 kB)
Collecting kiwisolver>=1.3.1
  Downloading kiwisolver-1.4.7-cp39-cp39-macosx_11_0_arm64.whl (64 kB)
     |████████████████████████████████| 64 kB 10.4 MB/s 
Collecting importlib-resources>=3.2.0
  Downloading importlib_resources-6.4.5-py3-none-any.whl (36 kB)
Collecting contourpy>=1.0.1
  Downloading contourpy-1.3.0-cp39-cp39-macosx_11_0_arm64.whl (249 kB)
     |████████████████████████████████| 249 kB 6.9 MB/s 
Collecting pyparsing>=2.3.1
  Downloading pyparsing-3.1.4-py3-none-any.whl (104 kB)
     |████████████████████████████████| 104 kB 13.7 MB/s 
Collecting cycler>=0.10
  Downloading cycler-0.12.1-py3-none-any.whl (8.3 kB)
Collecting fonttools>=4.22.0
  Downloading fonttools-4.54.1-cp39-cp39-macosx_11_0_arm64.whl (2.3 MB)
     |████████████████████████████████| 2.3 MB 12.2 MB/s 
Collecting pure-eval
  Downloading pure_eval-0.2.3-py3-none-any.whl (11 kB)
Collecting asttokens>=2.1.0
  Downloading asttokens-2.4.1-py2.py3-none-any.whl (27 kB)
Collecting executing>=1.2.0
  Downloading executing-2.1.0-py2.py3-none-any.whl (25 kB)
Installing collected packages: rpds-py, attrs, referencing, zipp, traitlets, six, platformdirs, jsonschema-specifications, urllib3, tornado, pyzmq, python-dateutil, markupsafe, jupyter-core, jsonschema, importlib-metadata, idna, fastjsonschema, charset-normalizer, certifi, webencodings, wcwidth, tomli, sphinxcontrib-serializinghtml, sphinxcontrib-qthelp, sphinxcontrib-jsmath, sphinxcontrib-htmlhelp, sphinxcontrib-devhelp, sphinxcontrib-applehelp, soupsieve, snowballstemmer, requests, Pygments, pure-eval, ptyprocess, parso, packaging, numpy, nbformat, jupyter-client, Jinja2, imagesize, executing, docutils, babel, asttokens, alabaster, wrapt, tzdata, typing-extensions, tinycss2, stack-data, sphinx, pytz, pyparsing, pyflakes, pycodestyle, prompt-toolkit, pluggy, pillow, pexpect, pandocfilters, nbclient, mistune, mccabe, matplotlib-inline, kiwisolver, jupyterlab-pygments, jedi, iniconfig, importlib-resources, fonttools, exceptiongroup, defusedxml, decorator, cycler, coverage, contourpy, bleach, beautifulsoup4, accessible-pygments, widgetsnbextension, tabulate, sphinx-gallery, pyvirtualdisplay, pytest, pyproject-metadata, pydocstyle, pydata-sphinx-theme, psutil, pathspec, pandas, nest-asyncio, nbconvert, mypy-extensions, meson, matplotlib, lxml, jupyterlab-widgets, joblib, ipython, flake8, execnet, Deprecated, debugpy, comm, click, appnope, xarray, sphinxcontrib-video, sphinxcontrib-svg2pdfconverter, sphinx-tags, sphinx-design, sphinx-copybutton, setuptools-scm, pyyaml, pytest-xvfb, pytest-xdist, pytest-timeout, pytest-rerunfailures, pytest-cov, pybind11, pikepdf, numpydoc, mpl-sphinx-theme, meson-python, ipywidgets, ipykernel, flake8-force, flake8-docstrings, colorspacious, black
Successfully installed Deprecated-1.2.14 Jinja2-3.1.4 Pygments-2.18.0 accessible-pygments-0.0.5 alabaster-0.7.16 appnope-0.1.4 asttokens-2.4.1 attrs-24.2.0 babel-2.16.0 beautifulsoup4-4.12.3 black-23.12.1 bleach-6.1.0 certifi-2024.8.30 charset-normalizer-3.3.2 click-8.1.7 colorspacious-1.1.2 comm-0.2.2 contourpy-1.3.0 coverage-7.6.1 cycler-0.12.1 debugpy-1.8.6 decorator-5.1.1 defusedxml-0.7.1 docutils-0.21.2 exceptiongroup-1.2.2 execnet-2.1.1 executing-2.1.0 fastjsonschema-2.20.0 flake8-7.1.1 flake8-docstrings-1.7.0 flake8-force-0.0.2 fonttools-4.54.1 idna-3.10 imagesize-1.4.1 importlib-metadata-8.5.0 importlib-resources-6.4.5 iniconfig-2.0.0 ipykernel-6.29.5 ipython-8.18.1 ipywidgets-8.1.5 jedi-0.19.1 joblib-1.4.2 jsonschema-4.23.0 jsonschema-specifications-2023.12.1 jupyter-client-8.6.3 jupyter-core-5.7.2 jupyterlab-pygments-0.3.0 jupyterlab-widgets-3.0.13 kiwisolver-1.4.7 lxml-5.3.0 markupsafe-2.1.5 matplotlib-3.9.2 matplotlib-inline-0.1.7 mccabe-0.7.0 meson-1.5.2 meson-python-0.16.0 mistune-3.0.2 mpl-sphinx-theme-3.9.0 mypy-extensions-1.0.0 nbclient-0.10.0 nbconvert-7.16.4 nbformat-5.10.4 nest-asyncio-1.6.0 numpy-2.0.2 numpydoc-1.8.0 packaging-24.1 pandas-2.2.3 pandocfilters-1.5.1 parso-0.8.4 pathspec-0.12.1 pexpect-4.9.0 pikepdf-9.3.0 pillow-10.4.0 platformdirs-4.3.6 pluggy-1.5.0 prompt-toolkit-3.0.48 psutil-6.0.0 ptyprocess-0.7.0 pure-eval-0.2.3 pybind11-2.13.6 pycodestyle-2.12.1 pydata-sphinx-theme-0.15.4 pydocstyle-6.3.0 pyflakes-3.2.0 pyparsing-3.1.4 pyproject-metadata-0.8.0 pytest-8.3.3 pytest-cov-5.0.0 pytest-rerunfailures-14.0 pytest-timeout-2.3.1 pytest-xdist-3.6.1 pytest-xvfb-3.0.0 python-dateutil-2.9.0.post0 pytz-2024.2 pyvirtualdisplay-3.0 pyyaml-6.0.2 pyzmq-26.2.0 referencing-0.35.1 requests-2.32.3 rpds-py-0.20.0 setuptools-scm-8.1.0 six-1.16.0 snowballstemmer-2.2.0 soupsieve-2.6 sphinx-7.4.7 sphinx-copybutton-0.5.2 sphinx-design-0.6.1 sphinx-gallery-0.17.1 sphinx-tags-0.4 sphinxcontrib-applehelp-2.0.0 sphinxcontrib-devhelp-2.0.0 sphinxcontrib-htmlhelp-2.1.0 sphinxcontrib-jsmath-1.0.1 sphinxcontrib-qthelp-2.0.0 sphinxcontrib-serializinghtml-2.0.0 sphinxcontrib-svg2pdfconverter-1.2.3 sphinxcontrib-video-0.2.1 stack-data-0.6.3 tabulate-0.9.0 tinycss2-1.3.0 tomli-2.0.2 tornado-6.4.1 traitlets-5.14.3 typing-extensions-4.12.2 tzdata-2024.2 urllib3-2.2.3 wcwidth-0.2.13 webencodings-0.5.1 widgetsnbextension-4.0.13 wrapt-1.16.0 xarray-2024.7.0 zipp-3.20.2
```
##step 4: installed python version 3.10
Tries to install matplotlib in edittable mode but failed as it required python version 3.10 or upper. 
Then installed python version 3.10 and set up the virtual environment again.
##step 5: Installed edittable mode
```bash
env) khairulanamrifat@Khairuls-MacBook-Pro matplotlib % python3.10 -m pip install --verbose --no-build-isolation --editable ".[dev]"

Using pip 24.2 from /Users/khairulanamrifat/matplotlib/env/lib/python3.10/site-packages/pip (python 3.10)
Obtaining file:///Users/khairulanamrifat/matplotlib
  Running command Checking if build backend supports build_editable
  Checking if build backend supports build_editable ... done
  Running command Preparing editable metadata (pyproject.toml)
  + meson setup /Users/khairulanamrifat/matplotlib /Users/khairulanamrifat/matplotlib/build/cp310 -Dbuildtype=release -Db_ndebug=if-release -Db_vscrt=md --native-file=/Users/khairulanamrifat/matplotlib/build/cp310/meson-python-native-file.ini
  The Meson build system
  Version: 1.5.2
  Source dir: /Users/khairulanamrifat/matplotlib
  Build dir: /Users/khairulanamrifat/matplotlib/build/cp310
  Build type: native build
  Program python3 found: YES (/Users/khairulanamrifat/matplotlib/env/bin/python3)
  Project name: matplotlib
  Project version: 0.1.0.dev51130+g60458da
  C compiler for the host machine: cc (clang 15.0.0 "Apple clang version 15.0.0 (clang-1500.3.9.4)")
  C linker for the host machine: cc ld64 1053.12
  C++ compiler for the host machine: c++ (clang 15.0.0 "Apple clang version 15.0.0 (clang-1500.3.9.4)")
  C++ linker for the host machine: c++ ld64 1053.12
  Host machine cpu family: aarch64
  Host machine cpu: aarch64
  Program python found: YES (/Users/khairulanamrifat/matplotlib/env/bin/python3.10)
  Did not find pkg-config by name 'pkg-config'
  Found pkg-config: NO
  Run-time dependency python found: YES 3.10
  pybind11-config found: YES (/Users/khairulanamrifat/matplotlib/env/bin/pybind11-config) 2.13.6
  Run-time dependency pybind11 found: YES 2.13.6

  Executing subproject freetype-2.6.1

  freetype-2.6.1| Project name: freetype2
  freetype-2.6.1| Project version: 2.6.1
  freetype-2.6.1| C compiler for the host machine: cc (clang 15.0.0 "Apple clang version 15.0.0 (clang-1500.3.9.4)")
  freetype-2.6.1| C linker for the host machine: cc ld64 1053.12
  freetype-2.6.1| Has header "unistd.h" : YES
  freetype-2.6.1| Has header "fcntl.h" : YES
  freetype-2.6.1| Has header "stdint.h" : YES
  freetype-2.6.1| Configuring ftconfig.h using configuration
  freetype-2.6.1| Configuring ftoption.h using configuration
  freetype-2.6.1| Build targets in project: 3
  freetype-2.6.1| Subproject freetype-2.6.1 finished.


  Executing subproject qhull

  qhull| Project name: qhull
  qhull| Project version: 8.0.2
  qhull| C compiler for the host machine: cc (clang 15.0.0 "Apple clang version 15.0.0 (clang-1500.3.9.4)")
  qhull| C linker for the host machine: cc ld64 1053.12
  qhull| Build targets in project: 4
  qhull| Subproject qhull finished.

  Run-time dependency dl found: YES
  Objective-C compiler for the host machine: clang (clang 15.0.0)
  Objective-C linker for the host machine: clang ld64 1053.12
  Run-time dependency appleframeworks found: YES (Cocoa)
  Configuring _version.py using configuration
  Program /Users/khairulanamrifat/matplotlib/tools/generate_matplotlibrc.py found: YES (/Users/khairulanamrifat/matplotlib/tools/generate_matplotlibrc.py)
  Build targets in project: 15

  matplotlib 0.1.0.dev51130+g60458da

    Subprojects
      freetype-2.6.1: YES
      qhull         : YES

    User defined options
      Native files  : /Users/khairulanamrifat/matplotlib/build/cp310/meson-python-native-file.ini
      buildtype     : release
      b_ndebug      : if-release
      b_vscrt       : md

  Found ninja-1.11.1.git.kitware.jobserver-1 at /Users/khairulanamrifat/matplotlib/env/bin/ninja
  + /Users/khairulanamrifat/matplotlib/env/bin/ninja
  [1/104] Compiling C++ object extern/agg24-svn/libagg.a.p/src_agg_trans_affine.cpp.o
  [2/104] Compiling C++ object extern/agg24-svn/libagg.a.p/src_agg_vpgen_segmentator.cpp.o
  [3/104] Compiling C++ object extern/agg24-svn/libagg.a.p/src_agg_bezier_arc.cpp.o
  [4/104] Compiling C++ object extern/agg24-svn/libagg.a.p/src_agg_vcgen_dash.cpp.o
  [5/104] Compiling C++ object extern/agg24-svn/libagg.a.p/src_agg_image_filters.cpp.o
  [6/104] Compiling C++ object extern/agg24-svn/libagg.a.p/src_agg_curves.cpp.o
  ../../extern/agg24-svn/src/agg_curves.cpp:24:18: warning: unused variable 'curve_distance_epsilon' [-Wunused-const-variable]
      const double curve_distance_epsilon                  = 1e-30;
                   ^
  1 warning generated.
  [7/104] Compiling C object subprojects/freetype-2.6.1/libfreetype.a.p/src_base_ftbdf.c.o
  [8/104] Compiling C object subprojects/freetype-2.6.1/libfreetype.a.p/src_base_ftbbox.c.o
  [9/104] Compiling C object subprojects/freetype-2.6.1/libfreetype.a.p/src_base_ftcid.c.o
  [10/104] Compiling C object subprojects/freetype-2.6.1/libfreetype.a.p/src_base_ftfntfmt.c.o
  [11/104] Compiling C++ object extern/agg24-svn/libagg.a.p/src_agg_vcgen_contour.cpp.o
  [12/104] Compiling C++ object extern/agg24-svn/libagg.a.p/src_agg_vcgen_stroke.cpp.o
  [13/104] Compiling C object subprojects/freetype-2.6.1/libfreetype.a.p/src_base_ftbitmap.c.o
  [14/104] Compiling C object subprojects/freetype-2.6.1/libfreetype.a.p/src_base_ftfstype.c.o
  [15/104] Compiling C object subprojects/freetype-2.6.1/libfreetype.a.p/src_base_ftgasp.c.o
  [16/104] Compiling C object subprojects/freetype-2.6.1/libfreetype.a.p/src_base_ftgxval.c.o
  [17/104] Compiling C object subprojects/freetype-2.6.1/libfreetype.a.p/src_base_ftinit.c.o
  [18/104] Compiling C object subprojects/freetype-2.6.1/libfreetype.a.p/src_base_ftglyph.c.o
  [19/104] Compiling C object subprojects/freetype-2.6.1/libfreetype.a.p/src_base_ftlcdfil.c.o
  [20/104] Compiling C object subprojects/freetype-2.6.1/libfreetype.a.p/src_base_ftmm.c.o
  [21/104] Compiling C object subprojects/freetype-2.6.1/libfreetype.a.p/src_base_ftotval.c.o
  [22/104] Compiling C object subprojects/freetype-2.6.1/libfreetype.a.p/src_base_ftpfr.c.o
  [23/104] Compiling C object subprojects/freetype-2.6.1/libfreetype.a.p/src_base_ftpatent.c.o
  [24/104] Compiling C object subprojects/freetype-2.6.1/libfreetype.a.p/src_base_ftsynth.c.o
  [25/104] Compiling C object subprojects/freetype-2.6.1/libfreetype.a.p/src_base_ftsystem.c.o
  [26/104] Compiling C object subprojects/freetype-2.6.1/libfreetype.a.p/src_base_fttype1.c.o
  [27/104] Compiling C object subprojects/freetype-2.6.1/libfreetype.a.p/src_base_ftwinfnt.c.o
  [28/104] Compiling C object subprojects/freetype-2.6.1/libfreetype.a.p/src_bzip2_ftbzip2.c.o
  [29/104] Compiling C object subprojects/freetype-2.6.1/libfreetype.a.p/src_base_ftstroke.c.o
  [30/104] Linking static target extern/agg24-svn/libagg.a
  [31/104] Compiling C object subprojects/freetype-2.6.1/libfreetype.a.p/src_lzw_ftlzw.c.o
  [32/104] Compiling C++ object extern/ttconv/libttconv.a.p/ttutil.cpp.o
  [33/104] Compiling C object subprojects/freetype-2.6.1/libfreetype.a.p/src_cid_type1cid.c.o
  [34/104] Compiling C object subprojects/freetype-2.6.1/libfreetype.a.p/src_cache_ftcache.c.o
  [35/104] Compiling C object subprojects/freetype-2.6.1/libfreetype.a.p/src_bdf_bdf.c.o
  [36/104] Compiling C object subprojects/freetype-2.6.1/libfreetype.a.p/src_pcf_pcf.c.o
  [37/104] Compiling C object subprojects/freetype-2.6.1/libfreetype.a.p/src_autofit_autofit.c.o
  [38/104] Compiling C object subprojects/freetype-2.6.1/libfreetype.a.p/src_base_ftbase.c.o
  [39/104] Compiling C object subprojects/freetype-2.6.1/libfreetype.a.p/src_psnames_psnames.c.o
  [40/104] Compiling C object subprojects/freetype-2.6.1/libfreetype.a.p/src_smooth_smooth.c.o
  [41/104] Compiling C object subprojects/freetype-2.6.1/libfreetype.a.p/src_pfr_pfr.c.o
  [42/104] Compiling C object subprojects/freetype-2.6.1/libfreetype.a.p/src_raster_raster.c.o
  [43/104] Compiling C++ object extern/ttconv/libttconv.a.p/pprdrv_tt.cpp.o
  [44/104] Compiling C object subprojects/freetype-2.6.1/libfreetype.a.p/src_base_ftdebug.c.o
  [45/104] Compiling C object subprojects/freetype-2.6.1/libfreetype.a.p/src_gzip_ftgzip.c.o
  [46/104] Compiling C object subprojects/freetype-2.6.1/libfreetype.a.p/src_type42_type42.c.o
  [47/104] Compiling C object subprojects/freetype-2.6.1/libfreetype.a.p/src_winfonts_winfnt.c.o
  [48/104] Compiling C object subprojects/freetype-2.6.1/libfreetype.a.p/src_type1_type1.c.o
  [49/104] Compiling C object subprojects/freetype-2.6.1/libfreetype.a.p/src_pshinter_pshinter.c.o
  [50/104] Compiling C object subprojects/qhull-8.0.2/libqhull_r.a.p/src_libqhull_r_mem_r.c.o
  [51/104] Compiling C object subprojects/freetype-2.6.1/libfreetype.a.p/src_psaux_psaux.c.o
  [52/104] Compiling C object subprojects/qhull-8.0.2/libqhull_r.a.p/src_libqhull_r_libqhull_r.c.o
  [53/104] Compiling C object subprojects/qhull-8.0.2/libqhull_r.a.p/src_libqhull_r_geom_r.c.o
  ../../subprojects/qhull-8.0.2/src/libqhull_r/geom_r.c:623:24: warning: variable 'flip' set but not used [-Wunused-but-set-variable]
    int i, j, k, pivoti, flip=0;
                         ^
  1 warning generated.
  [54/104] Compiling C object subprojects/qhull-8.0.2/libqhull_r.a.p/src_libqhull_r_global_r.c.o
  [55/104] Compiling C object subprojects/qhull-8.0.2/libqhull_r.a.p/src_libqhull_r_random_r.c.o
  [56/104] Compiling C object subprojects/qhull-8.0.2/libqhull_r.a.p/src_libqhull_r_qset_r.c.o
  [57/104] Compiling C object subprojects/qhull-8.0.2/libqhull_r.a.p/src_libqhull_r_poly_r.c.o
  [58/104] Compiling C object subprojects/qhull-8.0.2/libqhull_r.a.p/src_libqhull_r_geom2_r.c.o
  [59/104] Compiling C object subprojects/qhull-8.0.2/libqhull_r.a.p/src_libqhull_r_usermem_r.c.o
  [60/104] Compiling C object subprojects/qhull-8.0.2/libqhull_r.a.p/src_libqhull_r_userprintf_rbox_r.c.o
  [61/104] Compiling C object subprojects/qhull-8.0.2/libqhull_r.a.p/src_libqhull_r_userprintf_r.c.o
  [62/104] Compiling C object subprojects/qhull-8.0.2/libqhull_r.a.p/src_libqhull_r_user_r.c.o
  [63/104] Compiling C object subprojects/qhull-8.0.2/libqhull_r.a.p/src_libqhull_r_rboxlib_r.c.o
  [64/104] Compiling C object subprojects/qhull-8.0.2/libqhull_r.a.p/src_libqhull_r_stat_r.c.o
  [65/104] Compiling C++ object extern/ttconv/libttconv.a.p/pprdrv_tt2.cpp.o
  [66/104] Compiling C object subprojects/qhull-8.0.2/libqhull_r.a.p/src_libqhull_r_poly2_r.c.o
  ../../subprojects/qhull-8.0.2/src/libqhull_r/poly2_r.c:103:37: warning: variable 'notgood' set but not used [-Wunused-but-set-variable]
    int numpart= 0, facet_i, facet_n, notgood= 0, notverified= 0;
                                      ^
  1 warning generated.
  [67/104] Linking static target extern/ttconv/libttconv.a
  [68/104] Compiling C object subprojects/freetype-2.6.1/libfreetype.a.p/src_sfnt_sfnt.c.o
  [69/104] Compiling C object subprojects/qhull-8.0.2/libqhull_r.a.p/src_libqhull_r_merge_r.c.o
  ../../subprojects/qhull-8.0.2/src/libqhull_r/merge_r.c:2907:17: warning: variable 'total' set but not used [-Wunused-but-set-variable]
    int cycles=0, total=0, facets, nummerge, numdegen= 0;
                  ^
  1 warning generated.
  [70/104] Compiling C object subprojects/qhull-8.0.2/libqhull_r.a.p/src_libqhull_r_io_r.c.o
  [71/104] Linking static target subprojects/qhull-8.0.2/libqhull_r.a
  [72/104] Compiling C object subprojects/freetype-2.6.1/libfreetype.a.p/src_cff_cff.c.o
  [73/104] Compiling C object subprojects/freetype-2.6.1/libfreetype.a.p/src_truetype_truetype.c.o
  [74/104] Compiling C++ object src/_backend_agg.cpython-310-darwin.so.p/py_converters.cpp.o
  [75/104] Compiling C++ object src/ft2font.cpython-310-darwin.so.p/py_converters.cpp.o
  [76/104] Linking static target subprojects/freetype-2.6.1/libfreetype.a
  [77/104] Compiling C++ object src/_path.cpython-310-darwin.so.p/py_converters.cpp.o
  [78/104] Compiling C++ object src/ft2font.cpython-310-darwin.so.p/ft2font.cpp.o
  [79/104] Compiling C++ object src/_backend_agg.cpython-310-darwin.so.p/_backend_agg.cpp.o
  [80/104] Compiling C++ object src/_c_internal_utils.cpython-310-darwin.so.p/_c_internal_utils.cpp.o
  [81/104] Compiling C++ object src/_backend_agg.cpython-310-darwin.so.p/py_converters_11.cpp.o
  [82/104] Compiling C++ object src/_image.cpython-310-darwin.so.p/py_converters_11.cpp.o
  [83/104] Compiling C++ object src/_path.cpython-310-darwin.so.p/py_converters_11.cpp.o
  [84/104] Generating lib/matplotlib/mpl-data/matplotlibrc with a custom command
  [85/104] Linking target src/_c_internal_utils.cpython-310-darwin.so
  [86/104] Compiling Objective-C object src/_macosx.cpython-310-darwin.so.p/_macosx.m.o
  [87/104] Compiling C++ object src/_tkagg.cpython-310-darwin.so.p/_tkagg.cpp.o
  [88/104] Compiling C++ object src/_qhull.cpython-310-darwin.so.p/_qhull_wrapper.cpp.o
  [89/104] Linking target src/_macosx.cpython-310-darwin.so
  [90/104] Linking target src/_tkagg.cpython-310-darwin.so
  [91/104] Compiling C++ object src/_tri.cpython-310-darwin.so.p/tri__tri.cpp.o
  [92/104] Compiling C++ object src/_ttconv.cpython-310-darwin.so.p/_ttconv.cpp.o
  [93/104] Compiling C++ object src/_tri.cpython-310-darwin.so.p/tri__tri_wrapper.cpp.o
  [94/104] Compiling C++ object src/_image.cpython-310-darwin.so.p/_image_wrapper.cpp.o
  [95/104] Compiling C++ object src/_path.cpython-310-darwin.so.p/_path_wrapper.cpp.o
  [96/104] Compiling C++ object src/ft2font.cpython-310-darwin.so.p/ft2font_wrapper.cpp.o
  [97/104] Linking target src/_ttconv.cpython-310-darwin.so
  [98/104] Compiling C++ object src/_backend_agg.cpython-310-darwin.so.p/_backend_agg_wrapper.cpp.o
  [99/104] Linking target src/_tri.cpython-310-darwin.so
  [100/104] Linking target src/_path.cpython-310-darwin.so
  [101/104] Linking target src/_image.cpython-310-darwin.so
  [102/104] Linking target src/_qhull.cpython-310-darwin.so
  [103/104] Linking target src/_backend_agg.cpython-310-darwin.so
  [104/104] Linking target src/ft2font.cpython-310-darwin.so
  Preparing editable metadata (pyproject.toml) ... done
Requirement already satisfied: contourpy>=1.0.1 in ./env/lib/python3.10/site-packages (from matplotlib==0.1.0.dev51130+g60458da) (1.3.0)
Requirement already satisfied: cycler>=0.10 in ./env/lib/python3.10/site-packages (from matplotlib==0.1.0.dev51130+g60458da) (0.12.1)
Requirement already satisfied: fonttools>=4.22.0 in ./env/lib/python3.10/site-packages (from matplotlib==0.1.0.dev51130+g60458da) (4.54.1)
Requirement already satisfied: kiwisolver>=1.3.1 in ./env/lib/python3.10/site-packages (from matplotlib==0.1.0.dev51130+g60458da) (1.4.7)
Requirement already satisfied: numpy>=1.23 in ./env/lib/python3.10/site-packages (from matplotlib==0.1.0.dev51130+g60458da) (2.0.2)
Requirement already satisfied: packaging>=20.0 in ./env/lib/python3.10/site-packages (from matplotlib==0.1.0.dev51130+g60458da) (24.1)
Requirement already satisfied: pillow>=8 in ./env/lib/python3.10/site-packages (from matplotlib==0.1.0.dev51130+g60458da) (10.4.0)
Requirement already satisfied: pyparsing>=2.3.1 in ./env/lib/python3.10/site-packages (from matplotlib==0.1.0.dev51130+g60458da) (3.1.4)
Requirement already satisfied: python-dateutil>=2.7 in ./env/lib/python3.10/site-packages (from matplotlib==0.1.0.dev51130+g60458da) (2.9.0.post0)
Requirement already satisfied: meson-python>=0.13.1 in ./env/lib/python3.10/site-packages (from matplotlib==0.1.0.dev51130+g60458da) (0.16.0)
Requirement already satisfied: pybind11!=2.13.3,>=2.6 in ./env/lib/python3.10/site-packages (from matplotlib==0.1.0.dev51130+g60458da) (2.13.6)
Requirement already satisfied: setuptools_scm>=7 in ./env/lib/python3.10/site-packages (from matplotlib==0.1.0.dev51130+g60458da) (8.1.0)
Requirement already satisfied: setuptools>=64 in ./env/lib/python3.10/site-packages (from matplotlib==0.1.0.dev51130+g60458da) (74.1.2)
Requirement already satisfied: meson>=0.63.3 in ./env/lib/python3.10/site-packages (from meson-python>=0.13.1->matplotlib==0.1.0.dev51130+g60458da) (1.5.2)
Requirement already satisfied: pyproject-metadata>=0.7.1 in ./env/lib/python3.10/site-packages (from meson-python>=0.13.1->matplotlib==0.1.0.dev51130+g60458da) (0.8.0)
Requirement already satisfied: tomli>=1.0.0 in ./env/lib/python3.10/site-packages (from meson-python>=0.13.1->matplotlib==0.1.0.dev51130+g60458da) (2.0.2)
Requirement already satisfied: six>=1.5 in ./env/lib/python3.10/site-packages (from python-dateutil>=2.7->matplotlib==0.1.0.dev51130+g60458da) (1.16.0)
Building wheels for collected packages: matplotlib
  Running command Building editable for matplotlib (pyproject.toml)
  Building editable for matplotlib (pyproject.toml) ... done
  Created wheel for matplotlib: filename=matplotlib-0.1.0.dev51130+g60458da-cp310-cp310-macosx_14_0_arm64.whl size=10302 sha256=a4c7d3ff418b2b4b5ca9fb7a01d5d4b2a0fb87624f390b850da66d015ff4461b
  Stored in directory: /private/var/folders/vh/rhvstgln0qd4mytknzxdhxz40000gn/T/pip-ephem-wheel-cache-phae9wuk/wheels/af/ee/54/dca3616a05644a2656e0e83a535f68c29de7a746ddd8677234
Successfully built matplotlib
Installing collected packages: matplotlib
  Attempting uninstall: matplotlib
    Found existing installation: matplotlib 3.9.2
    Uninstalling matplotlib-3.9.2:
      Removing file or directory /Users/khairulanamrifat/matplotlib/env/lib/python3.10/site-packages/__pycache__/pylab.cpython-310.pyc
      Removing file or directory /Users/khairulanamrifat/matplotlib/env/lib/python3.10/site-packages/matplotlib-3.9.2.dist-info/
      Removing file or directory /Users/khairulanamrifat/matplotlib/env/lib/python3.10/site-packages/matplotlib/
      Removing file or directory /Users/khairulanamrifat/matplotlib/env/lib/python3.10/site-packages/mpl_toolkits/axes_grid1/
      Removing file or directory /Users/khairulanamrifat/matplotlib/env/lib/python3.10/site-packages/mpl_toolkits/axisartist/
      Removing file or directory /Users/khairulanamrifat/matplotlib/env/lib/python3.10/site-packages/mpl_toolkits/mplot3d/
      Removing file or directory /Users/khairulanamrifat/matplotlib/env/lib/python3.10/site-packages/pylab.py
      Successfully uninstalled matplotlib-3.9.2
Successfully installed matplotlib-0.1.0.dev51130+g60458da
```

## Step 6: Verified the installation

```bash
(env) khairulanamrifat@Khairuls-MacBook-Pro matplotlib % python3.10 -c "import matplotlib; print(matplotlib.__file__)"
/Users/khairulanamrifat/matplotlib/lib/matplotlib/__init__.py
```
