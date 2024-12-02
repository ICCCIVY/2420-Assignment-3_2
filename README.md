# 2420-Assignment-3_2
## Task 1 Create two new digital ocean droplets
1. Created two droplets on digital ocean:
![droplets](images/droplets.png)
2. ssh into each droplets
- web-server-1:
```
ssh -i .ssh/2420assign1 arch@143.198.145.186
```
- web-server-2:
```
ssh -i .ssh/2420assign1 arch@64.23.218.96 
```
## Task 2 Creat load balancer
![load](images/load.png)
  - The status show down because I have not start nginx yet.

## Task 3 Clone the updated starter code (the following command also ran in web-arch-1)
1. Re-create the webgen user for each server using instruction from part 1.
```
sudo useradd --system -d /var/lib/webgen -s /usr/bin/nologin webgen
```
```
sudo chown -R webgen:webgen /var/lib/webgen
```
```
sudo mkdir -p /var/lib/webgen/bin
```
```
sudo mkdir -p /var/lib/webgen/HTML
```
Adding new directory documents
```
sudo mkdir -p /var/lib/webgen/documents
```
2. Clone updated generate_index file
![clone](images/generate_index.png)
3. Create file-one and file-two under documents directory. 
```
sudo vim file-one
```
```
sudo vim file-two
```
I put simple content inside these two files.
![content](images/content.png)

4. Set correct ownership
```
sudo chown webgen:webgen /var/lib/webgen/documents/file-one
```
5. Run the generate_index script to create index.html
```
sudo ./generate_index 
```
![index](images/index.png)
6. Verify
![tree](images/tree.png)




