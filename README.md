# Git and GitHub with All Concepts🔥

### 🧠Some Terminology

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

আমরা যদি আমাদের সমস্ত কিছুকে Staging করতে চাই, তবে লিখতে পারি -

```javascript
git add --all
```

আমি শুধুমাত্র যে ডিরেক্টরির মধ্যে আছি শুধুমাত্র সেগুলোকে Staging করতে লিখব -

```javascript
git add .
```
