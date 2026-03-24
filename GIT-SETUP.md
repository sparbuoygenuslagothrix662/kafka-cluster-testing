# Git setup for this repository

Set author identity only for this repository:

```bash
cd /path/to/kafka-cluster-testing
git config user.name "Anatoly Slobozhanov"
git config user.email "your@email.com"
```

Check the effective values:

```bash
git config user.name
git config user.email
git config --list --show-origin
```
