# Introduction
```javascript
const setGreeting = (person, emoji) => {
  introduction.innerText = `Hi, I’m ${person.username} ${emoji}`
}

setGreeting(TKravel, '&#128075');
```
*// expected output*


<h1>Hi, I'm TKravel 👋</h1>

## About section
```javascript
import React, {useEffect, useState} from 'react';

export const AboutSection = () => {
const [aboutData, setAboutData] = useState({});
  useEffect(() => {
      fetch('http://me.com/get-details')
        .then((response) => response.json())
        .then((data) => setAboutData(data))
  }, []);

return (
  <section>
      <h2>About me</h2>
      <ul className='interests-list'>
         {aboutData.map((aboutItem) => {
            return (
              <li key={aboutItem.id}>
              <span>{aboutItem.icon}</span> {aboutItem}
              </li>
            )
          })
          }
      </ul>
      <h3>Bio</h3>
      <p className='about-bio>{aboutData.bio)</p>
  </section>
)};
```
*// expected output*


<h2>About me</h2>

- :family: Father to the coolest little 2yo
- :books: Life long learner
- :fishing_pole_and_fish: Avid fisherman
- :deciduous_tree: Nature lover
- :art: Artist
- :ghost: Horror and Sci-fi movie fan

<h3>Bio</h3>

I spent a decade creating G-code programs to machine aerospace parts out of raw metals. My curious nature led me to higher level languages. My love of learning and creative nature left me creating silly games and programs in my free time. My passion pushed me to dive deeper and continue learning more. Nowadays I enjoy creating Full Stack apps using the MERN stack, but I am always up to learning new languages and tools! Some areas I'd love to explore is block chain development, android development, Java, and Python.


<!---
TKravel/TKravel is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
