##SwiftLint

[Download SwiftLint](https://github.com/realm/SwiftLint)

Add extra buildphase with script:

```swift
if which swiftlint >/dev/null; then
  swiftlint
else
  echo "warning: SwiftLint not installed, download from https://github.com/realm/SwiftLint"
fi
```
### Rules
**disable**:  
`// swiftlint:disable <rule_name>`

**enable**:  
`// swiftlint:enable <rule_name>`
