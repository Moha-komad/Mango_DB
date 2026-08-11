# Student Task Sheet - MongoDB Shell



// 2. Insert at least 3 students
db.students.insertMany([
  {
    name: "Ali",
    age: 20,
    email: "ali@gmail.com",
    courses: ["HTML", "CSS", "JavaScript"]
  },
  {
    name: "Ahmed",
    age: 22,
    email: "ahmed@gmail.com",
    courses: ["React", "Node.js"]
  },
  {
    name: "Amina",
    age: 19,
    email: "amina@gmail.com",
    courses: ["MongoDB", "Express"]
  }
])

// 3. View all students
db.students.find().pretty()

// 4. Update Ali's email
db.students.updateOne(
  { name: "Ali" },
  { $set: { email: "ali123@gmail.com" } }
)

// View updated data
db.students.find().pretty()

// 5. Delete one student (Ahmed)
db.students.deleteOne(
  { name: "Ahmed" }
)

// View remaining students
db.students.find().pretty()

// 6. Optional: Insert a student with a nested address object
db.students.insertOne({
  name: "Fatima",
  age: 21,
  email: "fatima@gmail.com",
  courses: ["Python", "MongoDB"],
  address: {
    city: "Mogadishu",
    district: "Hodan",
    country: "Somalia"
  }
})

// Final output
db.students.find().pretty()
```



