# Glamour Book

A new Flutter project.

## Getting Started

### For localisation, run the command: 
```
flutter gen-l10n --arb-dir=assets/l10n
```

### For get_id and injectable, run either of the commands:

Use the watch flag to watch the files' system for edits and rebuild as necessary.
```
flutter packages pub run build_runner watch
```

If you want the generator to run one time and exits use
```
flutter packages pub run build_runner build --delete-conflicting-outputs    
```

Make sure you always Save your files before running the generator, if that does not work you can always try to clean and rebuild.
```
flutter packages pub run build_runner clean
```

### Git fetch all remote branches for tracking locally, pull them
```
git branch -r | grep -v '\->' | sed "s,\x1B\[[0-9;]*[a-zA-Z],,g" | while read remote; do git branch --track "${remote#origin/}" "$remote"; done
git fetch --all
git pull --all
```

### For running in ios devices
Navigate to ios directory, then run
```
pod deintegrate
pod install
```

For M1 devices,
install ffi first
```
sudo arch -x86_64 gem install ffi
```
then
```
pod deintegrate
arch -x86_64 pod install
```

