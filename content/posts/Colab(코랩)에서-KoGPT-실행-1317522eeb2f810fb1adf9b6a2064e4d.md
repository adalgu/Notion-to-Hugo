---
title: "Colab(코랩)에서 KoGPT 실행"
date: "2024-11-01T18:07:00.000Z"
lastmod: "2024-11-01T18:15:00.000Z"
draft: false
series: []
Published: "2022-11-05T03:22:00.000+00:00"
tags: []
categories: []
Featured: false
Author: "Gunn Kim"
authors:
  - "Gunn Kim"
Status: "Done"
Public: true
NOTION_METADATA:
  object: "page"
  id: "1317522e-eb2f-810f-b1ad-f9b6a2064e4d"
  created_time: "2024-11-01T18:07:00.000Z"
  last_edited_time: "2024-11-01T18:15:00.000Z"
  created_by:
    object: "user"
    id: "04ade8dc-857d-40ba-9484-61bf41015314"
  last_edited_by:
    object: "user"
    id: "a3871fb7-da3a-40d9-96a3-c7e4e39081e2"
  cover: null
  icon: null
  parent:
    type: "database_id"
    database_id: "8229e4e4-34a6-47f7-b098-c86b7cd83ad6"
  archived: false
  in_trash: false
  properties:
    Created:
      id: "Aqll"
      type: "created_time"
      created_time: "2024-11-01T18:07:00.000Z"
    series:
      id: "B%3C%3FS"
      type: "multi_select"
      multi_select: []
    Subtitle:
      id: "DD_F"
      type: "rich_text"
      rich_text: []
    Page ID:
      id: "FqAD"
      type: "formula"
      formula:
        type: "string"
        string: "1317522eeb2f810fb1adf9b6a2064e4d"
    draft:
      id: "JiWU"
      type: "checkbox"
      checkbox: false
    Last Updated:
      id: "%5C%5BBm"
      type: "last_edited_time"
      last_edited_time: "2024-11-01T18:15:00.000Z"
    Tweet:
      id: "%60SwQ"
      type: "rich_text"
      rich_text: []
    authors:
      id: "bK%3B%5B"
      type: "people"
      people: []
    custom-front-matter:
      id: "c~kA"
      type: "rich_text"
      rich_text: []
    Slug:
      id: "fRDG"
      type: "rich_text"
      rich_text: []
    Published:
      id: "fy%3Ft"
      type: "date"
      date:
        start: "2022-11-05T03:22:00.000+00:00"
        end: null
        time_zone: null
    tags:
      id: "jw%7CC"
      type: "multi_select"
      multi_select: []
    categories:
      id: "nbY%3F"
      type: "multi_select"
      multi_select: []
    Featured:
      id: "oN%3F%3A"
      type: "checkbox"
      checkbox: false
    summary:
      id: "x%3AlD"
      type: "rich_text"
      rich_text: []
    Name:
      id: "title"
      type: "title"
      title:
        - type: "text"
          text:
            content: "Colab(코랩)에서 KoGPT"
            link: null
          annotations:
            bold: false
            italic: false
            strikethrough: false
            underline: false
            code: false
            color: "default"
          plain_text: "Colab(코랩)에서 KoGPT"
          href: null
        - type: "text"
          text:
            content: " 실행"
            link: null
          annotations:
            bold: true
            italic: false
            strikethrough: false
            underline: false
            code: false
            color: "default"
          plain_text: " 실행"
          href: null
    Author:
      id: "1f9a8ffc-dde9-4927-a747-6e2c304d6bd7"
      type: "rich_text"
      rich_text:
        - type: "text"
          text:
            content: "Gunn Kim"
            link: null
          annotations:
            bold: false
            italic: false
            strikethrough: false
            underline: false
            code: false
            color: "default"
          plain_text: "Gunn Kim"
          href: null
    Status:
      id: "6980bb35-4874-4a92-9a8b-26cece24bfd0"
      type: "status"
      status:
        id: "93da1c50-b6e1-4627-8a1c-e289898a5b3e"
        name: "Done"
        color: "green"
    Public:
      id: "8b3317bf-8bd9-4e07-b430-829f6408dd57"
      type: "checkbox"
      checkbox: true
    Description:
      id: "a8a234b4-277e-4754-9339-c588720def12"
      type: "rich_text"
      rich_text: []
  url: "https://www.notion.so/Colab-KoGPT-1317522eeb2f810fb1adf9b6a2064e4d"
  public_url: "https://datarecipe.notion.site/Colab-KoGPT-1317522eeb2f810fb1adf9b6a2064e4d"
UPDATE_TIME: "2024-11-02T00:18:03.374Z"
EXPIRY_TIME: "2024-11-02T01:17:52.570Z"

---


## 코랩에 우선 패키지 설치


