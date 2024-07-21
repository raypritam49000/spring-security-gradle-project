
// check all java -version path
/usr/libexec/java_home -V

Matching Java Virtual Machines (6):
21.0.3 (x86_64) "Oracle Corporation" - "Java SE 21.0.3" /Library/Java/JavaVirtualMachines/jdk-21.jdk/Contents/Home
20.0.1 (x86_64) "Oracle Corporation" - "Java SE 20.0.1" /Library/Java/JavaVirtualMachines/jdk-20.jdk/Contents/Home
17.0.7 (x86_64) "Oracle Corporation" - "Java SE 17.0.7" /Library/Java/JavaVirtualMachines/jdk-17.jdk/Contents/Home
11.0.18 (x86_64) "Oracle Corporation" - "Java SE 11.0.18" /Library/Java/JavaVirtualMachines/jdk-11.jdk/Contents/Home
1.8.202.08 (x86_64) "Oracle Corporation" - "Java" /Library/Internet Plug-Ins/JavaAppletPlugin.plugin/Contents/Home
1.8.0_202 (x86_64) "Oracle Corporation" - "Java SE 8" /Library/Java/JavaVirtualMachines/jdk1.8.0_202.jdk/Contents/Home
/Library/Java/JavaVirtualMachines/jdk-21.jdk/Contents/Home

// shell java
echo $SHELL

// This command will download repository for open jdk
brew tap adoptopenjdk/openjdk

//installing jdk 11 and 8
brew install --cask adoptopenjdk11 adoptopenjdk8

//download utility jenv
brew install jenv

//add these two commands in zshrc
echo 'export PATH="$HOME/.jenv/bin:$PATH"' >> ~/.zshrc
echo 'eval "$(jenv init -)"' >> ~/.zshrc

//add our java to jenv
jenv add /Library/Java/JavaVirtualMachines/jdk-21.jdk/Contents/Home
jenv add /Library/Java/JavaVirtualMachines/jdk-20.jdk/Contents/Home
jenv add /Library/Java/JavaVirtualMachines/jdk-17.jdk/Contents/Home
jenv add /Library/Java/JavaVirtualMachines/jdk-11.jdk/Contents/Home
jenv add /Library/Java/JavaVirtualMachines/jdk1.8.0_202.jdk/Contents/Home


//now check versions
jenv versions

//to set java versions we can use:-

jenv local 1.8
java -version

jenv local 11
java -version

// To enable java to maven
jenv enable-plugin maven

//To enable java to grade
jenv enable-plugin gradle

jenv enable-plugin export
echo $JAVA_HOME

Note :- In case if you see changes are not reflecting, Please do restart your terminal.