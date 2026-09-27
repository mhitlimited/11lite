const root = document.documentElement;
const themeToggle = document.getElementById('themeToggle');
const iconMoon = document.getElementById('iconMoon');
const iconSun = document.getElementById('iconSun');
const menuToggle = document.getElementById('menuToggle');
const menu = document.getElementById('menu');
const yearEl = document.getElementById('year');
const langToggle = document.getElementById('langToggle');

if (yearEl) yearEl.textContent = new Date().getFullYear();

const savedTheme = localStorage.getItem('theme');
const prefersLight = window.matchMedia && window.matchMedia('(prefers-color-scheme: light)').matches;

if (savedTheme === 'light' || (!savedTheme && prefersLight)) {
  root.classList.add('light');
  if (iconMoon) iconMoon.style.display = 'none';
  if (iconSun) iconSun.style.display = 'block';
}

if (themeToggle) {
  themeToggle.addEventListener('click', () => {
    const isLight = root.classList.toggle('light');
    localStorage.setItem('theme', isLight ? 'light' : 'dark');
    if (iconMoon) iconMoon.style.display = isLight ? 'none' : 'block';
    if (iconSun) iconSun.style.display = isLight ? 'block' : 'none';
  });
}

if (menuToggle && menu) {
  menuToggle.addEventListener('click', () => {
    menu.classList.toggle('open');
  });

  menu.querySelectorAll('a').forEach((a) => {
    a.addEventListener('click', () => menu.classList.remove('open'));
  });
}

const i18nDict = {
  en: {
    open: 'Open',
    download: 'Download',
    back: 'Back',
    preparing: 'Preparing your download…',
    seconds: 'seconds left'
  },
  bn: {
    open: 'খুলো',
    download: 'ডাউনলোড',
    back: 'পিছনে',
    preparing: 'ডাউনলোড প্রস্তুত হচ্ছে…',
    seconds: 'সেকেন্ড বাকি'
  }
};

function setLang(l) {
  const lang = i18nDict[l] ? l : 'bn';
  localStorage.setItem('lang', lang);
  document.querySelectorAll('[data-i18n]').forEach((el) => {
    const key = el.getAttribute('data-i18n');
    const pair = i18nDict[lang]?.[key];
    if (pair) el.textContent = pair;
  });
  if (langToggle) {
    langToggle.textContent = lang === 'bn' ? 'EN/BN' : 'BN/EN';
  }
}

if (langToggle) {
  langToggle.addEventListener('click', () => {
    const current = localStorage.getItem('lang') || 'bn';
    setLang(current === 'bn' ? 'en' : 'bn');
  });
  setLang(localStorage.getItem('lang') || 'bn');
}
