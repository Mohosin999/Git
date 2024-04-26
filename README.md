# Git and GitHub with All Concepts🔥

## 🧠Some Terminology

**`Working Directory:`** আমরা আমাদের পিসি বা ল্যাপটপের যে ডিরেক্টরিতে কাজ করি সেটা হলো আমাদের ওয়ার্কিং ডিরেক্টরি ।

**`Local Repository:`** আমরা যখন গিটে কাজ করি তখন গিট আমাদের জন্য locally একটা codebase তৈরি করে, যার মধ্যে যে সমস্ত ফাইল, ফোল্ডার যাই কিছু চেঞ্জ হোক না কেন গিট সেটা ট্র্যাক করতে পারে । অর্থাৎ সেই ট্র্যাক করার জন্য গিট locally একটা রিপোজিটরি তৈরি করে, ওই লোকাল রিপোজিটরির বাইরের জিনিসগুলো হয়তো গিটের নজরে নেই । রিপোজিটরি মানে একটা ফোল্ডারই, যার মধ্যে অসংখ্য ফাইল রাখা যাবে এবং সেটা গিটের নজরে থাকবে ।

**`Git Initialize:`** Working Directory এবং Local Repository এর মধ্যে যে সম্পর্কটা তৈরি করা হয় সেটা Git Initialize দিয়ে তৈরি করা হয় ।

**`Staging:`** Staging মানে আমরা একটা ফাইলকে এক ধাপ এগিয়ে দিচ্ছি আমাদের ওয়ার্কিং ডিরেক্টরি থেকে লোকাল রিপোজিটরির দিকে, যাতে গিট ওখান থেকে এই ফাইলের tracking, versioning সবকিছু করতে পারে ।

### Create a file

```javascript
touch main.js
```

### To know the current status of a file or folder

```javascript
git status
```

এখন এখানে দেখা যাচ্ছে আমাদের **`main.js`** ফাইলটা Untracked অবস্থায় আছে । এখন এটা কি আমরা Staging করার জন্য **`git add`** কমান্ডটা লিখতে পারি ।

আমরা যদি একটা ফাইলকে Staging করতে চাই তবে সেই ফাইল এর নামটা লিখে দিব -

```javascript
git add main.js
```

আমরা যদি আমাদের সমস্ত (all everything) কিছুকে Staging করতে চাই, তবে লিখতে পারি -

```javascript
git add --all
```

আমি শুধুমাত্র যে ডিরেক্টরির (current directory) মধ্যে আছি শুধুমাত্র সেগুলোকে Staging করতে লিখব -

```javascript
git add .
```

Note: ami amr current directory er root ee giye jodi git add. and git add --all likhi, duitai same hobe ai khetre.

ai kaj gulo korle file ta git er track e chole jai, but ai fileta akhono local repositorir ayotte ase ni. seta korar jonne amader commit korte hobe.

commit korle akta specifiq uniq id generate hoy jetake bola hoy commit id. next ee ai id dore amra previos code ee back korte parbo ba next code ee jete parbo.

Remember this, commit korar ag porjonto amra amader working directory tei aci, committ korar por amra local repository te jete parbo.

let's commit -

```javascript
git commit -m "created main.js file successflly"
```

oneke aksathe kaj korle or ami jodi amr previous kajer history gulo dekhte chai then akta command khub help korbe seta holo "git log", ami jodi dekhte chai onno ra aikhane ki kaj korece amar age "git log" er maddhome ami sob sundor vabe dekhte parbo

```javascript
git log
```

amader jodi 50 ta commit thake "git log" lekhar sathe sathe sob gulo amader diye dibe. but amader jodi commit id and commit message ta dorkar hoy amra setao pete pari "git log --oneline" er maddhome

```javascript
git log --oneline
```

### Most Important Command

kew jodi tar current commit theke niddristo akta commit ee fire jete chay and current commit take na chay, thaole take likhte hobe

```javascript
git reset --hard commitID //( commitID - where you want to go )
```

er korar fole amra je commitID diyecilam sekhae eshe geci, tahole amader oi commit ta ki akbare delete hoye gelo? na seta hoyni, amra chaile setake abar firiye ante pari and amr Head take reset kore abar sekhane jete pari -

```javascript
git reset --hard desireCommitID
```

amra amader ager commit id ta dewar maddhome sei ager jaigai fire gelam.

Remember ai command gulo daily kajer jonne khub important, aikhane kuno graphical tool kaje asbe na.

akhon ami akbar pisone geci, samne aschi "git log" kintu ai history gulo dekhabe na, ai history gulo dekhte amader likhte hobe -

```javascript
git reflog
```

tarmane reflog sudhu matro je log dey tana, ati git er somosto commited histry addopanto shoho diye dey.

[Note] kuno commit ke akebare delete na kore dewatai valo

\*\* kuno akta file ke delete korar jonne likhte pare

```javascript
git rm filename
```

aita korle file ta delete hoye jabe but sei file ta akhono giter tracking er moddhe ace, giter database e akhono file ta maintion ee ace. ami jodi akhon atake akebare delete kore dite chai giter database thekeo tahole amader akta commit korte hobe

```javascript
git commit -m "deleted file"
```

akhon ata giter tracking thekeo/ giter database thekeo delete hoye gece.