[https://dacon.io/codeshare/4200](https://dacon.io/codeshare/4200)


### 패키지를 설치할 구글 드라이브 마운트


```python
import os, sys
from google.colab import drive
drive.mount('/content/drive')

my_path = '/content/package'
save_path = '/content/drive/MyDrive/Colab Notebooks/package' ## 패키지가 저장될 경로

os.symlink(save_path, my_path)
sys.path.insert(0, my_path)
```


### 패키지 설치하기


```python
!pip install --target=$my_path selenium
```


## 코랩에서 Kogpt 실행


[https://velog.io/@gtpgg1013/kogpt-%ED%95%9C%EA%B5%AD%EC%96%B4-%EC%83%9D%EC%84%B1-GPT-3-%EB%AA%85%EB%AC%B8%EA%B0%80-%EB%82%A9%EC%8B%9C%EC%98%A4](https://velog.io/@gtpgg1013/kogpt-%ED%95%9C%EA%B5%AD%EC%96%B4-%EC%83%9D%EC%84%B1-GPT-3-%EB%AA%85%EB%AC%B8%EA%B0%80-%EB%82%A9%EC%8B%9C%EC%98%A4)


### 예제코드 실행


```python
import torch
from transformers import AutoTokenizer, AutoModelForCausalLM 

tokenizer = AutoTokenizer.from_pretrained(
  'kakaobrain/kogpt', revision='KoGPT6B-ryan1.5b-float16',  # or float32 version: revision=KoGPT6B-ryan1.5b
  bos_token='[BOS]', eos_token='[EOS]', unk_token='[UNK]', pad_token='[PAD]', mask_token='[MASK]'
)
model = AutoModelForCausalLM.from_pretrained(
  'kakaobrain/kogpt', revision='KoGPT6B-ryan1.5b-float16',  # or float32 version: revision=KoGPT6B-ryan1.5b
  pad_token_id=tokenizer.eos_token_id,
  torch_dtype='auto', low_cpu_mem_usage=True
).to(device='cuda', non_blocking=True)
_ = model.eval()

prompt = '인공지능아, 너는 말을 할 수 있니?'
with torch.no_grad():
  tokens = tokenizer.encode(prompt, return_tensors='pt').to(device='cuda', non_blocking=True)
  gen_tokens = model.generate(tokens, do_sample=True, temperature=0.8, max_length=64)
  generated = tokenizer.batch_decode(gen_tokens)[0]
  
print(generated)
```


![](https://prod-files-secure.s3.us-west-2.amazonaws.com/94f51666-273a-443d-bf89-42827b5b6876/721152fd-075e-419f-aead-35c76bb522d7/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45GO43JXI4%2F20241102%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20241102T001752Z&X-Amz-Expires=3600&X-Amz-Signature=6937300cec688726c73799727812bd135f8b317d0239f526c29918adb7118b10&X-Amz-SignedHeaders=host&x-id=GetObject)


> 💡 실행은 되지만, 무료버전에서는 런타임이 종료되어 버린다.


## 코랩을 로컬 런타임에 연결


[https://velog.io/@t1won/Colab-Colab%EC%9D%84-%EB%A1%9C%EC%BB%AC-%EB%9F%B0%ED%83%80%EC%9E%84%EC%97%90-%EC%97%B0%EA%B2%B0](https://velog.io/@t1won/Colab-Colab%EC%9D%84-%EB%A1%9C%EC%BB%AC-%EB%9F%B0%ED%83%80%EC%9E%84%EC%97%90-%EC%97%B0%EA%B2%B0)


![](https://prod-files-secure.s3.us-west-2.amazonaws.com/94f51666-273a-443d-bf89-42827b5b6876/3c7bdd51-5f3f-4eea-a87a-7051cbfee61d/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45GO43JXI4%2F20241102%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20241102T001752Z&X-Amz-Expires=3600&X-Amz-Signature=130a7fe9a101bc146f88f7a466aa8be82e7d3032bbbf8215510a787cc27204fa&X-Amz-SignedHeaders=host&x-id=GetObject)


주피터 확장 프로그램을 설치


```python
pip install jupyter_http_over_ws
jupyter serverextension enable --py jupyter_http_over_ws
```


서버 시작과 인증


```python
jupyter notebook \
  --NotebookApp.allow_origin='https://colab.research.google.com' \
  --port=8888 \
  --NotebookApp.port_retries=0
```


런타임에 연결


```python
gunn@macmini ~ % jupyter notebook \
  --NotebookApp.allow_origin='https://colab.research.google.com' \
  --port=8888 \
  --NotebookApp.port_retries=0
[I 12:55:02.867 NotebookApp] Writing notebook server cookie secret to /Users/gunn/Library/Jupyter/runtime/notebook_cookie_secret
jupyter_http_over_ws extension initialized. Listening on /http_over_websocket
[I 12:55:03.072 NotebookApp] Serving notebooks from local directory: /Users/gunn
[I 12:55:03.072 NotebookApp] Jupyter Notebook 6.5.2 is running at:
[I 12:55:03.072 NotebookApp] http://localhost:8888/?token=73e61df1094637c8bd6f48e9da8e9fbf39be977ba4e509a6
[I 12:55:03.072 NotebookApp]  or http://127.0.0.1:8888/?token=73e61df1094637c8bd6f48e9da8e9fbf39be977ba4e509a6
[I 12:55:03.072 NotebookApp] Use Control-C to stop this server and shut down all kernels (twice to skip confirmation).
[C 12:55:03.075 NotebookApp] 
    
    To access the notebook, open this file in a browser:
        file:///Users/gunn/Library/Jupyter/runtime/nbserver-21674-open.html
    Or copy and paste one of these URLs:
        http://localhost:8888/?token=73e61df1094637c8bd6f48e9da8e9fbf39be977ba4e509a6
     or http://127.0.0.1:8888/?token=73e61df1094637c8bd6f48e9da8e9fbf39be977ba4e509a6
```


아래와 같은 서버주소+토큰을 코랩 로컬 런타임에 연결


http://localhost:8888/?token=73e61df1094637c8bd6f48e9da8e9fbf39be977ba4e509a6


### 패키지 설치 오류 해소


	```python
	Last login: Sat Nov  5 12:04:29 on ttys002
	gunn@macmini ~ % pip3 install transformers~=4.12.0
	DEPRECATION: Configuring installation scheme with distutils config files is deprecated and will no longer work in the near future. If you are using a Homebrew or Linuxbrew Python, please see discussion at https://github.com/Homebrew/homebrew-core/issues/76621
	Collecting transformers~=4.12.0
	  Downloading transformers-4.12.5-py3-none-any.whl (3.1 MB)
	     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 3.1/3.1 MB 16.3 MB/s eta 0:00:00
	Collecting tokenizers<0.11,>=0.10.1
	  Downloading tokenizers-0.10.3.tar.gz (212 kB)
	     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 212.7/212.7 kB 8.7 MB/s eta 0:00:00
	  Installing build dependencies ... done
	  Getting requirements to build wheel ... error
	  error: subprocess-exited-with-error
	  
	  × Getting requirements to build wheel did not run successfully.
	  │ exit code: 1
	  ╰─> [20 lines of output]
	      Traceback (most recent call last):
	        File "/opt/homebrew/lib/python3.9/site-packages/pip/_vendor/pep517/in_process/_in_process.py", line 363, in <module>
	          main()
	        File "/opt/homebrew/lib/python3.9/site-packages/pip/_vendor/pep517/in_process/_in_process.py", line 345, in main
	          json_out['return_val'] = hook(**hook_input['kwargs'])
	        File "/opt/homebrew/lib/python3.9/site-packages/pip/_vendor/pep517/in_process/_in_process.py", line 130, in get_requires_for_build_wheel
	          return hook(config_settings)
	        File "/opt/homebrew/Cellar/python@3.9/3.9.13_1/Frameworks/Python.framework/Versions/3.9/lib/python3.9/site-packages/setuptools/build_meta.py", line 177, in get_requires_for_build_wheel
	          return self._get_build_requires(
	        File "/opt/homebrew/Cellar/python@3.9/3.9.13_1/Frameworks/Python.framework/Versions/3.9/lib/python3.9/site-packages/setuptools/build_meta.py", line 159, in _get_build_requires
	          self.run_setup()
	        File "/opt/homebrew/Cellar/python@3.9/3.9.13_1/Frameworks/Python.framework/Versions/3.9/lib/python3.9/site-packages/setuptools/build_meta.py", line 174, in run_setup
	          exec(compile(code, __file__, 'exec'), locals())
	        File "setup.py", line 2, in <module>
	          from setuptools_rust import Binding, RustExtension
	        File "/private/var/folders/3_/zczr7dr10jx9w42gk6h237lw0000gn/T/pip-build-env-300co_am/overlay/lib/python3.9/site-packages/setuptools_rust/__init__.py", line 1, in <module>
	          from .build import build_rust
	        File "/private/var/folders/3_/zczr7dr10jx9w42gk6h237lw0000gn/T/pip-build-env-300co_am/overlay/lib/python3.9/site-packages/setuptools_rust/build.py", line 23, in <module>
	          from setuptools.command.build import build as CommandBuild  # type: ignore[import]
	      ModuleNotFoundError: No module named 'setuptools.command.build'
	      [end of output]
	  
	  note: This error originates from a subprocess, and is likely not a problem with pip.
	error: subprocess-exited-with-error
	
	× Getting requirements to build wheel did not run successfully.
	│ exit code: 1
	╰─> See above for output.
	
	note: This error originates from a subprocess, and is likely not a problem with pip.
	WARNING: There was an error checking the latest version of pip.
	gunn@macmini ~ % python -m pip install --upgrade pip
	Python 3.11.0 (v3.11.0:deaf509e8f, Oct 24 2022, 14:43:23) [Clang 13.0.0 (clang-1300.0.29.30)] on darwin
	Type "help", "copyright", "credits" or "license" for more information.
	>>> python
	Traceback (most recent call last):
	  File "<stdin>", line 1, in <module>
	NameError: name 'python' is not defined
	>>> !python -m pip install --upgrade pip
	  File "<stdin>", line 1
	    !python -m pip install --upgrade pip
	    ^
	SyntaxError: invalid syntax
	>>> quit()
	zsh: command not found: -m
	gunn@macmini ~ % pip3 install --upgrade pip3
	DEPRECATION: Configuring installation scheme with distutils config files is deprecated and will no longer work in the near future. If you are using a Homebrew or Linuxbrew Python, please see discussion at https://github.com/Homebrew/homebrew-core/issues/76621
	ERROR: Could not find a version that satisfies the requirement pip3 (from versions: none)
	ERROR: No matching distribution found for pip3
	WARNING: There was an error checking the latest version of pip.
	gunn@macmini ~ % pip3 install --upgrade pip 
	DEPRECATION: Configuring installation scheme with distutils config files is deprecated and will no longer work in the near future. If you are using a Homebrew or Linuxbrew Python, please see discussion at https://github.com/Homebrew/homebrew-core/issues/76621
	Requirement already satisfied: pip in /opt/homebrew/lib/python3.9/site-packages (22.1.1)
	Collecting pip
	  Downloading pip-22.3-py3-none-any.whl (2.1 MB)
	     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 2.1/2.1 MB 13.3 MB/s eta 0:00:00
	Installing collected packages: pip
	  Attempting uninstall: pip
	    Found existing installation: pip 22.1.1
	    Uninstalling pip-22.1.1:
	      Successfully uninstalled pip-22.1.1
	  DEPRECATION: Configuring installation scheme with distutils config files is deprecated and will no longer work in the near future. If you are using a Homebrew or Linuxbrew Python, please see discussion at https://github.com/Homebrew/homebrew-core/issues/76621
	DEPRECATION: Configuring installation scheme with distutils config files is deprecated and will no longer work in the near future. If you are using a Homebrew or Linuxbrew Python, please see discussion at https://github.com/Homebrew/homebrew-core/issues/76621
	Successfully installed pip-22.3
	gunn@macmini ~ % pip install transformers~=4.12.0
	DEPRECATION: Configuring installation scheme with distutils config files is deprecated and will no longer work in the near future. If you are using a Homebrew or Linuxbrew Python, please see discussion at https://github.com/Homebrew/homebrew-core/issues/76621
	Collecting transformers~=4.12.0
	  Using cached transformers-4.12.5-py3-none-any.whl (3.1 MB)
	Collecting requests
	  Downloading requests-2.28.1-py3-none-any.whl (62 kB)
	     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 62.8/62.8 kB 854.9 kB/s eta 0:00:00
	Collecting numpy>=1.17
	  Downloading numpy-1.23.4-cp39-cp39-macosx_11_0_arm64.whl (13.4 MB)
	     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 13.4/13.4 MB 33.2 MB/s eta 0:00:00
	Collecting filelock
	  Downloading filelock-3.8.0-py3-none-any.whl (10 kB)
	Collecting tqdm>=4.27
	  Downloading tqdm-4.64.1-py2.py3-none-any.whl (78 kB)
	     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 78.5/78.5 kB 3.6 MB/s eta 0:00:00
	Collecting huggingface-hub<1.0,>=0.1.0
	  Downloading huggingface_hub-0.10.1-py3-none-any.whl (163 kB)
	     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 163.5/163.5 kB 7.6 MB/s eta 0:00:00
	Collecting tokenizers<0.11,>=0.10.1
	  Using cached tokenizers-0.10.3.tar.gz (212 kB)
	  Installing build dependencies ... done
	  Getting requirements to build wheel ... done
	  Preparing metadata (pyproject.toml) ... done
	Requirement already satisfied: packaging>=20.0 in /opt/homebrew/lib/python3.9/site-packages (from transformers~=4.12.0) (21.3)
	Collecting pyyaml>=5.1
	  Downloading PyYAML-6.0-cp39-cp39-macosx_11_0_arm64.whl (173 kB)
	     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 174.0/174.0 kB 7.8 MB/s eta 0:00:00
	Collecting sacremoses
	  Downloading sacremoses-0.0.53.tar.gz (880 kB)
	     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 880.6/880.6 kB 22.8 MB/s eta 0:00:00
	  Preparing metadata (setup.py) ... done
	Collecting regex!=2019.12.17
	  Downloading regex-2022.10.31-cp39-cp39-macosx_11_0_arm64.whl (287 kB)
	     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 287.2/287.2 kB 13.3 MB/s eta 0:00:00
	Collecting typing-extensions>=3.7.4.3
	  Using cached typing_extensions-4.4.0-py3-none-any.whl (26 kB)
	Requirement already satisfied: pyparsing!=3.0.5,>=2.0.2 in /opt/homebrew/lib/python3.9/site-packages (from packaging>=20.0->transformers~=4.12.0) (3.0.9)
	Collecting urllib3<1.27,>=1.21.1
	  Downloading urllib3-1.26.12-py2.py3-none-any.whl (140 kB)
	     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 140.4/140.4 kB 6.7 MB/s eta 0:00:00
	Collecting charset-normalizer<3,>=2
	  Downloading charset_normalizer-2.1.1-py3-none-any.whl (39 kB)
	Requirement already satisfied: idna<4,>=2.5 in /opt/homebrew/lib/python3.9/site-packages (from requests->transformers~=4.12.0) (3.4)
	Collecting certifi>=2017.4.17
	  Downloading certifi-2022.9.24-py3-none-any.whl (161 kB)
	     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 161.1/161.1 kB 7.9 MB/s eta 0:00:00
	Requirement already satisfied: six in /opt/homebrew/lib/python3.9/site-packages (from sacremoses->transformers~=4.12.0) (1.16.0)
	Collecting click
	  Downloading click-8.1.3-py3-none-any.whl (96 kB)
	     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 96.6/96.6 kB 4.5 MB/s eta 0:00:00
	Collecting joblib
	  Downloading joblib-1.2.0-py3-none-any.whl (297 kB)
	     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 298.0/298.0 kB 12.5 MB/s eta 0:00:00
	Building wheels for collected packages: tokenizers, sacremoses
	  Building wheel for tokenizers (pyproject.toml) ... error
	  error: subprocess-exited-with-error
	  
	  × Building wheel for tokenizers (pyproject.toml) did not run successfully.
	  │ exit code: 1
	  ╰─> [51 lines of output]
	      running bdist_wheel
	      running build
	      running build_py
	      creating build
	      creating build/lib.macosx-12-arm64-cpython-39
	      creating build/lib.macosx-12-arm64-cpython-39/tokenizers
	      copying py_src/tokenizers/__init__.py -> build/lib.macosx-12-arm64-cpython-39/tokenizers
	      creating build/lib.macosx-12-arm64-cpython-39/tokenizers/models
	      copying py_src/tokenizers/models/__init__.py -> build/lib.macosx-12-arm64-cpython-39/tokenizers/models
	      creating build/lib.macosx-12-arm64-cpython-39/tokenizers/decoders
	      copying py_src/tokenizers/decoders/__init__.py -> build/lib.macosx-12-arm64-cpython-39/tokenizers/decoders
	      creating build/lib.macosx-12-arm64-cpython-39/tokenizers/normalizers
	      copying py_src/tokenizers/normalizers/__init__.py -> build/lib.macosx-12-arm64-cpython-39/tokenizers/normalizers
	      creating build/lib.macosx-12-arm64-cpython-39/tokenizers/pre_tokenizers
	      copying py_src/tokenizers/pre_tokenizers/__init__.py -> build/lib.macosx-12-arm64-cpython-39/tokenizers/pre_tokenizers
	      creating build/lib.macosx-12-arm64-cpython-39/tokenizers/processors
	      copying py_src/tokenizers/processors/__init__.py -> build/lib.macosx-12-arm64-cpython-39/tokenizers/processors
	      creating build/lib.macosx-12-arm64-cpython-39/tokenizers/trainers
	      copying py_src/tokenizers/trainers/__init__.py -> build/lib.macosx-12-arm64-cpython-39/tokenizers/trainers
	      creating build/lib.macosx-12-arm64-cpython-39/tokenizers/implementations
	      copying py_src/tokenizers/implementations/byte_level_bpe.py -> build/lib.macosx-12-arm64-cpython-39/tokenizers/implementations
	      copying py_src/tokenizers/implementations/sentencepiece_unigram.py -> build/lib.macosx-12-arm64-cpython-39/tokenizers/implementations
	      copying py_src/tokenizers/implementations/sentencepiece_bpe.py -> build/lib.macosx-12-arm64-cpython-39/tokenizers/implementations
	      copying py_src/tokenizers/implementations/base_tokenizer.py -> build/lib.macosx-12-arm64-cpython-39/tokenizers/implementations
	      copying py_src/tokenizers/implementations/__init__.py -> build/lib.macosx-12-arm64-cpython-39/tokenizers/implementations
	      copying py_src/tokenizers/implementations/char_level_bpe.py -> build/lib.macosx-12-arm64-cpython-39/tokenizers/implementations
	      copying py_src/tokenizers/implementations/bert_wordpiece.py -> build/lib.macosx-12-arm64-cpython-39/tokenizers/implementations
	      creating build/lib.macosx-12-arm64-cpython-39/tokenizers/tools
	      copying py_src/tokenizers/tools/__init__.py -> build/lib.macosx-12-arm64-cpython-39/tokenizers/tools
	      copying py_src/tokenizers/tools/visualizer.py -> build/lib.macosx-12-arm64-cpython-39/tokenizers/tools
	      copying py_src/tokenizers/__init__.pyi -> build/lib.macosx-12-arm64-cpython-39/tokenizers
	      copying py_src/tokenizers/models/__init__.pyi -> build/lib.macosx-12-arm64-cpython-39/tokenizers/models
	      copying py_src/tokenizers/decoders/__init__.pyi -> build/lib.macosx-12-arm64-cpython-39/tokenizers/decoders
	      copying py_src/tokenizers/normalizers/__init__.pyi -> build/lib.macosx-12-arm64-cpython-39/tokenizers/normalizers
	      copying py_src/tokenizers/pre_tokenizers/__init__.pyi -> build/lib.macosx-12-arm64-cpython-39/tokenizers/pre_tokenizers
	      copying py_src/tokenizers/processors/__init__.pyi -> build/lib.macosx-12-arm64-cpython-39/tokenizers/processors
	      copying py_src/tokenizers/trainers/__init__.pyi -> build/lib.macosx-12-arm64-cpython-39/tokenizers/trainers
	      copying py_src/tokenizers/tools/visualizer-styles.css -> build/lib.macosx-12-arm64-cpython-39/tokenizers/tools
	      running build_ext
	      running build_rust
	      error: can't find Rust compiler
	      
	      If you are using an outdated pip version, it is possible a prebuilt wheel is available for this package but pip is not able to install from it. Installing from the wheel would avoid the need for a Rust compiler.
	      
	      To update pip, run:
	      
	          pip install --upgrade pip
	      
	      and then retry package installation.
	      
	      If you did intend to build this package from source, try installing a Rust compiler from your system package manager and ensure it is on the PATH during installation. Alternatively, rustup (available at https://rustup.rs) is the recommended way to download and update the Rust compiler toolchain.
	      [end of output]
	  
	  note: This error originates from a subprocess, and is likely not a problem with pip.
	  ERROR: Failed building wheel for tokenizers
	  Building wheel for sacremoses (setup.py) ... done
	  Created wheel for sacremoses: filename=sacremoses-0.0.53-py3-none-any.whl size=895241 sha256=0231c8a22eb1063d21dc3f6ef49d636a4c2bbe433295649a7cc067cc8b43a392
	  Stored in directory: /Users/gunn/Library/Caches/pip/wheels/42/79/78/5ad3b042cb2d97c294535162cdbaf9b167e3b186eae55ab72d
	Successfully built sacremoses
	Failed to build tokenizers
	ERROR: Could not build wheels for tokenizers, which is required to install pyproject.toml-based projects
	gunn@macmini ~ % pip install torch~=1.12.1
	DEPRECATION: Configuring installation scheme with distutils config files is deprecated and will no longer work in the near future. If you are using a Homebrew or Linuxbrew Python, please see discussion at https://github.com/Homebrew/homebrew-core/issues/76621
	Collecting torch~=1.12.1
	  Downloading torch-1.12.1-cp39-none-macosx_11_0_arm64.whl (49.1 MB)
	     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 49.1/49.1 MB 47.4 MB/s eta 0:00:00
	Collecting typing-extensions
	  Using cached typing_extensions-4.4.0-py3-none-any.whl (26 kB)
	Installing collected packages: typing-extensions, torch
	  DEPRECATION: Configuring installation scheme with distutils config files is deprecated and will no longer work in the near future. If you are using a Homebrew or Linuxbrew Python, please see discussion at https://github.com/Homebrew/homebrew-core/issues/76621
	  DEPRECATION: Configuring installation scheme with distutils config files is deprecated and will no longer work in the near future. If you are using a Homebrew or Linuxbrew Python, please see discussion at https://github.com/Homebrew/homebrew-core/issues/76621
	DEPRECATION: Configuring installation scheme with distutils config files is deprecated and will no longer work in the near future. If you are using a Homebrew or Linuxbrew Python, please see discussion at https://github.com/Homebrew/homebrew-core/issues/76621
	Successfully installed torch-1.12.1 typing-extensions-4.4.0
	gunn@macmini ~ % pip install transformers~=4.12.0
	DEPRECATION: Configuring installation scheme with distutils config files is deprecated and will no longer work in the near future. If you are using a Homebrew or Linuxbrew Python, please see discussion at https://github.com/Homebrew/homebrew-core/issues/76621
	Collecting transformers~=4.12.0
	  Using cached transformers-4.12.5-py3-none-any.whl (3.1 MB)
	Collecting regex!=2019.12.17
	  Using cached regex-2022.10.31-cp39-cp39-macosx_11_0_arm64.whl (287 kB)
	Collecting requests
	  Using cached requests-2.28.1-py3-none-any.whl (62 kB)
	Collecting filelock
	  Using cached filelock-3.8.0-py3-none-any.whl (10 kB)
	Collecting sacremoses
	  Using cached sacremoses-0.0.53-py3-none-any.whl
	Collecting pyyaml>=5.1
	  Using cached PyYAML-6.0-cp39-cp39-macosx_11_0_arm64.whl (173 kB)
	Collecting huggingface-hub<1.0,>=0.1.0
	  Using cached huggingface_hub-0.10.1-py3-none-any.whl (163 kB)
	Collecting tqdm>=4.27
	  Using cached tqdm-4.64.1-py2.py3-none-any.whl (78 kB)
	Collecting tokenizers<0.11,>=0.10.1
	  Using cached tokenizers-0.10.3.tar.gz (212 kB)
	  Installing build dependencies ... done
	  Getting requirements to build wheel ... done
	  Preparing metadata (pyproject.toml) ... done
	Collecting numpy>=1.17
	  Using cached numpy-1.23.4-cp39-cp39-macosx_11_0_arm64.whl (13.4 MB)
	Requirement already satisfied: packaging>=20.0 in /opt/homebrew/lib/python3.9/site-packages (from transformers~=4.12.0) (21.3)
	Requirement already satisfied: typing-extensions>=3.7.4.3 in /opt/homebrew/lib/python3.9/site-packages (from huggingface-hub<1.0,>=0.1.0->transformers~=4.12.0) (4.4.0)
	Requirement already satisfied: pyparsing!=3.0.5,>=2.0.2 in /opt/homebrew/lib/python3.9/site-packages (from packaging>=20.0->transformers~=4.12.0) (3.0.9)
	Collecting certifi>=2017.4.17
	  Using cached certifi-2022.9.24-py3-none-any.whl (161 kB)
	Collecting charset-normalizer<3,>=2
	  Using cached charset_normalizer-2.1.1-py3-none-any.whl (39 kB)
	Requirement already satisfied: idna<4,>=2.5 in /opt/homebrew/lib/python3.9/site-packages (from requests->transformers~=4.12.0) (3.4)
	Collecting urllib3<1.27,>=1.21.1
	  Using cached urllib3-1.26.12-py2.py3-none-any.whl (140 kB)
	Requirement already satisfied: six in /opt/homebrew/lib/python3.9/site-packages (from sacremoses->transformers~=4.12.0) (1.16.0)
	Collecting click
	  Using cached click-8.1.3-py3-none-any.whl (96 kB)
	Collecting joblib
	  Using cached joblib-1.2.0-py3-none-any.whl (297 kB)
	Building wheels for collected packages: tokenizers
	  Building wheel for tokenizers (pyproject.toml) ... error
	  error: subprocess-exited-with-error
	  
	  × Building wheel for tokenizers (pyproject.toml) did not run successfully.
	  │ exit code: 1
	  ╰─> [51 lines of output]
	      running bdist_wheel
	      running build
	      running build_py
	      creating build
	      creating build/lib.macosx-12-arm64-cpython-39
	      creating build/lib.macosx-12-arm64-cpython-39/tokenizers
	      copying py_src/tokenizers/__init__.py -> build/lib.macosx-12-arm64-cpython-39/tokenizers
	      creating build/lib.macosx-12-arm64-cpython-39/tokenizers/models
	      copying py_src/tokenizers/models/__init__.py -> build/lib.macosx-12-arm64-cpython-39/tokenizers/models
	      creating build/lib.macosx-12-arm64-cpython-39/tokenizers/decoders
	      copying py_src/tokenizers/decoders/__init__.py -> build/lib.macosx-12-arm64-cpython-39/tokenizers/decoders
	      creating build/lib.macosx-12-arm64-cpython-39/tokenizers/normalizers
	      copying py_src/tokenizers/normalizers/__init__.py -> build/lib.macosx-12-arm64-cpython-39/tokenizers/normalizers
	      creating build/lib.macosx-12-arm64-cpython-39/tokenizers/pre_tokenizers
	      copying py_src/tokenizers/pre_tokenizers/__init__.py -> build/lib.macosx-12-arm64-cpython-39/tokenizers/pre_tokenizers
	      creating build/lib.macosx-12-arm64-cpython-39/tokenizers/processors
	      copying py_src/tokenizers/processors/__init__.py -> build/lib.macosx-12-arm64-cpython-39/tokenizers/processors
	      creating build/lib.macosx-12-arm64-cpython-39/tokenizers/trainers
	      copying py_src/tokenizers/trainers/__init__.py -> build/lib.macosx-12-arm64-cpython-39/tokenizers/trainers
	      creating build/lib.macosx-12-arm64-cpython-39/tokenizers/implementations
	      copying py_src/tokenizers/implementations/byte_level_bpe.py -> build/lib.macosx-12-arm64-cpython-39/tokenizers/implementations
	      copying py_src/tokenizers/implementations/sentencepiece_unigram.py -> build/lib.macosx-12-arm64-cpython-39/tokenizers/implementations
	      copying py_src/tokenizers/implementations/sentencepiece_bpe.py -> build/lib.macosx-12-arm64-cpython-39/tokenizers/implementations
	      copying py_src/tokenizers/implementations/base_tokenizer.py -> build/lib.macosx-12-arm64-cpython-39/tokenizers/implementations
	      copying py_src/tokenizers/implementations/__init__.py -> build/lib.macosx-12-arm64-cpython-39/tokenizers/implementations
	      copying py_src/tokenizers/implementations/char_level_bpe.py -> build/lib.macosx-12-arm64-cpython-39/tokenizers/implementations
	      copying py_src/tokenizers/implementations/bert_wordpiece.py -> build/lib.macosx-12-arm64-cpython-39/tokenizers/implementations
	      creating build/lib.macosx-12-arm64-cpython-39/tokenizers/tools
	      copying py_src/tokenizers/tools/__init__.py -> build/lib.macosx-12-arm64-cpython-39/tokenizers/tools
	      copying py_src/tokenizers/tools/visualizer.py -> build/lib.macosx-12-arm64-cpython-39/tokenizers/tools
	      copying py_src/tokenizers/__init__.pyi -> build/lib.macosx-12-arm64-cpython-39/tokenizers
	      copying py_src/tokenizers/models/__init__.pyi -> build/lib.macosx-12-arm64-cpython-39/tokenizers/models
	      copying py_src/tokenizers/decoders/__init__.pyi -> build/lib.macosx-12-arm64-cpython-39/tokenizers/decoders
	      copying py_src/tokenizers/normalizers/__init__.pyi -> build/lib.macosx-12-arm64-cpython-39/tokenizers/normalizers
	      copying py_src/tokenizers/pre_tokenizers/__init__.pyi -> build/lib.macosx-12-arm64-cpython-39/tokenizers/pre_tokenizers
	      copying py_src/tokenizers/processors/__init__.pyi -> build/lib.macosx-12-arm64-cpython-39/tokenizers/processors
	      copying py_src/tokenizers/trainers/__init__.pyi -> build/lib.macosx-12-arm64-cpython-39/tokenizers/trainers
	      copying py_src/tokenizers/tools/visualizer-styles.css -> build/lib.macosx-12-arm64-cpython-39/tokenizers/tools
	      running build_ext
	      running build_rust
	      error: can't find Rust compiler
	      
	      If you are using an outdated pip version, it is possible a prebuilt wheel is available for this package but pip is not able to install from it. Installing from the wheel would avoid the need for a Rust compiler.
	      
	      To update pip, run:
	      
	          pip install --upgrade pip
	      
	      and then retry package installation.
	      
	      If you did intend to build this package from source, try installing a Rust compiler from your system package manager and ensure it is on the PATH during installation. Alternatively, rustup (available at https://rustup.rs) is the recommended way to download and update the Rust compiler toolchain.
	      [end of output]
	  
	  note: This error originates from a subprocess, and is likely not a problem with pip.
	  ERROR: Failed building wheel for tokenizers
	Failed to build tokenizers
	ERROR: Could not build wheels for tokenizers, which is required to install pyproject.toml-based projects
	gunn@macmini ~ % pip install --upgrade pip
	DEPRECATION: Configuring installation scheme with distutils config files is deprecated and will no longer work in the near future. If you are using a Homebrew or Linuxbrew Python, please see discussion at https://github.com/Homebrew/homebrew-core/issues/76621
	Requirement already satisfied: pip in /opt/homebrew/lib/python3.9/site-packages (22.3)
	DEPRECATION: Configuring installation scheme with distutils config files is deprecated and will no longer work in the near future. If you are using a Homebrew or Linuxbrew Python, please see discussion at https://github.com/Homebrew/homebrew-core/issues/76621
	gunn@macmini ~ % pip install transformers
	DEPRECATION: Configuring installation scheme with distutils config files is deprecated and will no longer work in the near future. If you are using a Homebrew or Linuxbrew Python, please see discussion at https://github.com/Homebrew/homebrew-core/issues/76621
	Collecting transformers
	  Downloading transformers-4.24.0-py3-none-any.whl (5.5 MB)
	     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 5.5/5.5 MB 19.1 MB/s eta 0:00:00
	Collecting requests
	  Using cached requests-2.28.1-py3-none-any.whl (62 kB)
	Collecting filelock
	  Using cached filelock-3.8.0-py3-none-any.whl (10 kB)
	Requirement already satisfied: packaging>=20.0 in /opt/homebrew/lib/python3.9/site-packages (from transformers) (21.3)
	Collecting pyyaml>=5.1
	  Using cached PyYAML-6.0-cp39-cp39-macosx_11_0_arm64.whl (173 kB)
	Collecting huggingface-hub<1.0,>=0.10.0
	  Using cached huggingface_hub-0.10.1-py3-none-any.whl (163 kB)
	Collecting numpy>=1.17
	  Using cached numpy-1.23.4-cp39-cp39-macosx_11_0_arm64.whl (13.4 MB)
	Collecting regex!=2019.12.17
	  Using cached regex-2022.10.31-cp39-cp39-macosx_11_0_arm64.whl (287 kB)
	Collecting tqdm>=4.27
	  Using cached tqdm-4.64.1-py2.py3-none-any.whl (78 kB)
	Collecting tokenizers!=0.11.3,<0.14,>=0.11.1
	  Downloading tokenizers-0.13.1-cp39-cp39-macosx_12_0_arm64.whl (3.6 MB)
	     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 3.6/3.6 MB 30.2 MB/s eta 0:00:00
	Requirement already satisfied: typing-extensions>=3.7.4.3 in /opt/homebrew/lib/python3.9/site-packages (from huggingface-hub<1.0,>=0.10.0->transformers) (4.4.0)
	Requirement already satisfied: pyparsing!=3.0.5,>=2.0.2 in /opt/homebrew/lib/python3.9/site-packages (from packaging>=20.0->transformers) (3.0.9)
	Collecting certifi>=2017.4.17
	  Using cached certifi-2022.9.24-py3-none-any.whl (161 kB)
	Requirement already satisfied: idna<4,>=2.5 in /opt/homebrew/lib/python3.9/site-packages (from requests->transformers) (3.4)
	Collecting urllib3<1.27,>=1.21.1
	  Using cached urllib3-1.26.12-py2.py3-none-any.whl (140 kB)
	Collecting charset-normalizer<3,>=2
	  Using cached charset_normalizer-2.1.1-py3-none-any.whl (39 kB)
	Installing collected packages: tokenizers, urllib3, tqdm, regex, pyyaml, numpy, filelock, charset-normalizer, certifi, requests, huggingface-hub, transformers
	  DEPRECATION: Configuring installation scheme with distutils config files is deprecated and will no longer work in the near future. If you are using a Homebrew or Linuxbrew Python, please see discussion at https://github.com/Homebrew/homebrew-core/issues/76621
	  DEPRECATION: Configuring installation scheme with distutils config files is deprecated and will no longer work in the near future. If you are using a Homebrew or Linuxbrew Python, please see discussion at https://github.com/Homebrew/homebrew-core/issues/76621
	  DEPRECATION: Configuring installation scheme with distutils config files is deprecated and will no longer work in the near future. If you are using a Homebrew or Linuxbrew Python, please see discussion at https://github.com/Homebrew/homebrew-core/issues/76621
	  DEPRECATION: Configuring installation scheme with distutils config files is deprecated and will no longer work in the near future. If you are using a Homebrew or Linuxbrew Python, please see discussion at https://github.com/Homebrew/homebrew-core/issues/76621
	  DEPRECATION: Configuring installation scheme with distutils config files is deprecated and will no longer work in the near future. If you are using a Homebrew or Linuxbrew Python, please see discussion at https://github.com/Homebrew/homebrew-core/issues/76621
	  DEPRECATION: Configuring installation scheme with distutils config files is deprecated and will no longer work in the near future. If you are using a Homebrew or Linuxbrew Python, please see discussion at https://github.com/Homebrew/homebrew-core/issues/76621
	  DEPRECATION: Configuring installation scheme with distutils config files is deprecated and will no longer work in the near future. If you are using a Homebrew or Linuxbrew Python, please see discussion at https://github.com/Homebrew/homebrew-core/issues/76621
	  DEPRECATION: Configuring installation scheme with distutils config files is deprecated and will no longer work in the near future. If you are using a Homebrew or Linuxbrew Python, please see discussion at https://github.com/Homebrew/homebrew-core/issues/76621
	  DEPRECATION: Configuring installation scheme with distutils config files is deprecated and will no longer work in the near future. If you are using a Homebrew or Linuxbrew Python, please see discussion at https://github.com/Homebrew/homebrew-core/issues/76621
	  DEPRECATION: Configuring installation scheme with distutils config files is deprecated and will no longer work in the near future. If you are using a Homebrew or Linuxbrew Python, please see discussion at https://github.com/Homebrew/homebrew-core/issues/76621
	  DEPRECATION: Configuring installation scheme with distutils config files is deprecated and will no longer work in the near future. If you are using a Homebrew or Linuxbrew Python, please see discussion at https://github.com/Homebrew/homebrew-core/issues/76621
	  DEPRECATION: Configuring installation scheme with distutils config files is deprecated and will no longer work in the near future. If you are using a Homebrew or Linuxbrew Python, please see discussion at https://github.com/Homebrew/homebrew-core/issues/76621
	DEPRECATION: Configuring installation scheme with distutils config files is deprecated and will no longer work in the near future. If you are using a Homebrew or Linuxbrew Python, please see discussion at https://github.com/Homebrew/homebrew-core/issues/76621
	Successfully installed certifi-2022.9.24 charset-normalizer-2.1.1 filelock-3.8.0 huggingface-hub-0.10.1 numpy-1.23.4 pyyaml-6.0 regex-2022.10.31 requests-2.28.1 tokenizers-0.13.1 tqdm-4.64.1 transformers-4.24.0 urllib3-1.26.12
	gunn@macmini ~ % pip install torch
	DEPRECATION: Configuring installation scheme with distutils config files is deprecated and will no longer work in the near future. If you are using a Homebrew or Linuxbrew Python, please see discussion at https://github.com/Homebrew/homebrew-core/issues/76621
	Requirement already satisfied: torch in /opt/homebrew/lib/python3.9/site-packages (1.12.1)
	Requirement already satisfied: typing-extensions in /opt/homebrew/lib/python3.9/site-packages (from torch) (4.4.0)
	DEPRECATION: Configuring installation scheme with distutils config files is deprecated and will no longer work in the near future. If you are using a Homebrew or Linuxbrew Python, please see discussion at https://github.com/Homebrew/homebrew-core/issues/76621
	gunn@macmini ~ % pip install accelerate
	DEPRECATION: Configuring installation scheme with distutils config files is deprecated and will no longer work in the near future. If you are using a Homebrew or Linuxbrew Python, please see discussion at https://github.com/Homebrew/homebrew-core/issues/76621
	Collecting accelerate
	  Downloading accelerate-0.13.2-py3-none-any.whl (148 kB)
	     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 148.8/148.8 kB 2.0 MB/s eta 0:00:00
	Requirement already satisfied: pyyaml in /opt/homebrew/lib/python3.9/site-packages (from accelerate) (6.0)
	Requirement already satisfied: psutil in /opt/homebrew/lib/python3.9/site-packages (from accelerate) (5.9.3)
	Requirement already satisfied: numpy>=1.17 in /opt/homebrew/lib/python3.9/site-packages (from accelerate) (1.23.4)
	Requirement already satisfied: torch>=1.4.0 in /opt/homebrew/lib/python3.9/site-packages (from accelerate) (1.12.1)
	Requirement already satisfied: packaging>=20.0 in /opt/homebrew/lib/python3.9/site-packages (from accelerate) (21.3)
	Requirement already satisfied: pyparsing!=3.0.5,>=2.0.2 in /opt/homebrew/lib/python3.9/site-packages (from packaging>=20.0->accelerate) (3.0.9)
	Requirement already satisfied: typing-extensions in /opt/homebrew/lib/python3.9/site-packages (from torch>=1.4.0->accelerate) (4.4.0)
	Installing collected packages: accelerate
	  DEPRECATION: Configuring installation scheme with distutils config files is deprecated and will no longer work in the near future. If you are using a Homebrew or Linuxbrew Python, please see discussion at https://github.com/Homebrew/homebrew-core/issues/76621
	DEPRECATION: Configuring installation scheme with distutils config files is deprecated and will no longer work in the near future. If you are using a Homebrew or Linuxbrew Python, please see discussion at https://github.com/Homebrew/homebrew-core/issues/76621
	Successfully installed accelerate-0.13.2
	gunn@macmini ~ %
	```


	[https://colab.research.google.com/drive/1w-wLEbiwh3JqnB1TdwbYoEskbBFxNUJd#gceVm=folkloric-stone-367704/asia-northeast3-c/colab-1-vm](https://colab.research.google.com/drive/1w-wLEbiwh3JqnB1TdwbYoEskbBFxNUJd#gceVm=folkloric-stone-367704/asia-northeast3-c/colab-1-vm)


## 콘다 설치 : 맥 M1용 콘다 다운 받아서 설치


파이토치 설치 : 맥용 다운 받아서 설치 

- `pip3 install torch torchvision torchaudio`
- 설치한 후에도 import torch가 안먹힘
	- (x) `conda install pytorch torchvision torchaudio -c pytorch`
	- `conda install pytorch-cpu torchvision-cpu -c pytorch`
	- `conda install pytorch torchvision torchaudio -c pytorch-nightly`

## 로컬에서 KoGPT 실행


[https://github.com/kakaobrain/kogpt](https://github.com/kakaobrain/kogpt)


[https://huggingface.co/kakaobrain/kogpt](https://huggingface.co/kakaobrain/kogpt)


transformers 설치 오류


```javascript
Could not build wheels for tokenizers, which is required to install pyproject.toml-based projects
```


![](https://prod-files-secure.s3.us-west-2.amazonaws.com/94f51666-273a-443d-bf89-42827b5b6876/4a2134da-7b1c-461b-a612-7ecc8fb36264/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45GO43JXI4%2F20241102%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20241102T001752Z&X-Amz-Expires=3600&X-Amz-Signature=f44d43271634e309da0b46d57c4f58b769478fb0b3e31de439c956a6d5b5c498&X-Amz-SignedHeaders=host&x-id=GetObject)


러스트(c++ 유사한 것)를 설치하고,


`curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh`


`source "$HOME/.cargo/env”`


트랜스포머 설치하면, 성공


`pip install transformers~=4.12.0`


![](https://prod-files-secure.s3.us-west-2.amazonaws.com/94f51666-273a-443d-bf89-42827b5b6876/e285bbc4-3fd5-407e-b434-c818a77e9ad6/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45GO43JXI4%2F20241102%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20241102T001752Z&X-Amz-Expires=3600&X-Amz-Signature=6e6492b73245a7b7deea664007074a2838b8b24a08034b93f5b2c9a3d44e2bad&X-Amz-SignedHeaders=host&x-id=GetObject)


## 마침내 로컬에서 실행!


모델을 로딩하고,


![](https://prod-files-secure.s3.us-west-2.amazonaws.com/94f51666-273a-443d-bf89-42827b5b6876/54396faa-5b6e-4819-a5bf-382b2074ae96/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45GO43JXI4%2F20241102%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20241102T001752Z&X-Amz-Expires=3600&X-Amz-Signature=7f5b0731de575e686a93f32d14bfae67536dd643ec116c4dc6186fd6b4d1fb92&X-Amz-SignedHeaders=host&x-id=GetObject)


기사 제목을 넣어봤더니, 과거 기사를 가지고 스스로 작문한 결과를 내었다.


![](https://prod-files-secure.s3.us-west-2.amazonaws.com/94f51666-273a-443d-bf89-42827b5b6876/3f53d485-447c-49b8-b27a-0d72d2d15bbb/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45GO43JXI4%2F20241102%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20241102T001752Z&X-Amz-Expires=3600&X-Amz-Signature=c78edf42b29e1f05bce27b34eb548a95043577f1a6c26ebe92e507e588ec1841&X-Amz-SignedHeaders=host&x-id=GetObject)


CPU를 사용해서 작문시키니 100자 작문하는데도 꽤 오랜 시간이 걸린다.


그럼 M1 가속이 가능한지 해보자.


`device = torch.device('mps') # 해당 코드를 통해 device를 적용하시면 됩니다.`


M1 Pro 맥북에서 Pytorch GPU 가속


[https://velog.io/@hwanseung2/M1-Mac%EC%97%90%EC%84%9C-Pytorch-GPU-%EA%B0%80%EC%86%8D](https://velog.io/@hwanseung2/M1-Mac%EC%97%90%EC%84%9C-Pytorch-GPU-%EA%B0%80%EC%86%8D)


`device = torch.device('mps') # 해당 코드를 통해 device를 적용하시면 됩니다.`

	- 토치 디바이스는 cpu, cuda가 있는데, M1(Pro)은 `mps`
	- `mps`는 Apple의 [Metal Performance Shaders Framework](https://pytorch.org/blog/introducing-accelerated-pytorch-training-on-mac/)

[https://devocean.sk.com/blog/techBoardDetail.do?ID=163957](https://devocean.sk.com/blog/techBoardDetail.do?ID=163957)


![](https://prod-files-secure.s3.us-west-2.amazonaws.com/94f51666-273a-443d-bf89-42827b5b6876/9ea1d98b-0922-48d6-90ec-73786c98a7c5/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45GO43JXI4%2F20241102%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20241102T001752Z&X-Amz-Expires=3600&X-Amz-Signature=b3101ed26cce96864fed58347b0e2a8570469c09051c9b7e55c3bed515b52998&X-Amz-SignedHeaders=host&x-id=GetObject)


[https://www.youtube.com/watch?v=Zx2MHdRgAIc&ab_channel=DanielBourke](https://www.youtube.com/watch?v=Zx2MHdRgAIc&ab_channel=DanielBourke)


모델 로딩을 확실히 빠른데,


실행하면 아래와 같은 에러가…


![](https://prod-files-secure.s3.us-west-2.amazonaws.com/94f51666-273a-443d-bf89-42827b5b6876/972f7dda-b106-4602-9005-13c1dd19e9a7/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45GO43JXI4%2F20241102%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20241102T001752Z&X-Amz-Expires=3600&X-Amz-Signature=dd12351837b8b77e6d71bd69000e430543ed0457df85d5752aa19d31f6099277&X-Amz-SignedHeaders=host&x-id=GetObject)


topk on mps for k ≤16을 해결 필요


어떻게 해결할까?


[https://pytorch.org/docs/stable/generated/torch.topk.html#torch-topk](https://pytorch.org/docs/stable/generated/torch.topk.html#torch-topk)


[https://github.com/facebookresearch/detectron2/issues/4342](https://github.com/facebookresearch/detectron2/issues/4342)


[https://stackoverflow.com/questions/72681606/runtimeerror-currently-topk-on-mps-works-only-for-k-16-in-apple-silicon-gpu-d](https://stackoverflow.com/questions/72681606/runtimeerror-currently-topk-on-mps-works-only-for-k-16-in-apple-silicon-gpu-d)


[https://github.com/pytorch/pytorch/issues/78915](https://github.com/pytorch/pytorch/issues/78915)


[https://github.com/pytorch/pytorch/pull/79677](https://github.com/pytorch/pytorch/pull/79677)


[https://mingyu6952.tistory.com/entry/Anaconda-가상환경-확인생성활성화설치패키지-확인비활성화삭제](https://mingyu6952.tistory.com/entry/Anaconda-가상환경-확인생성활성화설치패키지-확인비활성화삭제)

