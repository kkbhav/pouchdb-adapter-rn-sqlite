pouchdb-adapter-rn-sqlite
======

PouchDB adapter using ReactNative SQLite as its backing store.

### Prerequisites

- [pouchdb-react-native](https://github.com/stockulus/pouchdb-react-native)
- A SQLite module
  - [react-native-sqlite-2 (recommended)](https://github.com/noradaiko/react-native-sqlite-2)
  - [react-native-sqlite-storage](https://github.com/andpor/react-native-sqlite-storage)

### Usage

Install from npm:

```bash
npm install pouchdb-react-native pouchdb-adapter-react-native-sqlite --save
react-native install react-native-sqlite-2
```

Then `import` it, notify PouchDB of the plugin, and initialize a database using the `react-native-sqlite` adapter name:

```js
import PouchDB from 'pouchdb-react-native'
import SQLite from 'react-native-sqlite-2'
import SQLiteAdapterFactory from 'pouchdb-adapter-rn-sqlite'

const SQLiteAdapter = SQLiteAdapterFactory(SQLite)
PouchDB.plugin(SQLiteAdapter)
const db = new PouchDB('mydb.db', {adapter: 'react-native-sqlite'});
```

## Changelog

- 1.0.0
  + Initial release
