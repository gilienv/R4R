 Install the complete R & RStudio in Your Machine 

1. Ubuntu version 12.04 (or higher)    
R version 3.0.1 or higher
$ sudo apt-get update
$ sudo apt-get install r-base
RStudio Server version 1.1.463
$ sudo apt-get install gdebi-core
$ wget https://download2.rstudio.org/rstudio-server-1.1.463-amd64.deb
$ sudo gdebi rstudio-server-1.1.463-amd64.deb
2. Debian 9+
R version 3.0.1 or higher 
$ sudo apt-get update
$ sudo apt-get install r-base

RStudio Server version 1.1.463
$ sudo apt-get install gdebi-core
$ wget https://download2.rstudio.org/rstudio-server-stretch-1.1.463-amd64.deb
$ sudo gdebi rstudio-server-stretch-1.1.463-amd64.deb
3. RedHat/CentOS 6 and 7
R version 3.0.1 or higher
$ yum update
$ yum install epel-release
$ yum install R 

RStudio Server version 1.1.463
$ wget https://download2.rstudio.org/rstudio-server-rhel-1.1.463-x86_64.rpm
$ sudo yum install rstudio-server-rhel-1.1.463-x86_64.rpm


Start RStudio Server for all OS
$  systemctl status rstudio-server.service 
$ systemctl is-enabled rstudio-server.service

Display information about R
$ yum info R


Search your computer Hostname
$ hostname 

Copy user hostname paste in your browser 
Hostname:8787

Login username and password
Installation dplyr & tidyverse
$ install.packages("devtools")
$ install.packages("dplyr", dependencies=TRUE)
To load dplyr
$ library(dplyr)

$install.packages("tidyverse",dependencies=TRUE)
To load tidyverse
$ library(tidyverse)

