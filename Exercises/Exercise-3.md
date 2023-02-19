<details><summary><b>List all files in the current directory and its subdirectories recursively, including hidden files and directories, sorted by size in descending order</b></summary><br>

```bash
$ find . -type f -o -type d -iname ".*" -print0 | xargs -0 du -hc | sort -hr
```
</details>

<details><summary><b> Find all files in the current directory and its subdirectories that contain the word "ERROR" in them</b></summary><br>

```bash
$ grep -r "ERROR" .
```
</details>

<details><summary><b>Count the number of lines in all .txt files in the current directory</b></summary><br>

```bash
$ find . -name "*.txt" -exec wc -l {} + | awk '{sum+=$1} END {print sum}'
/home/user/dir1
```
</details>

<details><summary><b>Print the 10 largest files in the current directory and its subdirectories</b></summary><br>

```bash
$ find . -type f -printf "%s\t%p\n" | sort -nr | head -10
```
</details>

<details><summary><b>Print the number of files in the current directory and its subdirectories</b></summary><br>

```bash
$ find . -type f | wc -l
```
</details>

<details><summary><b>Remove all files in the current directory that end with the .bak extension/b></summary><br>

```bash
$ find . -name "*.bak" -delete
```
</details>
