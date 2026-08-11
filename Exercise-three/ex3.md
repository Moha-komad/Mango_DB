// 1. Insert 3 students
db.students.insertMany([
  {
    name: "Alice",
    email: "alice@example.com",
    points: 80,
    courses: ["MongoDB", "JavaScript"]
  },
  {
    name: "Bob",
    email: "bob@example.com",
    points: 70,
    courses: ["Python", "MongoDB"]
  },
  {
    name: "Charlie",
    email: "charlie@example.com",
    points: 90,
    courses: ["Java", "MongoDB"]
  }
]);

// 2. Use $set to update one email
db.students.updateOne(
  { name: "Alice" },
  { $set: { email: "alice.new@example.com" } }
);

// 3. Use $inc to increase points
db.students.updateOne(
  { name: "Bob" },
  { $inc: { points: 10 } }
);

// 4. Use $push to add a new course
db.students.updateOne(
  { name: "Charlie" },
  { $push: { courses: "Node.js" } }
);

// 5. Use $pull to remove a course
db.students.updateOne(
  { name: "Charlie" },
  { $pull: { courses: "Java" } }
);

// 6. BONUS: Use $set, $inc, and $push together
db.students.updateOne(
  { name: "Alice" },
  {
    $set: { email: "alice.final@example.com" },
    $inc: { points: 5 },
    $push: { courses: "React" }
  }
);