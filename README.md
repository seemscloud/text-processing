#### `second column`
```bash
echo -e "Lorem\tipsum\tdolor\tsit\tamet" | awk '{print $2}'
```

#### `culumn via cut`
```bash
echo -e "Lorem\tipsum\tdolor\tsit\tamet" | cut -d" " -f1
echo -e "Lorem\tipsum\tdolor\tsit\tamet" | cut -d$'\t' -f3
echo -e "Lorem\tipsum\tdolor\tsit\tamet" | cut -d$'\t' -f1-2
```

#### `sort / uniq`
```bash
cat file.txt | sort | uniq
cat file.txt | sort | uniq -c 
```

##### `head / tail`
```bash
cat /etc/passwd | tail -n +3

cat /etc/passwd  | head -n -2
```

##### `sed`
```bash
echo "Seems Cloud" | sed "s/Seems/sEEMS/g"
echo "Seems Cloud" | sed "s|Seems|sEEMS|g"
```

##### `python2 URI encode / decode`
```bash
alias urlencode='python2 -c "import urllib, sys; print urllib.quote(sys.argv[1] if len(sys.argv) > 1 else sys.stdin.read()[0:-1])"'
alias urldecode='python2 -c "import urllib, sys; print urllib.unquote(sys.argv[1] if len(sys.argv) > 1 else sys.stdin.read()[0:-1])"'
```

##### `python3 URI encode`
```bash
alias urlencode='python3 -c "from urllib import parse; import sys; print(parse.quote(sys.argv[1] if len(sys.argv) > 1 else sys.stdin.read()[0:-1]))"'
alias urldecode='python3 -c "from urllib import parse; import sys; print(parse.unquote(sys.argv[1] if len(sys.argv) > 1 else sys.stdin.read()[0:-1]))"'
```
