List of devices attached
```
adb devices
```

```
adb shell
```

```
pm list packages
```

List third-party packages
```
pm list packages				# List all installed packages
pm list packages -s				# List only system packages
pm list packages -3				# List only third-party (user-installed) packages
pm list packages -3 | wc -l		# wc (word count), -l (Lines)
pm list packages -f				# List packages with their associated file paths.
```
