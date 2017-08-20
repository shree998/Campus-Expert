# Title
GCompris, Revolutionarizing the Akademia
## Subtitle
where child turns into a contributor

## Abstract

GCompris is a high-quality educational software suite comprising of numerous activities for children aged 2 to 10. The talk will cover how GCompris started its journey with KDE years back to GCompris taking KDE to schools with its recent version. It will cover how it turns an infant to a toddler to a contributor covering the architecture of GCompris and understanding it in depth.

## Description

GCompris can be seen as a success in the Free
Software community in reaching a large audience by leveraging the multi-platform nature of Qt.
GCompris is a high-quality educational software suite comprising of numerous activities for children aged 2 to 10. It started its journey in 2014 with KDE. It has been a long and wonderful journey since then. Recently we replaced the Gtk+ version for Windows with Qt version and took KDE to schools with its latest version. It offers 137 activities and more are being developed with time.
It will cover the journey of an infant to a contributor with GCompris which will also cover different parts of GCompris and will help people who want to contribute to it.

1. So, the journey starts with an infant who comes across GCompris and explores its different sections from mathematical to language to science and mouse coordination. The activities are divided into various genres and difficulty on the basis of age levels and type of activity which will be shown which helps the infant to grow which is their first involvement in KDE by using it. GCompris is completely supported in 17 languages and partially supported in 15+ other languages.

2. The infant then grows to a child and thinks of creating his/her own activity. Then they come across the architecture of GCompris which will be explained in depth in the talk which has:
1. A C++ core in src/core
2. QML activities in src/activities
3. Each activity in its folder
4. An activity can extend an other one and provide it a dataset
5. At compilation time each activity is zipped in a ‘rcc’ file which is loaded at run time.

3. The child than grows and gets curious further on how to contribute. Then he finally learns how to get started in the project that he played while he was an infant so that he/she can be equip other infants with more activities.
They learn about
1. GCompris Codebase which covers activity Development
2. Compilation chain in CMake
3. Core Development which includes
a) Activity API
b) C++ Widgets
c) QML Widgets
4. Documentation
5. Graphics
6. Packaging
7. Localization.

4. Then the infant who earlier played with the activities finally decides the area of interest and finally turns into a contributor :)

The talk would cover our so success story so far and how we are helping an infant to grow and finally contribute to a project they once used along with the future state which would be to take KDE and GCompris to as many schools/kids as we can so that every infant understand their power and contributes to the community.
It will also cover the role of teachers who turn into contributors to facilitate and help their pupils and bringing/making this academia a fun way to learn.
