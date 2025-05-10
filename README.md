# Internationalization & Localization Checklist  

> 🚧 This document is a work in progress.  

Internationalization (i18n) and localization (l10n) involve numerous intricate details. This checklist serves as a reference for planning during the software design phase. However, it provides only a high-level overview. Since different countries and regions have unique requirements and standards, this document does not cover specific implementation details. Instead, it highlights key considerations to keep in mind when designing for international audiences.  

## Language & Translation  

### Character Sets and Encoding 

Although UTF-8 is widely adopted, some platforms may not support it by default and instead use their own encoding schemes, such as ISO 8859-1, GBK, JIS, or Big5.

Have you accounted for this in your application's character processing? Does your platform support displaying the required character sets, including Latin, CJK ideographic, Cyrillic, Thai, and others?

Here is the wikipedia page for [charset encoding](https://en.wikipedia.org/wiki/Character_encoding#Common_character_encodings). 

### Transcription Systems  

In cases where certain character sets are unsupported, do you need a transcription system? For example, some Unix-based systems only support the ASCII character set and cannot display Cyrillic characters, requiring transliteration into Latin script.  

### Dialects and Regional Variants  

+ **Multi Official Language:** A country or region may have multiple official languages or dialects. For example, Singapore recognizes English, Chinese, and Malay, while Hong Kong uses both Cantonese and English. Have you accounted for these linguistic variations?  
+ **Region dialects:** Additionally, a single language may have multiple regional variations. For instance, Arabic as spoken in Saudi Arabia differs significantly from that used in the United Arab Emirates. Likewise, spelling and pronunciation vary between British English, Australian English, and American English.

### Fonts

For some languages use same character set may have different font glyphs.

- Japanese Kanji and Chinese character has different glyph standard. For same character, Chinese font and Japanese font may has different displaying formals.
- Vietnamese and English share Latin characters, but Vietnamese has tones, so the center of gravity of Vietnamese fonts is lower than that of English fonts.

## UI, Layout & Typography  

### Right-to-Left (RTL) & Left-to-Right (LTR) Support  

Have you ensured that your UI properly supports RTL languages such as Arabic and Hebrew? 

### Line Breaking & Layout Adjustments  

Different languages have different line-breaking rules. For example, Chinese and Japanese do not use spaces to separate words, while Thai requires special segmentation rules. Does your layout handle these differences correctly without causing layout thrashing?  

## UX & Interaction Design  

### Keyboard Layouts

Keyboard layouts vary by region. Common layouts include QWERTY, QWERTZ, and AZERTY, and even within the same language, there may be differences. For example, the U.S. uses a standard QWERTY layout, while the U.K. has a slightly different variation. [See more details](https://en.wikipedia.org/wiki/Keyboard_layout).  

+ When designing shortcut keys, ensure they remain accessible and intuitive across different keyboard layouts.
+ Have your software been adopted for user's language Input Method Editor (IME). You need to ensure that the user's input method can be worked normally in your software.

## Content & Resources  

### Sorting Rules  

Sorting rules vary between regions, even though for one language. 

- Most of regions that uses alphabets-based language typically use alphabet-dictionary order based on item titles.
- In mainland China, sorting by Pinyin is common. Hong Kong sorts by stroke count, whereas Taiwan follows Bopomofo order.

Moreover, alphabetical orders differ across languages, affecting sorting logic. Ensure your sorting algorithm accounts for these regional differences.  

### Date Formats, Time Zones & Daylight Saving Time  

+ **Date format:** Which date format is used in your target regions? Is it *DD/MM/YYYY*, *YYYY/MM/DD*, or *MM/DD/YYYY*? [See the distribution map of date formatting among different regions](https://en.wikipedia.org/wiki/List_of_date_formats_by_country).
+ **Time Zone:** Have you considered the time zone differences for each regions and countries? For example, the U.S. actually has six time zones, Eastern Time Zone, Central Time Zone, Mountain Time Zone, Pacific Time Zone, Alaska Time Zone, and Hawaii-Aleutian Time Zone. Here is the [details for time zone map](https://www.timeanddate.com/time/map/).
+ **Daylight saving time:** Are month names written as numbers or spelled out? Do you need to account for daylight saving time adjustments? For example, some European region and U.S. have daylight saving time.
+ **Special Calendar:** Some countries may not use the Gregorian calendar. For example, Japan uses the era name calendar(令和/平成/昭和), and Thailand uses the Thai Solar Calendar.

### Number Formats, Measurement Units & Mathematical Conventions  

Different regions have unique numerical formatting and measurement units.  

- The U.S. and U.K. use a comma (`1,000,000`) as a thousand separator and a dot (`1.5`) for decimals, whereas Germany, France and other European countries reverse this notation (`1.000.000` and `1,5`).  
- India groups numbers differently, using a **2-2-3** format: `10,00,000` instead of `1,000,000`.  
- Measurement units vary: the U.S. uses inches, feet, and pounds, while most of the world follows the metric system.  

Ensure your application can handle these variations dynamically.  

### Natural Language Processing (NLP) Considerations  

If your application involves NLP features such as search, spell checking, or text analysis, are these adapted for different languages?

### Audio, Video & Media Localization  

Have you prepared subtitles and translated resources for different languages? If your product supports live streaming or real-time interactions, do you provide interpretation services?  

### Cultural Sensitivities for Symbolism  

Have you accounted for cultural taboos and regional sensitivities?  

- In monarchies like Thailand and Iran, criticism of the royal family is strictly prohibited.  
- In Muslim-majority countries, certain animal symbols (e.g., pigs, donkeys) are considered inappropriate.  
- Some regions restrict religious imagery; for example, Christmas-related elements are not permitted in Saudi Arabia and Yemen.  
- Symbols can have vastly different meanings:  
  - The “OK” gesture (`👌`) is positive in the U.S. but offensive in France, Germany, and Brazil.  
  - The thumbs-up sign (`👍`) may be considered sarcastic in Greece and parts of Latin America.  

To avoid unintended offense, research regional interpretations before including symbols in your UI.  

## Monetization & Payments  

+ **Currency Unit:** What is the smallest currency unit in the target market? In China, it's 0.1 yuan, whereas in the U.S., it's 0.01 dollars.  
+ **Regulation:** Are currency exchange rates, transaction policies, and regional banking regulations accounted for?  
+ **Formal Written:** How are large amounts displayed? In China, Japan and Korea, amounts may be written in uppercase Chinese characters(壹/贰/叁/肆/伍), whereas English uses full word spelling, for example, the number `1,013,978.1` is written in form "One million thirteen thousand nine hundred seventy-eight and one tenth".

## Performance & Optimization  

### CDN & Network Zones  

Have you optimized content delivery networks (CDNs) for different regions to ensure low-latency performance? Is it optimized for local networks?

## Security & Access Control  

Are there specific compliance or data protection laws that need to be followed, such as GDPR in Europe or PIPL in China?

+ You should seek for user's permission according to the law the *ePrivacy Directive* by setting cookie acceptance button for websites in European and America.

## Legal & Compliance  

Have you considered regional legal requirements related to software distribution, content moderation, and user privacy? For example, 

+ The European Union has very strict privacy legislation. If you collect user's interactions and information without permission, you will be fined.
+ In China, your software and website must be verified with ICP and copyright license before publishing, and annotate the license notably in specified position.

## Accessibility & Inclusive Design  

Have you accounted for accessibility standards?  

- Different countries use different Braille systems and sign languages.  
- Screen readers and assistive technologies should be tested across various locales. 

## Geography



## Cultural Factor

Certain expressions or phrases may have region-specific variations that need careful translation to avoid sounding unnatural or inappropriate. 

+ For example, in Arabic-speaking regions, formal texts often include religious phrases like "Allahu Akbar" ("Allah is great"). 
+ In Japan and South Korea, appropriate honorifics should be used based on social and contextual factors, like「です」「ます」, and「습니다」 

## References  

- [W3C Internationalization Best Practices](https://w3c.github.io/bp-i18n-specdev/)  
