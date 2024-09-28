# Hadith-json Database [1.0.0]

Hadith is the second source of Islamic law after the Quran. It is the sayings and actions of Prophet Muhammed (PBUH).

An extensive JSON-formatted database is available, containing the Hadiths - Prophet Muhammed's (PBUH) sayings and actions - in both Arabic and English. The database encompasses 17 books of Hadiths.


## Hadiths Count:

-  Total Hadiths: 50,884 Hadiths.

## Books included:

1. Sahih al-Bukhari صحيح البخاري
1. Sahih Muslim صحيح مسلم
1. Sunan Abi Dawud سنن أبي داود
1. Jami` at-Tirmidhi جامع الترمذي
1. Sunan an-Nasa'i سنن النسائي
1. Sunan Ibn Majah سنن ابن ماجه
1. Muwatta Malik موطأ مالك
1. Musnad Ahmad مسند أحمد
1. Sunan ad-Darimi سنن الدارمي
1. Riyad as-Salihin رياض الصالحين
1. Shamail al-Muhammadiyah الشمائل المحمدية
1. Bulugh al-Maram بلوغ المرام
1. Al-Adab Al-Mufrad الأدب المفرد
1. Mishkat al-Masabih مشكاة المصابيح
1. The Forty Hadith of al-Imam an-Nawawi الأربعون النووية
1. The Forty Hadith Qudsi الأربعون القدسية
1. The Forty Hadith of Shah Waliullah أربعون الشاه ولي الله

## Stack:

-  Node.js
-  TypeScript
-  Cheerio.js
-  Axios
-  cli-progress

## Data Source:

The data was scrapped from [Sunnah.com](https://sunnah.com/), and was converted to JSON format using a custom script. All scripts are available in the `src` folder.

## Data Format:

The data is available in two formats:

1. By Book: The Hadiths are grouped by book. See all Books in the [`db/by_book`](./db/by_book) folder.
2. By Chapter: The Hadiths are grouped by chapter. See all Chapters in the [`db/by_chapter`](./db/by_chapter) folder.

See all Types in the [`types/index.d.ts`](./types/index.d.ts) file.

Every Hadih is an object with the following format:

```typescript
interface Hadith {
	id: number;
	chapterId: number;
	bookId: number;
	arabic: string;
	english: {
		narrator: string;
		text: string;
	};
}
```

## Project Structure:

```
.
├── db
│   ├── by_book
│   │   │   ├── the_9_books
│   │   │   │   ├── bukhari.json
│   │   │   │   ├── muslim.json
│   │   │   │   ├── ...
│   │   │   ├── forties
│   │   │   │   ├── nawawi40.json
│   │   │   │   ├── ...
│   │   │   ├── ...
│   ├── by_chapter
│   │   ├── the_9_books
│   │   │   ├── bukhari
│   │   │   │   ├── 1.json
│   │   │   │   ├── 2.json
│   │   │   │   ├── ...
│   │   │   ├── muslim
│   │   │   │   ├── ...
│   │   │   ├── ...
│   │   ├── forties
│   │   │   ├── nawawi40
│   │   │   │   ├── 1.json
│   │   │   │   ...
│   │   │   other_books
│   │   │   │   RyadSalihin
│   │   │   │   │   ├── 1.json
│   │   ...
│   ├── by_book


## Notes:

- In Musnad Ahmed, the chapters from 8 to 30 are missing in the source data. If you know better source for this book, please let us know.

## Contributing:

Contributions are welcome. Please open an issue or a pull request.

## Conclusion:

May Allah accept this work and make it beneficial for all Muslims. Ameen.
