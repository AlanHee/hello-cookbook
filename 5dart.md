### Dart
An approachable, portable, and productive language for high-quality apps on any platform 

- assert (condition, optionalMessage)
* onle bool ture is ture
* init var is NULL

### language speical
```
// ?. 判断是否为空    ?? when left is false then 
bool out = outgoing[a]?.contains(b) ?? false; //

List foo = []
  ..add('far')
  ..add('foo')
  ..toList();
```

### JSON convert 
```
final packageJson = json.decode(packageResponse.body) as Map<String, dynamic>;
return PackageInfo.fromJson(packageJson);
```

### load json file
```
import 'dart:io';
import 'dart:convert';
final List films = json.decode(File('films.json').readAsStringSync()); 
final id = 1;
final flim = films.firstWhere((flim) => flim['id'] == id);
if(flim !=null){ 
	//...
}
```

### create flutter plugin
```dart
flutter create --org org.alan.com --template plugin my_flutter_plugin
// publish before check
flutter pkcages pub publish --dry-run
// publish it
flutter packages pub publish
```
### JSON Schema是描述你的JSON数据格式
