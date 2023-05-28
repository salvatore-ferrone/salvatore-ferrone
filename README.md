### Hi there 👋

<!--
**salvatore-ferrone/salvatore-ferrone** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->

when testing the website locally do:
``` bash
hugo server
```

then, when you want to send the code to the server do:
``` bash
cd ./salvatore-ferrone/personalsite/public
hugo -t hugo-blog-awesome
git remote -v  
git status
git add .
git commit -m "commit message"
git push origin main 
```

the command:
```
hugo -t hugo-blog-awesome
```
Creates all of the static assets and puts them in the public folder.
I made the public folder a submodle of the `salvatore-ferrone.github.io` repository. Thus, when within this folder, when we push to the main brain, we are pushing to the main branch of the submodule: `salvatore-ferrone.github.io`.

The static assets get updated immediately and the website should be updated instantaneously. 