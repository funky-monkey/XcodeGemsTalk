## depcheck

[Download depcheck](https://github.com/wojteklu/depcheck)

Add extra buildphase with script:

```swift
if which depcheck >/dev/null; then
  depcheck
else
  echo "warning: depcheck not installed, download from https://github.com/wojteklu/depcheck"
fi
```

###Run:

**analyze**:  
`depcheck analyze --project ProjectName.xcodeproj`

**usage**:  
`depcheck usage --project ProjectName.xcodeproj`

**graph**: 
Shows nice exported graph of classes used. 
`depcheck graph --project ProjectName.xcodeproj`
