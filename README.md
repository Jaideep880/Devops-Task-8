Java Maven Build Job in Jenkins 🚀

This guide walks you through setting up Jenkins to build a simple Java application using Maven, marking your first step into CI/CD automation.
Tools Required
- Jenkins (Local installation or via Docker)
- Java JDK (Version 8 or 11)
- Maven (For building the Java application)
- Git (Optional – you can run from a local folder)

Getting Started
1. Create a Simple Java Application
Create a basic Java file:
// HelloWorld.java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, Jenkins + Maven!");
    }
}


2. Define the Maven Build Configuration (pom.xml)
<project>
    <modelVersion>4.0.0</modelVersion>
    <groupId>com.example</groupId>
    <artifactId>hello</artifactId>
    <version>1.0</version>
    <build>
        <plugins>
            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-compiler-plugin</artifactId>
                <version>3.8.1</version>
                <configuration>
                    <source>1.8</source>
                    <target>1.8</target>
                </configuration>
            </plugin>
        </plugins>
    </build>
</project>


3. Run Jenkins via Docker
Launch Jenkins using Docker:
docker run -p 8080:8080 jenkins/jenkins:lts


4. Configure Jenkins for Maven Builds
Inside Jenkins:
- Go to: Manage Jenkins → Global Tool Configuration → Add Maven (e.g., Maven 3.8.6)
- Create a new Freestyle Project
- In the Build section: Select "Invoke top-level Maven targets"
- Set Goal: clean package
- Save & Build the job

5. Verify Build Success
After running the job:
- Check Console Output
- Look for: BUILD SUCCESS confirmation

Deliverables
✅ Basic Java HelloWorld app with pom.xml
✅ Configured Jenkins Freestyle job
✅ Screenshot of successful build console output

This README ensures clarity, organization, and a professional touch. Let me know if you need further refinements! 🎯✨
