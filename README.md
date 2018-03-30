## **INFOS**
This is the bash script I wrote to auto-update https://vote.ripaex.io each 2 minutes.
Current version: v1.2

## **REQUIREMENTS**

Install packages: **wget**, **curl**, **sed**, **[jq](https://stedolan.github.io/jq/)** and **[bc](https://www.gnu.org/software/bc/manual/html_mono/bc.html)**

**Ubuntu:** `sudo apt-get install -y wget curl sed jq bc`

**CentOS:** `sudo yum install -y wget curl sed jq bc`

**[ripa-node](https://github.com/RipaEx/ripa-node)** installed and sync. on port 5500 on local server.

A functional local web server like **[nginx](https://www.nginx.com/)** or **[apache](http://httpd.apache.org/)**  to share the generated report.


## **INSTALL**

#### **Download the script**

> wget https://raw.githubusercontent.com/RipaEx/ripa-vote/master/TxtVoteReport.sh -O ~/TxtVoteReport.sh

#### **Make it executable**

> chmod 700 ~/TxtVoteReport.sh

## **CONFIGURE**

Edit the script to customize the OutputFile variable value.

> OutputFile='/var/www/html/index.txt'


## **ADD CRONJOB**

```
crontab -e

#----------------------------------
*/2 * * * * ~/TxtVoteReport.sh
#----------------------------------
```
