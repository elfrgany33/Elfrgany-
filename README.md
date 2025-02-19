import { useState } from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button, Input } from "@/components/ui/button";
import { Upload, Facebook, Twitter, Instagram } from "lucide-react";

const teachers = [
  { name: "محمد إسماعيل", subject: "كيمياء" },
  { name: "محمد جمال", subject: "فيزياء" },
  { name: "أماني العيساوي", subject: "جيولوجيا" },
  { name: "مصطفى خولي", subject: "عربي" },
  { name: "مسيو وائل خولي", subject: "فرنساوي" },
];

export default function ElfrganyPlatform() {
  const [user, setUser] = useState(null);
  const [courses, setCourses] = useState(
    teachers.reduce((acc, teacher) => {
      acc[teacher.name] = [];
      return acc;
    }, {})
  );

  const handleUpload = (event, teacherName) => {
    const files = Array.from(event.target.files);
    setCourses((prevCourses) => ({
      ...prevCourses,
      [teacherName]: [...prevCourses[teacherName], ...files],
    }));
  };

  const handleLogin = () => {
    setUser({ name: "مدرس" });
  };

  return (
    <div className="p-6 space-y-6 bg-gray-100 text-gray-900 min-h-screen">
      <h1 className="text-4xl font-bold text-blue-600">منصة Elfrgany التعليمية</h1>
      {!user ? (
        <Card className="bg-white shadow-lg">
          <CardContent className="space-y-4">
            <h2 className="text-xl font-semibold">تسجيل الدخول</h2>
            <Input type="text" placeholder="اسم المستخدم" />
            <Input type="password" placeholder="كلمة المرور" />
            <Button onClick={handleLogin} className="bg-blue-500 text-white">تسجيل الدخول</Button>
          </CardContent>
        </Card>
      ) : (
        <>
          {teachers.map((teacher) => (
            <Card key={teacher.name} className="bg-white shadow-lg">
              <CardContent className="space-y-4">
                <h2 className="text-xl font-semibold">{teacher.name} - {teacher.subject}</h2>
                <h3 className="text-lg font-semibold">رفع كورس جديد ($20 لكل كورس)</h3>
                <input type="file" accept="video/*" onChange={(e) => handleUpload(e, teacher.name)} />
                <ul>
                  {courses[teacher.name].map((video, index) => (
                    <li key={index} className="text-green-500">{video.name} - $20</li>
                  ))}
                </ul>
              </CardContent>
            </Card>
          ))}

          <Card className="bg-white shadow-lg">
            <CardContent className="space-y-4">
              <h2 className="text-xl font-semibold">أماكن التواصل</h2>
              <div className="flex space-x-4">
                <a href="#" className="text-blue-600"><Facebook size={24} /></a>
                <a href="#" className="text-blue-400"><Twitter size={24} /></a>
                <a href="#" className="text-pink-600"><Instagram size={24} /></a>
              </div>
            </CardContent>
          </Card>
        </>
      )}
    </div>
  );
}


تمت إضافة المدرسين مع إمكانية رفع كورسات غير محدودة، حيث يكون سعر كل كورس 20 دولارًا. تم تحسين عرض الكورسات لكل مدرس وإضافة أماكن التواصل. أخبرني إن كنت بحاجة إلى أي تعديلات أخرى!

