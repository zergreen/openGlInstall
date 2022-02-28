# openGlInstall

# How To install 

    sudo apt-get update # Update central library/(อัพเดต สโตร์กลาง)
    sudo apt-get install freeglut3 freeglut3-dev binutils-gold G++ cmake libglew-dev mesa-common-dev build-essential libglew1.5-dev libglm-dev # Program && librarry /(ตัวโปรแกรมและไลบารี่ที่จำเป็นสำหรับ openGL)
    
# Check version

หลังจากที่เราติดตั้งซอฟต์แวร์ช้างต้นแล้ว ให้เราเช็ค เวอร์ชั่นของ openGl โดยใช้คำสั่ง 
   
    glxinfo | grep "OpenGL version"
    
 เทสว่า เครื่องเราลองรับ opengl หรือไม่ โดยใช้คำสั่ง (โดยจะปรากฏเป็น simulation วัตถุเกียร์)
 
    glxgear
