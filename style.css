const jokeEl = document.getElementById('joke');
const newBtn = document.getElementById('newJoke');
const tweetBtn = document.getElementById('tweet');

async function fetchJoke() {
  jokeEl.textContent = 'Loading…';
  try {
    const res = await fetch('https://icanhazdadjoke.com/', {
      headers: { 'Accept': 'application/json' }
    });
    if (!res.ok) throw new Error('Network response was not ok');
    const data = await res.json();
    jokeEl.textContent = data.joke;
  } catch (err) {
    jokeEl.textContent = 'Could not fetch a joke. Try again later.';
    console.error('fetchJoke error:', err);
  }
}

newBtn.addEventListener('click', fetchJoke);
tweetBtn.addEventListener('click', () => {
  const text = encodeURIComponent(jokeEl.textContent);
  const url = `https://twitter.com/intent/tweet?text=${text}`;
  window.open(url, '_blank');
});

// Fetch a joke on load
window.addEventListener('load', fetchJoke);
