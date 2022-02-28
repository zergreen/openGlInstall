# openGlInstall

การติดตั้ง openGL บน linux (Ubuntu) [ใน 3 นาที]

# How To install 

    sudo apt-get update # Update central library/(อัพเดต สโตร์กลาง)
    sudo apt-get install freeglut3 freeglut3-dev binutils-gold G++ cmake libglew-dev mesa-common-dev build-essential libglew1.5-dev libglm-dev # Program && librarry /(ตัวโปรแกรมและไลบารี่ที่จำเป็นสำหรับ openGL)
    
# Check version

หลังจากที่เราติดตั้งซอฟต์แวร์ช้างต้นแล้ว ให้เราเช็ค เวอร์ชั่นของ openGl โดยใช้คำสั่ง 
   
    glxinfo | grep "OpenGL version"
    
 เทสว่า เครื่องเราลองรับ opengl หรือไม่ โดยใช้คำสั่ง (โดยจะปรากฏเป็น simulation วัตถุเกียร์)
 
    glxgear
    
# Compile And Run code

<p>การรันไฟล์ .cpp เราต้องนำเข้าไลบารี่ที่ เราได้ระบุไว้ในส่วนของ include ซึ่ง ณ ที่นี้ ได้แก่ Gl, GLEW, glfw <br>
   ซึ่งเราจะ นำเข้าไลบารี่ มาคอมไพล์ด้วยวิธีดังนี้ </p>

    g++ main.cpp -lGL -lGLEW -lglfw
    
รูปแบบ syntax -l คือ

    # -l => มาจากคำว่า library ส่วนที่ตามหลังคือ ไลบารี่นั้น โดยเราสามารรันแบนี้ก็ได้
    # -lGl หรือ -l Gl
    
โดยหลังจากที่เราคอมไพล์ไฟล์แล้วเราจะได้ไฟล์เบื้องต้นมาชื่อว่า a.out โดยการรันไฟล์นี้ จะเหมือนกับใน gcc คือ

    ./a.out
    
# Trick

เราสามารถรวบทั้งการคอมไพล์และรันมาไว้ในบรรทัดเดียวกันได้ดังนี้

    g++ main.cpp -lGL -lGLEW -lglfw && ./a.out
    # หรือเราจะตั้งชื่อไฟล์ด้วยก็ได้ เช่น
    g++ main.cpp -o test -lGL -lGLEW -lglfw && ./test

# Suggest

ถ้าคอมไพล์ไม่ผ่านทั้งที่โค้ดถูกแล้วแสดงว่าอาจจะไม่ได้นำเข้าไลบารี่เข้ามาคอมไพล์ด้วย แนะนำว่าให้เซิชใน <br>
StackOverFlow แล้ว ติดตั้งไลบารี่นั้นซ่ะ แล้วตอนคอมไพล์ก็แนบไลบารี่นั้นด้วย

# Test On

เทสบนสถาปัตยกรรม
    
    OS: Ubuntu 20.04.3 LTS x86_64
    CPU: Intel I5
    GPU: NVIDIA
    DATE: 1/3/2022
