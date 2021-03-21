# react-native-ez-storage

A JSON-Based react native storage system!

### Install

```
npm install --save react-native-ez-storage
```

### Usage

```javascript
import Store from "react-native-ez-storage";

Store.set("numberValue", 1);
Store.set("stringValue", "Hi");
Store.set("objectValue", { key: "value" });

Store.get("numberValue").then((v) => v === 1);
Store.get("stringValue").then((v) => v === "Hi");
Store.get("objectValue").then(({ key }) => key === "value");

Store.remove("numberValue");

Store.merge("objectValue", { key2: "value2" });

Store.multiSet({ key1: "key1Value", key2: "key2Value" });
Store.multiGet(["key1", "key2"]).then(
  ({ key1, key2 }) => key1 === "key1Value" && key2 === "key2Value"
);
Store.multiRemove(["key1", "key2"]);
Store.multiMerge({ key3: { a: 1 }, key4: { b: 2 } });
```

### Dependencies

- [@react-native-community/async-storage](https://react-native-async-storage.github.io/async-storage/)
