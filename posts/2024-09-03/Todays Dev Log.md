# Todays Dev Log

## Nova Blog
Made the favicon for the Nova Blog, but figured I should try to have AI generate something for me since I didn't want to have to break out a photo editor just to make a 64x64 simple logo, so I made a really quick and dirty shape and tried to put it into the AI to clean it up. Here's the results:
#### Initial:
![[Untitled.png]]

#### Result:

![[symmetrical_32x32_logo.png]]

Not very good at prompting, but here's what I put in: 
> Could you turn this into a 32x32 pixel art style logo and make it symmetrical, fixing up the proportions of the sides?

Safe to say AI isn't taking our jobs anytime soon. Mine isn't perfect, but here's what I wanted:

![[blackBg.png]]

Also found out the images do not translate, so I'm updating the generation file to compensate

## Nova Library

Wasn't super productive on the Library today, but generally where I'd like to start is removing all imports in components which refer to `@/pages/*` and take those functions/data and put them in files that only export.

Generally nothing that exports should import something from a recipient of that export, but that flow is all over Nova Library. In the same way, data should not be drilled or passed between components directly. Single Source of Truth as it were.

I started building the app with this principle, but it fell apart at some point. Now I'd like to clean up the app, and kind of need to as for things like the `ItemFieldRouter` component which generates field of whatever type is necessary where prop drilling, while direct, is happening and is ugly.