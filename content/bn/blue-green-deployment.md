---
title: নীল সবুজ স্থাপনা (Blue Green Deployment)
status: Completed
category: ধারণা
tags: ["অ্যাপ্লিকেশন", "", ""]
---

## এটা কি

ন্যূনতম ডাউনটাইম সহ চলমান কম্পিউটার সিস্টেম আপডেট করার জন্য নীল-সবুজ স্থাপনা একটি কৌশল।
অপারেটর দুটি পরিবেশ বজায় রাখে, যা "নীল" এবং "সবুজ" নামে ডাকা হয়।
একটি প্রোডাকশন ট্র্যাফিক পরিবেশন করে (সংস্করণটি যেটি সেই সময় ব্যবহারকারীরা ব্যবহার করেন), যখন অন্যটি আপডেট করা হয়।
একবার অ-সক্রিয় (সবুজ) পরিবেশে পরীক্ষা শেষ হয়ে গেলে,
উৎপাদনে ট্র্যাফিক সুইচ ওভার করা হয় (প্রায়শই লোড ব্যালেন্সার ব্যবহারের মাধ্যমে)।
মনে রাখবেন যে নীল-সবুজ স্থাপনার অর্থ হল সম্পূর্ণ পরিবেশ পরিবর্তন করা, একযোগে, অনেকগুলি পরিষেবা সমন্বিত করে।
বিভ্রান্তিকরভাবে, কখনও কখনও শব্দটি একটি সিস্টেমের মধ্যে পৃথক পরিষেবার ক্ষেত্রে ব্যবহৃত হয়।
এই অস্পষ্টতা এড়াতে, পৃথক উপাদান উল্লেখ করার সময় "শূন্য-ডাউনটাইম স্থাপনা (zero-downtime deployment)" শব্দটি পছন্দ করা হয়।

## এটা যেসব সমস্যাতে দৃষ্টিপাত করে

নীল-সবুজ স্থাপনাগুলি সফ্টওয়্যার আপডেট করার সময় ন্যূনতম ডাউনটাইমের অনুমতি দেয় যা পশ্চাদগামী সামঞ্জস্যের অভাবের কারণে "লকস্টেপ" এ পরিবর্তন করতে হয়।
উদাহরণস্বরূপ, নীল-সবুজ স্থাপনা একটি ওয়েবসাইট এবং একটি ডাটাবেস সমন্বিত একটি অনলাইন স্টোরের জন্য উপযুক্ত হবে যা আপডেট করা প্রয়োজন, কিন্তু ডাটাবেসের নতুন সংস্করণ ওয়েবসাইটের পুরানো সংস্করণের সাথে কাজ করে না এবং এর তদ্বিপরীত।
এই ক্ষেত্রে, উভয় একই সময়ে পরিবর্তন করা প্রয়োজন।
যদি এটি উৎপাদন সিস্টেমে করা হয় তবে গ্রাহকরা ডাউনটাইম লক্ষ্য করবেন।

## এটা কিভাবে সাহায্য করে

নীল-সবুজ স্থাপনা নন-ক্লাউড নেটিভ সফ্টওয়্যারের জন্য একটি উপযুক্ত কৌশল যা ন্যূনতম ডাউনটাইমের সাথে আপডেট করা দরকার।
যাইহোক, এটির ব্যবহার সাধারণত একটি "গন্ধ(smell)" যা লেগাসি সফ্টওয়্যারগুলি কে পুনরায় ইঞ্জিনিয়ার করার প্রয়োজন তৈরী করে যাতে উপাদানগুলি পৃথকভাবে আপডেট করা সম্ভব হয় ওঠে ।      