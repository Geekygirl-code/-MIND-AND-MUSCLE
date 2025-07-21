---
title: "ABS WORKOUT PLAN"
date: 2019-10-29T10:07:47+06:00
draft: false

# post thumb
image: "images/featured-post/post-1.jpg"

# meta description
description: "this is meta description"

# taxonomies
categories:
  - "Android And Gaming"
tags:
  - "Photos"
  - "Game"
  - "React"
  - "Python"
  - "New"

# post type
type: "featured"
---

Follow this workout plan diligently to get your pack of abs and increase the temperature this summer!

Dumbbell crunches (10 reps, 10 sec rest)

Hanging leg raises (10 reps, 10 sec rest)

Decline plank with foot touch (10 reps, 10 sec rest)

Bicycle crunches (15 each side, 10 sec rest)

WORKOUT PLANS

<style>
  #like-btn {
    background: none;
    border: none;
    cursor: pointer;
    font-size: 18px;
    color: #ccc; /* light gray for unliked */
    transition: color 0.2s ease;
    user-select: none;
  }
  #like-btn.liked {
    color: red;
  }
  #like-count {
    font-size: 16px;
    margin-left: 8px;
    vertical-align: middle;
    color: #333;
    user-select: none;
  }
</style>

<button id="like-btn" aria-label="Like button">❤️</button>
<span id="like-count">0</span>

<script>
  const likeBtn = document.getElementById('like-btn');
  const likeCountSpan = document.getElementById('like-count');

  // Load count and liked state from localStorage (per visitor)
  let count = parseInt(localStorage.getItem('likeCount')) || 0;
  let liked = localStorage.getItem('liked') === 'true';

  likeCountSpan.textContent = count;

  if (liked) {
    likeBtn.classList.add('liked');
  } else {
    likeBtn.classList.remove('liked');
  }

  likeBtn.addEventListener('click', () => {
    if (!liked) {
      count++;
      liked = true;
      likeBtn.classList.add('liked');
      // Send GA4 event if available
      if (typeof gtag === 'function') {
        gtag('event', 'blog_post_like', {
          event_category: 'engagement',
          event_label: window.location.pathname,
          value: count
        });
      }
    } else {
      // Optional: allow un-like
      count = count > 0 ? count - 1 : 0;
      liked = false;
      likeBtn.classList.remove('liked');
    }
    likeCountSpan.textContent = count;
    localStorage.setItem('likeCount', count);
    localStorage.setItem('liked', liked);
  });
</script>
