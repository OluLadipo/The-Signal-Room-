[README (2).md](https://github.com/user-attachments/files/34595760/README.2.md)
# The Signal Room

Your manager sends "hey, do you have a minute to chat?" with no context. Your heart rate jumps to 118. You start replaying everything you did this week.

This is the room for that.

### ✧ [Step inside](https://thesignalroom-oluladipo.netlify.app/)

*For people who are neurodivergent or wired differently at work.*

---

## Four rooms

**The Decoder.** Eight real work messages, the kind that wreck your whole afternoon. Each one gets decoded three ways: what you hear, what it usually means, and what to do next. Plus a script you can copy and send. Watch the heart meter drop from 118 bpm to 72 as each one clicks.

**Your Wiring.** Six questions. One of five work archetypes. Find out if you're the Deep Diver, the Pattern Seer, the Spark, the Quiet Radar or the Steady Architect, and what actually fuels and drains you.

**The Manual.** Build a "how to work with me" guide in a couple of minutes. How you communicate, how you focus, how you take feedback, what to do when you're overloaded. Then copy it with a ready-made note for your next one-on-one.

**Stim Mixer.** Rain, ocean, brown noise, soft hum and chimes. Mix your own or tap a preset for focus, calm or sleepy.

## The signal clears up

At the top of the page there's a static-filled signal line. Every message you decode, every room you finish, it gets a little cleaner. See how close to 100% you can get it.

Lumi, the little guide with the antenna, is waiting to say hi.

And if the animations are a lot, flip on **calm mode**. Everything holds still.

## Behind the scenes

A few crumbs from the code. The rest stays in the room.

**The signal is literally noise fading out.** The wave is a clean sine curve with static layered on top, and the static shrinks as your clarity goes up:

```js
const noise = (1 - c) * 46;
const clean = Math.sin(x / w * Math.PI * 6 + t * 1.4) * 22 * (.4 + .6 * c);
```

**Clarity is earned.** Decoding messages, getting your archetype and copying your manual all count:

```js
function clarity(){
  const v = (st.seen.length + (st.result ? 2 : 0) + (st.copied ? 2 : 0)) / 12;
  return Math.min(1, v);
}
```

**Brown noise, made from scratch.** No audio files. Random static gets smoothed sample by sample until it turns into that deep, steady rumble:

```js
last = (last + .02 * w) / 1.02;
```

**Your stuff stays yours.** Your archetype, your manual and your mixer levels are saved in your own browser. Nothing gets sent anywhere.

What's inside each decoded message, which archetype you'll land on, what Lumi looks like when you get there... you'll have to step inside.

## Built with

One HTML file. Vanilla JavaScript, canvas, hand-drawn SVG and the Web Audio API. No frameworks, no audio files, no build step. Respects reduced-motion settings.

## Made by

**Olu Ladipo** · Oluméism
[Portfolio](https://oluladportfolio.netlify.app/) · [LinkedIn](https://www.linkedin.com/in/oluladipoinsights) · [Shop](https://olumeism.gumroad.com)

### ✧ [Clear your signal](https://thesignalroom-oluladipo.netlify.app/)
