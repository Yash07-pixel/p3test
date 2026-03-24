✅ EXPERIMENT 3 – COMPLETE FLOW
🔹 1. Check Gradle
gradle -v
🔹 2. Create Project
IntelliJ → New Project → Gradle
Groovy DSL
Group: org.example
🔹 3. Update build.gradle
plugins {
    id 'application'
}

repositories {
    mavenCentral()
}

dependencies {
    testImplementation 'org.junit.jupiter:junit-jupiter:5.8.1'
}

application {
    mainClass = 'org.example.Main'
}
🔹 4. Create Main Class

Path:

src/main/java/org/example/Main.java

Code:

package org.example;

public class Main {
    public static void main(String[] args) {
        System.out.println("Hello from Gradle!");
    }
}
🔹 5. Run Project
gradle run
🔹 6. Create docs Folder
Root → docs/
Add index.html
🔹 7. Push to GitHub
git init
git add .
git commit -m "gradle project"
git remote add origin <URL>
git push -u origin master
🔹 8. Deploy Website
GitHub → Settings → Pages
Branch: master
Folder: /docs
Save
🔹 9. Update build.gradle (Testing)
dependencies {
    testImplementation 'org.seleniumhq.selenium:selenium-java:4.41.0'
    testImplementation 'org.testng:testng:7.12.0'
}

test {
    useTestNG()
}
🔹 10. Reload Gradle
🔹 11. Create Test Package
src/test/java → org.test
🔹 12. Create Test Class
WebpageTest.java
🔹 13. Add Code
Paste Selenium code
Update:
URL → your GitHub Pages link
Title → exact title
🔹 14. Run Test
gradle test
🔹 15. Verify
Browser opens
Website loads
Test passes
