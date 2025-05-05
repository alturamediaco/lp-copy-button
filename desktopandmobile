document.addEventListener('DOMContentLoaded', function () {
  const copyButtons = document.querySelectorAll('.copy-btn, .copy-btn-mob');

  copyButtons.forEach(button => {
    button.addEventListener('click', function () {
      const isMobile = button.classList.contains('copy-btn-mob');
      const wrapSelector = isMobile ? '.copy-wrap-mob' : '.copy-wrap';
      const textSelector = isMobile ? '.copy-text-mob' : '.copy-text';

      const tickerWrap = button.closest(wrapSelector);
      const ticker = tickerWrap?.querySelector(textSelector);
      const textToCopy = ticker?.innerText.trim();
      if (!textToCopy) return;

      navigator.clipboard.writeText(textToCopy);

      const label = button.querySelector('.copy-label');
      const originalText = label.textContent;
      label.textContent = "Copied!";

      button.classList.add('clicked');

      setTimeout(() => {
        label.textContent = originalText;
        button.classList.remove('clicked');
      }, 1200);
    });
  });
});
