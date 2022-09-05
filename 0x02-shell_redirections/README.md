echo Hello, World
echo "\"(Ôo)'"
cat /etc/passwd
cat /etc/passwd /etc/hosts
tail /etc/passwd
head /etc/passwd
head --lines=3 iacta | tail --lines=1
echo "Best School" > "\*\\\'\"Best School\"\'\\\*$\?\*\*\*\*\*:)"
ls -la > ls_cwd_content
echo -en "" | tail --lines=1 iacta >> iacta
find . -name '*.js' -type f -delete
find -mindepth 1 -type d | wc -l
ls -t | head
sort | uniq -u
grep -i root /etc/passwd
grep -i bin /etc/passwd | wc -l
grep -iA 3 root /etc/passwd
grep -iv bin /etc/passwd
grep -i "^[a-z]" /etc/ssh/sshd_config
tr Ac Ze
tr -d cC
rev
cut -d':' -f1,6 /etc/passwd | sort
find . -empty -printf "%f\n"
find -type f -name "*.gif" -printf "%f\n" | rev | cut -d'.' -f 2- | rev | LC_ALL=C sort -f
cut -c 1 | tr -d '\n' | sort
tail -n +2 | cut -f1 | sort | uniq -c | sort -nr | head -11 | tr -s ' ' | cut -d' ' -f3
