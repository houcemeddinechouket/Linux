## Search for files
  <details><summary><b>Search in /etc all file/directories with host in their name</b></summary><br>

  ```bash
  find /etc -name "\*host*"`
```
 </details>
 <details><summary><b>Search from current position all files/directories with permissions 777 and after remove them</b></summary><br>
 
  ```bash
find . -perm 777 -exec rm -f '{}' \;
```
 </details>
 <details><summary><b> Search in /etc all files/directories with size less of 100 kilobytes</b></summary><br>

```bash
find /etc -size -100k
   ```
 </details>
  <details><summary><b>Search starting from current position, descending maximum three directories levels, files with size major of 2 megabyte</b></summary><br>

```bash

find . -maxdepth 3 -type f -size +2M
```

</details>

<details><summary><b>Find all files that have same i-node of file</b></summary><br>

```bash
find . -samefile file
```
 </details>
<details><summary><b>Show all files that aren't owned by user owner</b></summary><br>

```bash
find . \! -user owner
 ```
 </details>

<details><summary><b>Search name ignoring case</b></summary><br>

```bash
find . -iname name
  ```
</details>

<details><summary><b>Find all files with permissions equal to 222. E.g. only file with permissions 222 will be showed</b></summary><br>

```bash
find . -perm 222
  ```
 </details>
<details><summary><b>Find all files with at least permissions 222. E.g. 777 match as valid.</b></summary><br>

 ```bash
find . -perm -222
  ```
 </details>

<details><summary><b>Find all files with write for owner or write for group or write for others (at least one)</b></summary><br>

```bash
find . -perm /222
  ```
 </details>
<details><summary><b>Find all files with at least  permission write for group</b></summary><br>

```bash
find . -perm -g=w
  ```
 </details>
<details><summary><b>Show all files accessed at least two days ago (more than 24 hours)</b></summary><br>

```bash
find . -atime +1 
```
 </details>

