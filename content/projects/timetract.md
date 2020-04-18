# TimeTract

The idea of TimeTract originated from a Google Sheets I created to automatically log and format my RescueTime data. When others found it motivating, I thought that it would be useful to create an app that allows people to view how others spend their time, and get motivated by a competitive atmosphere where they compete to become the most productive.

The first prototype evolved from a hackathon project, and after a few months, I decided to use React Native to turn TimeTract into a mobile app.

I released TimeTract onto [Google Play](https://play.google.com/store/apps/details?id=com.leonzalion.timetract) on March 13, 2020. The initial version supported users joining a single group with other TimeTract users.

After frustration with working with REST APIs, I decided to refactor the TimeTract backend to use GraphQL using Apollo Client and Prisma2. However, I've since been busy working on other projects.

On March 25, 2020, an update of TimeTract was released that used GraphQL to communicate with the backend. However, I came across an issue with Prisma2 and couldn't get the app to work properly, and frustration of debugging the same problem eventually led me to switch my focus to other projects.

After gaining an interest in Flutter development, I'm hoping to refactor TimeTract to use Flutter in the near future.

For now, you can view TimeTract's source code at the [app's GitHub repository](https://github.com/leonzalion/TimeTractApp), as well as the [backend server's GitHub repository](https://github.com/leonzalion/TimeTractServer).