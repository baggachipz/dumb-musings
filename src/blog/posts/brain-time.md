---
layout: layouts/post.njk
title: Your brain's timing is lying to you.
description: Showing you how your brain processes time.
date: 2026-08-25
---

I recently listened to [Neil deGrasse Tyson's podcast](https://startalkmedia.com/show/your-inner-cosmos-with-david-eagleman/) With David Eagleman. In it, they discussed an [experiment](https://edge.org/conversation/brain-time) where people's perception of timing is skewed; sometimes, something can appear to happen before it even does. This fascinated me, so I cobbled together a little demonstration to play with. Enjoy!

<iframe
  id="brain-time"
  src="/experiments/brain-time/"
  title="Brain Time — temporal recalibration experiment"
  width="100%"
  height="820"
  allow="fullscreen"
  scrolling="no"
  style="border:1px solid #333;border-radius:12px;display:block;background:#111;overflow:hidden;box-sizing:content-box"></iframe>

<script>
(() => {
  const frame = document.getElementById("brain-time");
  const MIN_H = 400, MAX_H = 4000;

  // The height attribute is the content box, and the site's global
  // border-box would otherwise subtract the border from it, leaving the
  // frame's viewport short of its own content and scrolling inside itself.
  // content-box is set inline on the element; this is the reason why.

  window.addEventListener("message", event => {
    // Identity check first: never resize on a message from another frame.
    if (event.source !== frame.contentWindow) return;
    if (event.origin !== window.location.origin) return;
    if (!event.data || event.data.type !== "brain-time:height") return;

    const height = Number(event.data.height);
    if (!Number.isFinite(height)) return;
    frame.height = Math.min(MAX_H, Math.max(MIN_H, Math.ceil(height)));
  });

  // SPACE only reaches the experiment if the keyboard is inside the frame.
  frame.addEventListener("load", () => frame.contentWindow.focus());
})();
</script>