# International / Localization Checklist

> 🚧 This document is under construction as far.

There are many tedious details in the localization and internationalization of software. This checklist is intended to provide a checklist for planning reference during the software design phase. Of course, this is just an outline. Because the specifications of different countries and regions are different, the specific processing details will not be given. You only need to consider this general direction in international design.

## Language Translation

### Charset, encoding and alphabets

Although UTF-8 has been widely used in the mainstream world, some platforms may not support UTF-8 by default, but use their own encoding schemes, such as ISO 8859-1, GBK, Big5, etc. Have you considered this in the character processing part of your program? Does your platform support displaying the corresponding character set? Such as Latin letters, ideographic characters, Cyrillic characters, Thai letters, etc.

### Transcription system

### Dialects and area language

A country or region may have multiple languages ​​or dialects in use. For example, Singapore uses Chinese, English and Malay, and Hong Kong uses Cantonese and English at the same time. Have you considered this?

Similarly, a language can be used in multiple regions, but there will be dialect differences. For example, the Arabic used in Saudi Arabia and the United Arab Emirates is very different, and there are also differences in spelling and pronunciation between British English, Australia English and American English.

### Custom words

## UI, Layout and Typography

### RTL & LTR

### Linebreaks

### Input Methods & IME (Input Method Editor)

## UX and Interaction Design

### Shortcut Key

## Content and Resource Design

### Sorting Rules

### Date Format, Time Zones and Daylight Saving

What date format does the region you serve use? DMY, YMD, or MDY? What are the requirements for writing months and numbers? Does it use daylight saving time?

### Numbers, Measurements and Math Formulas

### Natural Language Process

### Audio,Video and other media

Have you prepared subtitle files and translation resources for different languages? Are the translation resources for simultaneous interpretation also ready?

### Taboo for words, symbols

Have you considered the taboos in different countries and regions? For example, in some monarchical countries, such as Thailand and Iran, any disrespectful words to the king are prohibited. Please avoid these contents. Similarly, in the Muslim world, some animal symbols such as pigs and donkeys are also considered symbols of uncleanness.

## Monetization & Payments

What is the smallest unit of currency in the region you serve? For example, China is 0.1 yuan and the United States is 0.01 dollar. Is there a collection plan? Are factors such as exchange rates and currency control policies taken into account? What number format is used for the amount involved? For example, China uses uppercase Chinese characters while English uses word spelling.

## Performance & Optimization

### CDN / Network Zone

## Security & Access Control

## Legal & Compliance

## Other details

### Accessible

Different countries and regions use different Braille and sign languages. Did you take this into consideration when designing?

## Reference

+ [W3C Draft- i18n](https://w3c.github.io/bp-i18n-specdev/)
