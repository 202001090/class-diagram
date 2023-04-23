  classDiagram
 
   Admin --> Database
Admin --> Announcements
Admin --> Password

Faculty --> CourseReports
Faculty --> CourseInfo

Student --> Grades
Student --> CourseReports
Student --> Fees
Student --> Attendance
Student --> PersonalInfo
Student --> Feedback

Database <--> Student
Database <--> Faculty
     direction RL

class Admin {
  +addStudentInfo()
  +dropStudentInfo()
  +addFacultyInfo()
  +dropFacultyInfo()
  +broadcastAnnouncements()
  +allocatePassword()
}

class Faculty {
  +generateCourseReports()
  +maintainCourseInfo()
}

class Student {
  +trackGradesAndTranscripts()
  +generateCourseReports()
  +generateFeesReceipt()
  +trackAttendance()
  +modifyPersonalInfoAndAchievements()
  +provideFeedback()
}

class Database {
  +addStudentInfo()
  +dropStudentInfo()
  +addFacultyInfo()
  +dropFacultyInfo()
}

class Announcements {
  +broadcastGeneralAnnouncements()
}

class Password {
  +allocatePassword()
}

class CourseReports {
  +generateCourseReports()
}

class CourseInfo {
  +maintainCourseInfo()
}

class Grades {
  +trackGradesAndTranscripts()
}

class Fees {
  +generateFeesReceipt()
}

class Attendance {
  +trackAttendance()
}

class PersonalInfo {
  +modifyPersonalInfoAndAchievements()
}

class Feedback {
  +provideFeedback()
}
