# Time-Scene

> A booking and scheduling widget where the whole scene follows the time you pick.
> Choose a day and a time slot, and your background video moves through the day, from sunrise to night. Drop it into any website.

**Status: work in progress.** Nothing here is final yet. The usage example below shows the planned design.

---

## What is it?

`Time-Scene` is a scheduling widget for websites. A visitor picks a day from a calendar, then moves through the available time slots. As they move, the background video and the clock change with them: pick 6:30 AM and you see sunrise, pick 9:00 PM and you see night.

It is meant for any site that lets people book a time, such as consultants, clinics, studios, restaurants, tutors and event pages.

## Why?

Most booking widgets look the same. This one makes choosing a time feel like something, and it is built so that anyone can fit it to their own brand and their own video.

## Planned features

- Day calendar and time-slot picker
- Frosted-glass panel over a full-screen background video
- Video, clock and scene follow the selected time
- Bring your own time-lapse video
- Theme that adapts to your video (colors, glass tint)
- Works on any website, with no framework needed
- Mobile and keyboard friendly

## How it will be used (planned)

```html
<script src="time-scene.js"></script>

<time-scene
  video="/videos/my-city-timelapse.mp4"
  date="2026-09-30">
</time-scene>
```

Your website decides what happens after a time is chosen. The widget tells your site which slot was picked, and your site handles the actual booking.

> The widget does **not** store bookings or run a server in version 1. It is the front end of a booking experience, and you connect it to the booking system you already use.

## Use your own video

You can replace the sample video with your own time-lapse. For the best result:

| Requirement | Why |
|---|---|
| One continuous clip covering a full day (sunrise to night) | The slider moves through the clip |
| Camera completely still | Smooth scrubbing |
| MP4 (H.264), no audio | Works everywhere |
| 1080p or smaller, about 10 to 30 MB | Loads fast |
| Encoded with frequent keyframes | Without this, scrubbing is jumpy |

A helper script to check and prepare your video is on the roadmap.

## Roadmap

- [ ] Full-screen background video
- [ ] Frosted-glass panel
- [ ] Time-slot list
- [ ] Video follows the selected time
- [ ] Clock display
- [ ] Day calendar
- [ ] Package as a single `<time-scene>` tag
- [ ] Theme colors adapt to the video
- [ ] Video preparation helper
- [ ] Accessibility and mobile support
- [ ] Documentation and demo site
- [ ] Version 2: upload your own video through a web page

## Credits

- Sample image: photo by **Msganaw Wogaso** on [Unsplash](https://unsplash.com)
- Sample video: generated from that image using an AI video tool

## License

MIT
