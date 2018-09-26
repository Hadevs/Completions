# Completions
Very simple completions for using it with any type of variable.
![alt text](preview.png)

### Examples

```swift
// 1.
let stringClosure: ItemClosure<String> = {
	value in
	print("This works: \(value)")
}

stringClosure("Hi")

//2.
func sendRequest(with completion: OptionalItemClosure<AnswerResponse>) {
  request { data in
		completion(try? AnswerResponse.from(data))
	}
}

sendRequest(with: {
  response in

})

```
