# MaaResourcesSync

适用于Windows平台的Maa资源增量更新脚本，基于 Git `SSH Fetch` 方案。  
速度不一定快，但能用。

[MaaResources镜像仓库](https://github.com/LaviniaFalcone/MaaResourceMirror) | [下载地址](https://github.com/LaviniaFalcone/MaaResourceSync/releases)

## 常见问题

### 这个东西有什么用
> 用于更新 `Maa` 自动战斗等功能所需的资源等。

### 如何使用 
> 解压到 `Maa` 所在目录，运行 `sync.bat` 即可更新资源。


### 资源下载速度慢
> 如果实在是太慢（`≤100KB/s`）可以试试关掉脚本重新打开。

### 其它问题
> 请提交 [Issue](https://github.com/LaviniaFalcone/MaaResourceSync/issues)

## 如何修改更新源
如果你想让MRS从自己的仓库拉取更新，可以把公钥添加到自己仓库的 `Deploy keys` 列表中，然后将 `sync.bat` 中的：
```shell
git remote add mirror git@github.com:LaviniaFalcone/MaaResourceMirror
```
更改为：
```shell
git remote add mirror YOUR_REPO_SSH_URL
```

### [SSH 公钥](https://github.com/LaviniaFalcone/MaaResourceSync/blob/main/id_rsa.pub)
```
ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAACAQDNlkaeJHkuXs9Bkd8friq5yQ8Q+hHIdj1/dbVJbmzWWhN0A1JEJniRO7t08wj0RaTZeHOfSYnbpA5nBYFoYse5TyMeOCwMH8LaWdAhplteOoTmDUX9IGMDdToeV8ijqE5mN4L6rB5W8gtpA0prfUDwCHcBUeptRnqaiz1W0noodOWhEDbcCKJhc2/zsYkcm9bpQmy39tgPRJK1zE3l7wE6JAfEM81PQMUgtY7KVar2mv0DbPwvlPVKjau/3Yw4lcXvXdOcg6LsK/lsrxi37Zt5wqviqLU0GwNbinUyF4DL8Tq5xt95qMsbk6am9PGn/G54UdgRp87wrqcyoYLEVYxxNI7Vve/G5JWNUW/1UWiJUJIb7O0/v1286c5qdNIOxeRFq+bf0MpdCewzPDin4QJipzNCWVwhX+26eEuJrtMJLVBWdXkwJGZhRTj33i96+KyE+r5qEEul+0GTLns33YMr0iekMGS83K3PLAMJtvW5QZQua3dvu+b3moNKAcHyI0BRYxBA9saKsO34O1x6Y5vcykpaFm8aOGY7KeI8686mbyecohzZPqYld2tQCxO9sdF9LIxi0Y10IK9gjC2YSGGTDKveMvR/2O6U7eO9d68sgPqqgVgV+hewj0iNH7Lk/xQbx/HZ/W+uhC5jgOkXDsP5wHoetE6Dn1Fl9psE90HIVQ==
```
