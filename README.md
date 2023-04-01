# CertificateIdentification
IDCard LicensePlate Passport DrivingLicense VehicleLicense HomeReturnPermit Recaptcha etc 身份证、车牌、护照、驾驶证、行驶证、回乡证、携程验证码（深度学习）等识别


## 携程验证码的样式
### 目前携程的验证码分类
- 缺口拖拽类型： 验证码包含两张图片，一张是缺口部分，一张是背景底图，需要将缺口图片拖拽到背景中缺口的对应位置；
- 图形点选类型：验证码包含两张图片，一张是上面部分题目（请点击下面的****），一张是下面的背景图片，背景图片中散落着一些**形状类型**，需要将上面部分的图形，完美匹配下面的目标；
- 文字点选类型：验证码包含两张图片，一张是上面部分题目（请点击下面的****），一张是下面的背景图片，背景图片中散落着一些**文字类型**，需要将上面部分的文字，完美陪陪下面的目标；

下面是具体的展示以及相应的访问代码： 
#### 拖拽验证码
![0_0](https://user-images.githubusercontent.com/112738714/229259758-c4354975-4639-41fc-902e-f41dd3a5df0c.png)
![0_1](https://user-images.githubusercontent.com/112738714/229259755-6ff894e1-a96e-4d18-8b73-43f8d42944aa.png)

```python
import requests

url = "https://frp-cup.top:63320/predict"

payload={'nMsgType': '200',
'sU': 'hello_verify',
'sP': 'hello_verify',
'sS': '0',
'Category': '100',
'SubCategory': '0'}
files=[
  ('img_upper',('0_0.png',open('前面小图片.png','rb'),'image/png')),
  ('img_bottom',('0_1.png',open('后面大图片.png','rb'),'image/png'))
]
headers = {}

response = requests.request("POST", url, headers=headers, data=payload, files=files)

print(response.text)
```


#### 形状点选验证码
![227715190-02bcb9e3-85e0-4612-9f4a-a51345263033](https://user-images.githubusercontent.com/112738714/229259904-03db8276-8c7b-4bdb-9b77-cf61fa4709aa.png)
![227715197-e09f9d7d-2fdf-47c4-80f0-40ac59482ae2](https://user-images.githubusercontent.com/112738714/229259908-8e74f563-b9e4-45d8-80a1-e208472fc06f.png)

```python
import requests

url = "https://frp-cup.top:63320/predict"

payload={'nMsgType': '200',
'sU': 'hello_verify',
'sP': 'hello_verify',
'sS': '0',
'Category': '100',
'SubCategory': '898'}
files=[
  ('img_upper',('0_0.png',open('前面小图片.png','rb'),'image/png')),
  ('img_bottom',('0_1.png',open('后面大图片.png','rb'),'image/png'))
]
headers = {}

response = requests.request("POST", url, headers=headers, data=payload, files=files)

print(response.text)
```

#### 文字点选验证码
![227715243-f961b4e2-4152-4c33-94e0-af4e4de2a714](https://user-images.githubusercontent.com/112738714/229259933-3aa6eddf-4774-44ca-8399-107f2611b567.jpg)
![227715252-d115ed32-b95c-4d42-94d6-f8628ea41d27](https://user-images.githubusercontent.com/112738714/229259934-72502e37-b7ad-4a35-b065-4157c4a7d55a.jpg)


```python
import requests

url = "https://frp-cup.top:63320/predict"

payload={'nMsgType': '200',
'sU': 'hello_verify',
'sP': 'hello_verify',
'sS': '0',
'Category': '100',
'SubCategory': '989'}
files=[
  ('img_upper',('0_0.png',open('前面小图片.png','rb'),'image/png')),
  ('img_bottom',('0_1.png',open('后面大图片.png','rb'),'image/png'))
]
headers = {}

response = requests.request("POST", url, headers=headers, data=payload, files=files)

print(response.text)
```


目前携程验证码的识别率平均能达到 95+%，欢迎大家技术交流、使用，可以加邮箱、或者微信

## 身份证识别
![v2-83751f78d2f781854766bd030e2bd5bf_1440w](https://user-images.githubusercontent.com/112738714/229268471-b9f02acc-cd5f-43f9-a6e8-87ba60b10d65.jpg)
```python
import requests

url = "https://frp-cup.top:63320/predict"

payload={'nMsgType': '200',
'sU': 'hello_verify',
'sP': 'hello_verify',
'sS': '0',
'Category': '200',
'SubCategory': '0'}
files=[
  ('image',('1440w.jpg',open('身份证图片.jpg','rb'),'image/jpeg'))
]
headers = {}

response = requests.request("POST", url, headers=headers, data=payload, files=files)

print(response.text)
```

## 车牌识别
![7a9d7d014d8446232b1de5b89a689a96](https://user-images.githubusercontent.com/112738714/229269469-62935cda-c29d-451b-bda0-d0b5d1767ad6.jpeg)

```python
import requests

url = "https://frp-cup.top:63320/predict"

payload={'nMsgType': '200',
'sU': 'hello_verify',
'sP': 'hello_verify',
'sS': '0',
'Category': '0',
'SubCategory': '0'}
files=[
  ('image',('2fd.jpeg',open('车牌图片.jpeg','rb'),'image/jpeg'))
]
headers = {}

response = requests.request("POST", url, headers=headers, data=payload, files=files)

print(response.text)
```
**ghost_man_evil@126.com**
**w_|_x: tinalee_muzi**

![小城生活-30](https://user-images.githubusercontent.com/112738714/229260608-498a7c6a-70cb-4995-9d04-6f307ba24d24.jpg)

