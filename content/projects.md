+++
title = "Projects"
date = "21 Nov 21 7:44 EEST"
+++
Hi! I'm Alexandros. I make websites (see below 👇) and I design for print (e.g. this <a href="https://www.embitsakis.com/?=$3#view=persistent,0" class="intext" target="_blank">book</a>, this <a href="https://www.vogiatzogloucollection.gr/uploads/docs/2018/04/153.pdf" class="intext" target="_blank">one</a> and this <a href="https://www.vogiatzogloucollection.gr/uploads/docs/2018/04/154.pdf" class="intext" target="_blank">one</a>). Check out my drawings on <a href="https://instagram.com/onedrawingperday" class="intext" target="_blank">IG</a>. To say “<span style="color:red">hi!</span>” just click on the bouncing smiley. Cheers!

[https://www.potentialproject.gr](https://www.potentialproject.gr)
[https://www.embitsakis.com](https://www.embitsakis.com)
[https://www.christofiscollection.gr](https://www.christofiscollection.gr)
[https://www.galleryalma.com](https://www.galleryalma.com)
[https://www.svetlin.gr](https://www.svetlin.gr)
[https://www.mantalinapsoma.com](https://www.mantalinapsoma.com)
[https://www.oneangelabroad.com](https://www.oneangelabroad.com)
[https://www.dimitrisgeorgakopoulos.gr](https://www.dimitrisgeorgakopoulos.gr)
[https://assembliessummit.tumblr.com](https://assembliessummit.tumblr.com)
[https://unknownartistproject.tumblr.com](https://unknownartistproject.tumblr.com/)

{{< smiley.inline >}}
    {{/* Get address, protocol and other parameters */}}
{{- $address := "aa@onedrawingperday.com" -}}
{{- $protocol := "mailto" -}}
{{- $parts := split $address "@" -}}
{{- $user := (index $parts 0) -}}
{{- $domain := (index $parts 1) | default "" -}}
{{/* Compute md5 fingerprint */}}
{{- $fingerprint := md5 (print $address $protocol (index (seq 999 | shuffle) 0)) | truncate 8 "" -}}
<a id="smiley" data-user="{{ range $index := seq (sub (len $user) 1) 0}}{{ substr $user $index 1}}{{ end }}"{{ with $domain }} data-domain="{{ range $index := seq (sub (len $domain) 1) 0}}{{ substr $domain $index 1}}{{ end }}"{{ end }}>
  <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" width="50" height="50" baseProfile="full" viewBox="-21 -21 42 42">
    <defs>
      <radialGradient id="b" cx=".2" cy=".2" r=".5" fx=".2" fy=".2">
        <stop offset="0" stop-color="#fff" stop-opacity=".7"/>
        <stop offset="1" stop-color="#fff" stop-opacity="0"/>
      </radialGradient>
      <radialGradient id="a" cx=".5" cy=".5" r=".5">
        <stop offset="0" stop-color="#ff0"/>
        <stop offset=".75" stop-color="#ff0"/>
        <stop offset=".95" stop-color="#ee0"/>
        <stop offset="1" stop-color="#e8e800"/>
      </radialGradient>
    </defs>
    <circle r="20" fill="url(#a)" stroke="#000" stroke-width=".15"/>
    <circle r="20" fill="url(#b)"/>
    <g id="c">
      <ellipse cx="-6" cy="-7" rx="2.5" ry="4"/>
      <path fill="none" stroke="#000" stroke-linecap="round" stroke-width=".5" d="M10.6 2.7a4 4 0 0 0 4 3"/>
    </g>
    <use xlink:href="#c" transform="scale(-1 1)"/>
    <path fill="none" stroke="#000" stroke-width=".75" d="M-12 5a13.5 13.5 0 0 0 24 0 13 13 0 0 1-24 0"/>
  </svg>
</a>
  <script>
       function updateKeyframes() {
      const styleSheet = document.styleSheets[0];
      const vw = window.innerWidth;
      const vh = window.innerHeight;

      const moveXKeyframes = `
        @keyframes moveX {
          from { left: 0; } to { left: ${vw - 50}px; }
        }
      `;
      const moveYKeyframes = `
        @keyframes moveY {
          from { top: 0; } to { top: ${vh - 50}px; }
        }
      `;

      // Remove existing keyframes
      for (let i = styleSheet.cssRules.length - 1; i >= 0; i--) {
        if (styleSheet.cssRules[i].name === 'moveX' || styleSheet.cssRules[i].name === 'moveY') {
          styleSheet.deleteRule(i);
        }
      }

      // Insert new keyframes
      styleSheet.insertRule(moveXKeyframes, styleSheet.cssRules.length);
      styleSheet.insertRule(moveYKeyframes, styleSheet.cssRules.length);
    }

    window.addEventListener('resize', updateKeyframes);
    updateKeyframes(); // Initial call to set keyframes

    const smiley = document.getElementById('smiley');

    smiley.addEventListener('touchstart', () => {
      smiley.style.animationPlayState = 'paused';
      smiley.querySelector('svg').style.transform = 'scale(1.5)';
      smiley.querySelector('svg').style.filter = 'drop-shadow(0 0 15px red)';
    });

    smiley.addEventListener('touchend', () => {
      smiley.style.animationPlayState = 'running';
      smiley.querySelector('svg').style.transform = 'scale(1)';
      smiley.querySelector('svg').style.filter = 'none';
    });
  </script>
<script>
  // Get the smiley element
  var smileyElement = document.getElementById("smiley");

  // Reverse the user and domain stored in the data attributes
  var user = smileyElement.getAttribute("data-user").split('').reverse().join('');
  var domain = smileyElement.getAttribute("data-domain").split('').reverse().join('');

  // Construct the email address
  var email = user + "@" + domain;

  // Set the mailto link in the existing <a> element
  smileyElement.href = "mailto:" + email;
</script>
{{< /smiley.inline >}}