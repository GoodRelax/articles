document.addEventListener('DOMContentLoaded', () => {
  const codeBlocks = document.querySelectorAll('pre');

  codeBlocks.forEach((codeBlock) => {
    if (codeBlock.querySelector('.copy-btn')) return;

    const button = document.createElement('button');
    button.className = 'copy-btn';
    button.type = 'button';
    button.innerText = 'Copy';

    button.addEventListener('click', () => {
      const codeText = codeBlock.innerText;

      navigator.clipboard.writeText(codeText).then(() => {
        button.innerText = 'Copied!';
        button.classList.add('copied');

        setTimeout(() => {
          button.innerText = 'Copy';
          button.classList.remove('copied');
        }, 2000);
      }).catch(err => {
        console.error('Copy failed:', err);
      });
    });

    codeBlock.appendChild(button);
  });
});
