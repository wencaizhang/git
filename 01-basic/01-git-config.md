
# 配置命令

## 设置用户名和邮箱
#### 设置用户名

```bash
git config --global user.name "your name"
```
 
#### 设置用户邮箱

```bash
git config --global user.email "your email"
``` 
 
 
#### 查看用户名

```bash
git config user.name
```
#### 查看邮箱

```bash
git config user.email
```
## 设置代理

#### 设置代理
```bash
git config --global http.proxy http://demo.com:8080
```

#### 查看代理
```bash
git config --global --get --global http.proxy
```

#### 取消代理
```bash
git config --global --unset http.proxy
```

## 查看git 设置列表信息

```bash
git config --global list
```
