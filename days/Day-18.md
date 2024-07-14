# Learned
### Information Gathering (Reconnaissance)
 - Hunting Subdomains  
 - Validate Subdomain

# A Few Details
### Hunting Subdomains
Sublis3r  
 `sublis3r -d example.com`  

Amass  
 `amass -enum -d example.com`  

Subfinder  
 `subfinder -d example.com`  

Assetfinder  
 `assetfinder example.com`  

crt.sh  
> search queary: %.example.com `% is wildcard`  

### Validate Subdomain
httprobe  
 `httprobe -prefer-https | grep https > file.txt`  
 

