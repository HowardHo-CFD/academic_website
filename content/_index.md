---

---

<h3 id="quote-typer"></h3>

<script src="https://unpkg.com/typeit@8.8.7/dist/index.umd.js"></script>
<script>
  const quotes = [
    "\"If we knew what we were doing, it wouldn't be called research\" - Albert Einstein",
    "\"Who owns the mesh, owns the solution\" - Hrvoje Jasak",
    "\"All models are wrong, but some are useful\" - George Box",
    "\"Roads? Where we're going, we don't need roads.\" - Dr. Emmett Brown",
    "\"Computers are useless. They can only give you answers.\" ― Pablo Picasso",
    "\"Nothing in life is to be feared, it is only to be understood.\" — Marie Curie",
    "\"I have not failed. I've just found 10,000 ways that won't work.\" — Thomas Edison",
    "\"Any sufficiently advanced technology is indistinguishable from magic.\" — Arthur C. Clarke",
    "\"Never tell me the odds.\" — Han Solo",
    "\"If debugging is the process of removing bugs, then programming must be the process of putting them in.\" — Edsger W. Dijkstra",
    "Caffeinated, Frustrated, Despaired (CFD)"
  ];

  // Fisher-Yates shuffle
  for (let i = quotes.length - 1; i > 0; i--) {
    const j = Math.floor(Math.random() * (i + 1));
    [quotes[i], quotes[j]] = [quotes[j], quotes[i]];
  }

  new TypeIt("#quote-typer", {
    strings: quotes,
    speed: 60,
    breakLines: false,
    loop: true,
    lifeLike: false
  }).go();
</script>

