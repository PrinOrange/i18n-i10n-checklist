# International / Localization Checklist

> 🚧 This document is under construction as far.

There are many tedious details in the localization and internationalization of software. This checklist is intended to provide a checklist for planning reference during the software design phase. Of course, this is just an outline. Because the specifications of different countries and regions are different, the specific processing details will not be given. You only need to consider this general direction in international design.

## Language Translation

### Charset, encoding and alphabets

Although UTF-8 has been widely used in the mainstream world, some platforms may not support UTF-8 by default, but use their own encoding schemes, such as ISO 8859-1, GBK, Big5, etc. Have you considered this in the character processing part of your program? Does your platform support displaying the corresponding character set? Such as Latin letters, ideographic characters, Cyrillic characters, Thai letters, etc.

### Transcription system

In some cases, some character sets may not be supported. Do you need to transcribe letters? For example, some Unix systems only support the ASCII character set and cannot display Cyrillic letters. Cyrillic letters need to be transcribed into Latin letters.

### Dialects and area language

A country or region may have multiple languages ​​or dialects in use. For example, Singapore uses Chinese, English and Malay, and Hong Kong uses Cantonese and English at the same time. Have you considered this?

Similarly, a language can be used in multiple regions, but there will be dialect differences. For example, the Arabic used in Saudi Arabia and the United Arab Emirates is very different, and there are also differences in spelling and pronunciation between British English, Australia English and American English.

### Custom words

Some countries and regions may have their own idiomatic expressions, which need to be taken into account when translating content, otherwise it will appear abrupt or impolite. For example, the Arab region usually adds religious terms such as "Allah is great" and "Allahu Akbar" in formal texts, while Japan and South Korea need to use appropriate honorifics according to different situations.

## UI, Layout and Typography

### RTL & LTR

### Linebreaks, Layout Thrashing

### Input Methods & IME (Input Method Editor)

## UX and Interaction Design

### Shortcut Key

Different regions use different keyboards. Common keyboards include QWERTY, QWERTZ, and AZERTY. Even different regions use different keyboards for the same language. For example, the United States uses the standard QWERTY keyboard layout, while the United Kingdom uses the British standard layout. [See more details](https://en.wikipedia.org/wiki/Keyboard_layout).
Different keyboard layouts mean that the number and location of keys may also be different. The design of shortcut keys needs to be carefully considered.

## Content and Resource

### Sorting Rules

Different countries and regions have different sorting rules for list items. For example, English-speaking regions usually sort by the dictionary order of the item title, while mainland China prefers to sort by the dictionary order of the pinyin of the item title, but Hong Kong uses the number of strokes and Taiwan uses the order of phonetic symbols.
In addition, the alphabetical order of many different countries may also be different, resulting in different sorting rules, which also needs to be considered.

### Date Format, Time Zones and Daylight Saving

What date format does the region you serve use? DMY, YMD, or MDY? What are the requirements for writing months and numbers? Does it use daylight saving time?

### Numbers, Measurements and Math Formulas

Different countries and regions have different numerical formats and measurement unit representations, which need to be considered.

For example, the United Kingdom and the United States use a comma "," to express a thousand separator and a dot "." to express a decimal point, but Germany, France, etc. use a dot "." to express a thousand separator and a comma "," to express a decimal point. And Switzerland, France Sometimes use a space (1 000 000) as a thousands separator.

Also pay attention to the number grouping. India uses the 2-2-3 grouping method. For example, 100,000 is written as 1,00,000 in India, and 1,000,000 is written as 10,00,000 in India.

### Natural Language Process

### Audio, Video and other media

Have you prepared subtitle files and translation resources for different languages? Are the translation resources for simultaneous interpretation also ready?

### Taboo for words, symbols

Have you considered the taboos in different countries and regions? For example, in some monarchical countries, such as Thailand and Iran, any disrespectful words to the king are prohibited. Please avoid these contents. Similarly, in the Muslim world, some animal symbols such as pigs and donkeys are also considered symbols of uncleanness.

Similarly, due to religious and cultural factors, some elements are considered taboo. For example, in Saudi Arabia and Yemen, Christmas elements are not allowed in products due to religious reasons.

In addition, different countries and regions may have different interpretations of symbols, which needs to be taken into consideration. For example, the OK gesture 👌, although it has a positive meaning in the United Kingdom, the United States and other regions, is negative or even offensive in France, Germany and Brazil. Even the thumbs-up 👍, although it means approval in most cases, may mean sarcasm or ridicule in Greece and Latin America, so try not to use it in your products.

## Monetization & Payments

What is the smallest unit of currency in the region you serve? For example, China is 0.1 yuan and the United States is 0.01 dollar. Is there a collection plan? Are factors such as exchange rates and currency control policies taken into account? What number format is used for the amount involved? For example, China uses uppercase Chinese characters while English uses word spelling.

## Performance & Optimization

### CDN / Network Zone

## Security & Access Control

## Legal & Compliance

## Other Details

### Accessible

Different countries and regions use different Braille and sign languages. Did you take this into consideration when designing?

## Reference

+ [W3C Draft- i18n](https://w3c.github.io/bp-i18n-specdev/)
