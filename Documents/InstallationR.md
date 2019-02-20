 ## Install the complete R & RStudio in Your Machine 

### 1. Ubuntu version 12.04 (or higher)    
   -R version 3.0.1 or higher
   
   <code>$ sudo apt-get update </code>

   <code>$ sudo apt-get install r-base</code>

  - RStudio Server version 1.1.463

<code>$ sudo apt-get install gdebi-core</code>

<code>$ wget https://download2.rstudio.org/rstudio-server-1.1.463-amd64.deb</code>

<code>$ sudo gdebi rstudio-server-1.1.463-amd64.deb</code>

### 2. Debian 9+
  -R version 3.0.1 or higher 
  
<code>$ sudo apt-get update</code>

<code>$ sudo apt-get install r-base</code>

  - RStudio Server version 1.1.463

<code>$ sudo apt-get install gdebi-core</code>

<code>$ wget https://download2.rstudio.org/rstudio-server-stretch-1.1.463-amd64.deb</code>

<code>$ sudo gdebi rstudio-server-stretch-1.1.463-amd64.deb</code>

### 3. RedHat/CentOS 6 and 7
R version 3.0.1 or higher

<code>$ yum update</code>

<code>$ yum install epel-release</code>

<code>$ yum install R </code>

### RStudio Server version 1.1.463

<code>$ wget https://download2.rstudio.org/rstudio-server-rhel-1.1.463-x86_64.rpm</code>

<code>$ sudo yum install rstudio-server-rhel-1.1.463-x86_64.rpm</code>


### Start RStudio Server for all OS

<code>$  systemctl status rstudio-server.service </code>

<code>$ systemctl is-enabled rstudio-server.service</code>

### Display information about R
<code>$ yum info R</code>


### Search your computer Hostname
<code>$ hostname </code>

### Copy user hostname paste in your browser 
Hostname:XXXX

### Login username and password

### Installation dplyr & tidyverse

<code>$ install.packages("devtools")</code>

<code>$ install.packages("dplyr", dependencies=TRUE)</code>

### To load dplyr
<code>$ library(dplyr)</code>

<code>$install.packages("tidyverse",dependencies=TRUE)</code>
 
### To load tidyverse
<code>$ library(tidyverse)</code>

