# pyclrs
Print color on Linux or Windows terminals.

<br>

# 1. Install

```bash
pip install pyclrs
```
![install](https://github.com/liuhedong135/pyclrs/blob/master/photo/install.gif)
<br>



---

<br>

# 2. Functions
```python
from pyclrs.color import Use
c = Use('Hello World')
``` 

## 2.1 Color

- **black** 
  - *`c.backblack()`* or *`c.foreblack`*
- **red**   
  - *`c.backblack()`* or *`c.foreblack`*
- **green** 
  - *`c.backblack()`* or *`c.foreblack`*
- **yellow** 
  - *`c.backblack()`* or *`c.foreblack`*
- **blue**
  - *`c.backblack()`* or *`c.foreblack`*
- **nagebta** 
  - *`c.backblack()`* or *`c.foreblack`*
- **cyan** 
  - *`c.backblack()`* or *`c.foreblack`*
- **white** 
  - *`c.backblack()`* or *`c.foreblack`*

<br>

## 2.2 Mode

- **default**
  - *`c.default()`*
- **highlight**
  - *`c.highlight()`*
- **underline**
  - *`c.underline()`*
- **twinkle**
  - *`c.twinkle()`*
- **hide**
  - *`c.hide()`*
- **excute**
  - *`c.excute()`*

<br>

---

<br>

# 3. Example

<br>

## 3.1 Simple Use

![simple](https://github.com/liuhedong135/pyclrs/blob/master/photo/simple.gif)

```python
from pyclrs.color import Use

p1 = Use('Hello World')
print(p1.excute())

p2 = Use('Hello World')
p2.backred()
p2.foreblack()
print(p2.excute())

p3 = Use('Hello World')
p3.forered()
p3.twinkle()
print(p3.excute())
```

<br>

## 3.2 Check the state of server

![check](https://github.com/liuhedong135/pyclrs/blob/master/photo/check.gif)

```python
from pyclrs.color import Use

title = Use('%-17s%-10s%-10s'%("Ipaddr","Server","Status"))
title.backcyan()
title.foreblack()
redis = Use('%-10s'%'Started')
redis.backwhite()
redis.foregreen()
mysql = Use('%-10s'%'Stopped')
mysql.backwhite()
mysql.forered()
mysql.twinkle()
httpd = Use('%-10s'%'Unknown')
httpd.backwhite()
httpd.foreyellow()
addr1 = Use('%-17s%-10s'%('192.168.100.100','redis'))
addr1.backwhite()
addr1.foreblack()
addr2 = Use('%-17s%-10s'%('192.168.100.101','mysql'))
addr2.backwhite()
addr2.foreblack()
addr3 = Use('%-17s%-10s'%('192.168.100.102','httpd'))
addr3.backwhite()
addr3.foreblack()

print(title.excute())
print(addr1.excute()+redis.excute())
print(addr1.excute()+mysql.excute())
print(addr1.excute()+httpd.excute())
```
