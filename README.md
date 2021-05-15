A language and compiler for writing Firestore security rules. The compiler also generates TypeScript interfaces. The main idea is to be able to add idiomatic type validation to routes, as if they had strict type-checking. The language also has some nice features to elegantly express rules for certain situations, which otherwise would be too cumbersome to encode.

This is a fork of [Fireward](https://github.com/bijoutrouvaille/fireward).

## Changes
- Forbids `readonly` fields to update ever.
- Trim some unnecessary rules (to me), to avoid hitting the firestore rule size limit.
- Fix missing object, when `resources` are not set.
- Accessing fields with the `Map.get` instead of calling field's name on the map.
