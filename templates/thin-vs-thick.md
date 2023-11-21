# Thin vs Thick Packages
### Overview
  - Packages are deemed **Thin** or **Thick** via their package.toml
###### Prerequisite
- [Full understanding of package.toml]()
  
### Thick Package
  - This is the default package upload format.
###### Con
  - Takes up most disk space on Users machine
###### Format
  ```
  [[package.windows-aarch64.packman]]
name = "package1"
url = "https://myBucket.s3.amazonaws.com/packman/package1/4.0.1/windows-aarch64/package.zip"
location = "${base}"

[[package.windows-aarch64.packman]]
name = "package2"
url = "https://myBucket.s3.amazonaws.com/packman/package2/1.0.1/windows-aarch64/package.zip"
location = "${base}"
  ```
### Thin Package
  - This is the default package upload format.
###### Pro
  - Common packages are not download twice, thus saving Users disk space.
###### Format
  ```
[[package.windows-x86_64.packman]]
name = "Create"
url = "https://tmp-toml-database.s3.us-east-2.amazonaws.com/tmp1.zip"
main = true
location = "${base}"

[[package.windows-x86_64.packman]]
name = "ext1"
url = "https://tmp-toml-database.s3.us-east-2.amazonaws.com/tmp2.zip"
main = false
location = "${base}/abc/extension1"

  ```  