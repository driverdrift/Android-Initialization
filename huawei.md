# third-party app
```
for pkg in $(pm list packages -3 | cut -d':' -f2 | grep -Ev '^(io\.github\.muntashirakon\.AppManager|com\.google\.android\.inputmethod\.latin)'); do
	echo "Trying to unistall: $pkg"
	pm uninstall "$pkg"
done
```
# system app
