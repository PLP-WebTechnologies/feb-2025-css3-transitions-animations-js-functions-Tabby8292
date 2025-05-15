# CSS3 Transitions, Animations, and Advanced JavaScript Functions

## Objectives

Create smooth CSS transitions and animations.body.light {
  background-color: #ffffff;
  color: #000000;
}

body.dark {
  background-color: #222222;
  color: #ffffff;
}

@keyframes pulse {
  0% {
    transform: scale(1);
    color: inherit;
  }
  50% {
    transform: scale(1.2);
    color: #ff4081;
  }
  100% {
    transform: scale(1);
    color: inherit;
  }
}

.pulse-animation {
  animation: pulse 0.5s ease;
}

Use JavaScript functions for dynamic behavior.// Load saved theme from localStorage
window.addEventListener('DOMContentLoaded', () => {
  const savedTheme = localStorage.getItem('theme') || 'light';
  applyTheme(savedTheme);
  document.getElementById('theme').value = savedTheme;
});

// Apply selected theme and save it
document.getElementById('theme').addEventListener('change', (e) => {
  const selectedTheme = e.target.value;
  applyTheme(selectedTheme);
  localStorage.setItem('theme', selectedTheme);
});

// Animate title on button click
document.getElementById('animateBtn').addEventListener('click', () => {
  const title = document.getElementById('title');
  title.classList.remove('pulse-animation'); // Reset animation
  void title.offsetWidth; // Force reflow
  title.classList.add('pulse-animation');
});

// Helper to apply theme class to body
function applyTheme(theme) {
  document.body.classList.remove('light', 'dark');
  document.body.classList.add(theme);
}

Implement local storage for data persistence.

## Instructions
Add CSS animations to elements like buttons or images.

>[!NOTE]
> - Write a JavaScript function that:
> - Stores and retrieves user preferences using localStorage.
> - Implements an animation triggered by user actions.

## Tasks

Create a CSS animation.
Store data in localStorage.
Apply JavaScript to trigger animations.

Happy Coding! 💻✨
