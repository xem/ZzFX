# ZzFX - Zuper Zmall Zeeded Zound Zynth
By Frank Force - 2019

ZzFX Features
- Micro synth engine with 6 controllable parameters, you can add more.
- Seeded sounds can also be played using as few as 4 bytes, ex: z(3)
- Able to produce a wide variety of sound effect types.
- Tiny footprint, after being minified with closure ZzFX lib is 375 bytes!
- Compresses well with JSCrush (alongside the rest of your game)
- You can include just the Z function by itself if you don't want seeds.

ZzFX UI Features
- This entry is mostly just a wrapper around ZzFX.
- When the page loads it is filled with cards each corresponding to a seed.
- Just click on a card to play the sound for that seed.
- Each card also has a unique visual apearance tied to that seed.
- You can click on the ZzFX logo to copy the last played seed or change it!
- There is a section in code to set up a preset custom card layout.

Additional notes...
- Be careful of variable name collisions! vars used are ZzFfXRr, don't use them.
- If you use closure compiler, it will shorten the internal variable names.
- You can use R() instead of Math.Random() to save space.
- Feel free to completely modify any of this code!
- Try playing multiple sounds at once for unique effects.
- You can also use negative seeds.
- Try using any repeated numbers in your code as seeds, maybe you'll get lucky.
- There is built in 5% frequency randomness in z(), you can change it.
- You can also add parameters to z(), like a float to scale volume by, etc.

**Here's the latest version of the minfied code you can use directly!**

```
// ZzFX - Minified Code (375 bytes) - MIT License - Copyright (c) 2019 - Frank Force
z=e=>{h=R(5E3);s=r;r=e;R();R();Z((R(1E5)+h)/1E6,f=R(1E5),R(9),R(f),R(1E5)/1E9,R(1E5));r=s}
Z=(e,l,m,g,n,p)=>{h=[];for(F=f=0;++F<l;f+=1+R(m))h[F]=Math.cos(f*e*Math.cos(f*n+p))*(F<g?F/g:1-(F-g)/(l-g))
F=X.createBuffer(1,1E5,1E5);F.getChannelData(0).set(h);h=X.createBufferSource();h.buffer=F;h.connect(X.destination);h.start()}
X=new AudioContext;r=0
R=e=>(r^=r<<3,r^=r>>2,r%e)
```
