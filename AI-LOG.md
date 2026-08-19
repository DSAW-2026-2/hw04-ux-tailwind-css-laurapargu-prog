# AI-LOG.md

## Did you use AI to generate Tailwind classes? Did you also use it for the wireframes?

I used AI mainly as a guide while rebuilding the landing page with Tailwind,
not to generate the finished page and hand it over as-is. I explained what I
wanted each section to look like, and the AI suggested utility classes for
spacing, colors, and the `dark:` variant syntax, which I then reviewed and
adjusted directly in the HTML. I also used AI for command-line help along the
way — things like unzip commands and general git/bash tasks while managing the
project files — not for writing the page content itself.

For the wireframes, I used Figma's AI-assisted tool (Figma Make) to get a
starting point for the screens, and then adjusted the states and layout from
there. So AI acted more like an assistant that sped up repetitive parts of the
process, while the structure and the actual design decisions were still made
by me.

## What did you modify and why?

I modified several of the AI-suggested Tailwind classes based on how the page
actually looked once rendered. The main changes were around the color palette
— I adjusted colors like the dark blue `#080736` and its related shades so the
dark mode version felt consistent instead of just inverting colors randomly.
I also tweaked spacing, border radius, and hover states on the cards because
the first suggestions didn't quite match the layout I had in mind.

Beyond styling, I had to write and adjust the JavaScript for the dark mode
toggle myself so it correctly read and saved the theme in `localStorage`,
since that logic needed to match exactly how the Tailwind `dark:` classes were
being applied.

## What did you learn about Tailwind that you wouldn't have learned if AI had done everything?

The hardest part to understand at first was how the `dark:` variant actually
works together with `darkMode: "class"` in the Tailwind config — I didn't
immediately get why toggling one class on `<html>` was enough to flip the
whole page's theme instead of needing separate dark-mode CSS rules. Going
through it class by class instead of just accepting the AI's suggestions
helped me actually understand that behavior.

I also learned the real difference between the responsive prefixes (`sm:`,
`md:`, `lg:`) and how Tailwind's mobile-first approach works: unprefixed
classes apply by default, and each prefix only overrides the style from that
breakpoint upward. Working through the utility classes manually also made it
clearer how spacing, flex/grid, borders, and shadows compose together to build
a component, instead of treating Tailwind like a black box that just produces
a finished design.
