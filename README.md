framework-standard-edition
==========================

Symfony框架标准版

**使用文檔**

* [安裝](#installation)

**Bundle開發文檔**

<a name="installation"></a>

### 安裝

#### 1) 創建項目

```bash
composer create-project wiz/framework-standard-edition . -s dev
```

#### 2) 加載Bundle（https://packagist.wizmacau.com/）

選擇所需Bundle，具體請參考下面的安裝文檔。

> **注意:**
> 使用以下bundle請確保已在項目根目錄composer.json文件中已加入repositories路徑。

----------

    "repositories": [
        {
            "type": "composer",
            "url": "http://packagist.wizmacau.com"
        }
    ]
    
----------

[查看 WizCmsBundle 安裝文檔](https://github.com/wizmacau/framework-standard-edition/blob/master/app/Resources/doc/install/cms-bundle.md)

#### 3) 完成部署

```bash
# 更新數據表，請確定app/config/parameter.yml數據參數正確並且數據庫存在
app/console doctrine:schema:update --force

# 創建管理員賬號
app/console fos:user:create --super-admin
```
