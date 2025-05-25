1. What is PostgreSQL?
PostgreSQL একটি ওপেন-সোর্স রিলেশনাল ডেটাবেজ ম্যানেজমেন্ট সিস্টেম (RDBMS), যা ডেটা সংরক্ষণ, পরিচালনা এবং অ্যাক্সেস করার জন্য ব্যবহৃত হয়। 
3.Explain the Primary Key and Foreign Key concepts in PostgreSQL.
Primary Key: একটি কলাম বা কলামগুলোর কম্বিনেশন যা প্রতিটি সারিকে ইউনিকভাবে চিহ্নিত করে।
Foreign Key: একটি টেবিলের কলাম যা অন্য একটি টেবিলের Primary Key কে রেফার করে। 
5.Explain the purpose of the WHERE clause in a SELECT statement.
WHERE ক্লজ ব্যবহার করে ডেটাবেজ থেকে নির্দিষ্ট শর্ত অনুযায়ী রেকর্ড ফিল্টার করা হয়। উদাহরণস্বরূপ:
SELECT * FROM students WHERE age > 18;
7.How can you modify data using UPDATE statements?
UPDATE স্টেটমেন্টের মাধ্যমে টেবিলের বিদ্যমান ডেটা আপডেট করা যায়। উদাহরণ:
UPDATE students SET age = 20 WHERE id = 1;
মানে ID 1 থাকা শিক্ষার্থীর বয়স ২০ করা হবে।
8.What is the significance of the JOIN operation, and how does it work in PostgreSQL? 
JOIN অপারেশন ব্যবহার করে একাধিক টেবিল থেকে সম্পর্কযুক্ত ডেটা একত্রে আনা যায়। উদাহরণ:
SELECT students.name, courses.title
FROM students
JOIN enrollments ON students.id = enrollments.student_id
JOIN courses ON enrollments.course_id = courses.id;
এখানে তিনটি টেবিল একসাথে যুক্ত হয়েছে এবং শিক্ষার্থীর নাম ও কোর্স শিরোনাম দেখাচ্ছে।