# ilib-localematcher

Represent a locale matcher instance, which is used
to see which locales can be matched with each other in
various ways.

## Installation

```
npm install ilib-localematcher

or

yarn add ilib-localematcher
```

## The LocaleMatcher Class

The LocaleMatcher class does the following things:

* get the most likely full locale for a partial locale
    * also get a minimal version of that full locale
* compare two locales together to see how well they match
* find region containment information
    * which UN.49 region a country is in. For example, Japan
      is in East Asia.
    * which larger UN.49 regions a smaller UN.49 region is in.
      For example, East Asia is in Asia.
* find the smallest common UN.49 region that two regions are both in
    * for example, the smallest common region between Japan
    and India is "Asia".
* find the macrolanguage for those language codes that represent a
  subtype of a macrolanguage
    * a macrolanguage is a collection of very closely related
      languages, a little further apart than dialects, but not
      quite distinct enough to be considered completely separate
      languages.
    * for example, the language code "nb" is for Norwegian Bokmal.
      Its macro language code is "no" for Norwegian.
    * This is useful because a user's locale may be set to the
      subtype, but the translations may be represented with the
      macrolanguage code instead. It would be useful to show that
      user the macrolanguage translations rather than fall back
      to the source language for your app. (English?)
 
See the full API documentation for [LocaleMatcher class](./docs/LocaleMatcher.html)
for specifics.

## License

Copyright © 2021, JEDLSoft

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.

See the License for the specific language governing permissions and
limitations under the License.

## Release Notes

### v1.0.0

- initial version
- copied from ilib 14.9.0