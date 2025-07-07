---
source: https://danielabaron.me/blog/learning-from-screencasts/?ref=writesoftwarewell.com
author:
  - "[[@DanielaMBaron]]"
published: 2022-11-01
---
2025-05-26 20:09

Status: #child 

Tags: [[learning-techniques]] [[dev]]

# Maximize learning from screencasts

**Update (March 2024):** I recently had an engaging conversation on the Geeking Out podcast with host Adriana Villela, where we discussed the challenges of keeping up with rapid changes in the tech world. We covered various learning methods, acknowledging that there's no one-size-fits-all approach. Drawing from my 20+ years of experience in the field, I shared some of my favorite learning resources and techniques. Additionally, I opened up about my own learning journey where I had to learn HashiCorp Nomad from scratch as part of a platform migration. If you're interested in gaining valuable insights into learning processes, I recommend [giving the episode a listen](https://geeking-out.simplecast.com/episodes/the-one-where-we-geek-out-on-how-to-learn-daniela-baron).

This post will cover some techniques to get the most out of online learning with screencasts. There are many services offering this including [Pluralsight](https://www.pluralsight.com/product/skills), , [Wes Bos Courses](https://wesbos.com/courses), and [Learn UI Design](https://www.learnui.design/) to name just a few. I happen to have the most experience with Pluralsight, but the advice in this post applies to all screencast style courses. Note that these are generally paid services.

## Definition

A screencast is a digital video recording of a computer screen while someone is using it, and usually includes audio narration. A course based on screencasts will have the instructor recording their screen while they run through presentation slides, terminal commands, setting up a development environment, writing code in an editor, running code, etc.

Typically these will be broken down into smaller sections rather than one massive recording. When taking the course, you can select which video to watch, then use the video player controls to pause, go forward, go back, speed up and so on. There is no time limit to complete the course, and no one is taking attendance.

## Passive Learning

Let's start with what not to do. Since the course format is video, it's tempting to treat this like a Netflix series, pop some popcorn, sit back, and binge watch.

This is the passive approach, and while not a complete waste of time, it's not the most effective way of learning. You're likely to forget most of what was covered. Instead, I recommend ==active learning==. This ==requires more effort and takes longer, but the payoff is more information retained and a higher quality learning experience.==

## Organize

One of the most effective ways to retain what you've learned is to write it down as you go. This requires some organization, a kind of [mise en place](https://en.wikipedia.org/wiki/Mise_en_place) for techies.

When starting a new course, create a directory. I suggest having one directory for all courses, then sub-directories for each course you take. For example, if taking a course on Idiomatic Ruby from Pluralsight:

```bash
cd ~/path/to/courses

mkdir idiomatic-ruby-pluralsight && cd idiomatic-ruby-pluralsight

mkdir exercises doc-images

touch README.md
```

The resulting directory will be something like this:

```bash
courses

└── idiomatic-ruby-pluralsight

    ├── README.md

    ├── doc-images

    └── exercises
```

The `README.md` is where the course notes will go. It doesn't have to be markdown, you could write in a plain text file, or even a Google/Microsoft/Libre Office document. But I've found that [markdown](https://en.wikipedia.org/wiki/Markdown) is optimal for technical writing as it supports syntax highlighted code blocks.

The `exercises` folder will be used for saving any code examples developed during the course. The `doc-images` folder is where you will place any screenshots - for example, if taking a course on css, svg, or developing a web app, it will be useful to save screenshots of what the app looks like as you build it up, and then reference these images in `README.md`.

Most courses are broken up into major sections, with each section having several smaller subsections with a short video for each. A good place to start organizing your notes is to create ==headings and subheadings matching the course structure==. This way you'll know where to add your notes as you're watching each video.

For example, here's the table of contents from the Idiomatic Ruby course on Pluralsight:

![idiomatic Ruby course TOC](https://danielabaron.me/static/6556559c5822fcfc6504ba6c77df42e9/00a4e/idiomatic-ruby-course-toc.png)

idiomatic Ruby course TOC

In this case, I would create headings in `courses/idiomatic-ruby-pluralsight/README.md` as follows. I also link to the main course website:

```markdown
# Idiomatic Ruby

My notes from Pluralsight [course](https://app.pluralsight.com/library/courses/ruby-idiomatic/table-of-contents).

## Blocks, Conditionals, and Symbols

### Blocks Coding

### Blocks Details

...

## Building Objects

### Desired Behavior

...
```

## Arrange Windows

If your monitor is wide enough, I've found the optimal window arrangement for watching course videos and taking notes and the same time is to have the video playing on the right half of the monitor, and the editor open on the left half. For example, here's a screenshot from when I was learning Idiomatic Ruby with Pluralsight, at the section where we're learning about Enumerable methods:

![screencast notes and video side by side](https://danielabaron.me/static/b0cccffe0da34be4343d735303f1c10d/5a190/screencast-notes-and-video-side-by-side.png)

screencast notes and video side by side

If that's awkward for you, try different arrangements or even put each one one a different monitor if using multiple monitors. Once you find an optimal window layout, stick with that for video learning.

## Take Notes

Now that you're organized for note taking, it's time to start watching the videos. But this is not the same as watching funny cat videos on Youtube.

==Every time a significant point is covered in the course, pause the video, and write down what you just learned in the corresponding section of `README.md` *in your own words*.== This is key, do not simply transcribe the instructor's words. Make sure you understand the concept enough that you could explain it to someone else, then write down that explanation. In fact, that someone else is "future you", who will look back on these notes several months from now to reference the material.

==The power of writing is that it makes you remember that you learned a topic, even if you don't remember the details.== Next time you need to recall that information, you'll be able to pull up your notes and find the section where you wrote it down. Some examples from my experience include negative indexing in Python and the splat operator in Ruby. I haven't used either of these often enough to have memorized the details, but distinctly remember learning about them in courses and can quickly find these topics in my notes whenever I encounter some code that uses these.

Furthermore, while video is a great ==medium for learning==, it's ==slow for recall==. Later at work, if you need to pull up a detail that was covered in the course, it would be too ==slow to try and find in which video section this detail was covered== and watch the video again. Or your membership might have expired or the course is no longer available. Your notes serve as a permanent reference.

## Write Code

Since these are technical courses, there will be many sections where the instructor writes some code and explains it. This is another good place to pause the video. Write the code yourself in the `exercises` directory you created earlier, make sure it compiles/runs and returns the same result as shown in the course.

Do not just watch the instructor code or copy/paste from the solutions (if provided), it won't stick. ==There's something very powerful about typing out the code yourself.== After each section you type out, ==look back on it and make sure you understand every line==. Go ahead and add explanatory comments, this is not the time to worry about "clean code" should there be comments or not. This is educational material - ==add any comments that will help future you understand the code==.

==Another variation on this is sometimes the instructor will announce the next problem that will be solved in code.== This is a good time to pause the video and try to write out the code yourself *before* the instructor shows how to do it. Then compare your solution to the instructors.

Finally, you'll want to link up the code you wrote to the `README.md` notes so the explanations you've been writing flow with the code. One way is to place relevant snippets of code directly in the `README.md` using fenced code blocks. Another way is to link from the `README.md` to the specific file in the `exercises` directory. For example:

![screencast example code](https://danielabaron.me/static/b21e478194874031da2208e6326aaef3/5a190/screencast-example-code.png)

screencast example code

## Screenshot Flow

For courses that have a visual component - such as learning a framework for building a web app, css, svg, etc, you'll want to take screenshots of what you're building and save these as part of your notes. Here's the flow I use for Mac:

1. Cmd + Control + Shift + 4 to turn the cursor into a crosshair. Right click on the mouse and drag to capture the relevant portion of the screen. When you release the mouse, the selection will be saved to the clipboard.
2. Open the [Preview app](https://support.apple.com/en-ca/guide/preview/welcome/mac) using either [Alfred](https://www.alfredapp.com/) or [Spotlight Search](https://support.apple.com/en-ca/guide/mac-help/mchlp1008/mac). The default hot key for Alfred is Option + Space. For Spotlight Search it's Command + Space.
3. Hit Cmd + N to create a new file. It will automatically place the contents of the clipboard into the new file.
4. Hit Cmd + S and save the file to `/path/to/course/doc-images`.
5. Update `README.md` to link to the newly created image, for example:
```markdown
Here is what the homepage looks like:

![brief description of image](doc-images/my-screenshot.png "brief description of image")
```

Windows users see this [support article](https://support.microsoft.com/en-us/windows/use-snipping-tool-to-capture-screenshots-00246869-1843-655f-f220-97299b865f6b) on using the Snipping Tool to capture screenshots.

It seems like a lot of steps but since most of this flow uses keyboard shortcuts, you'll get very efficient after doing it a few times. More on keyboard shortcuts in the next section.

## Keyboard Shortcuts

The process of taking notes and writing code exercises from the video requires frequent pausing of the video player in the browser tab, where the course is hosted, switching to your code editor, then going back to the video player, possibly rewinding back a few seconds if you missed something. Trying to do all this with a mouse will be very tedious and could lead to wrist and shoulder pain due to frequency of switching.

I highly recommend learning keyboard shortcuts to control all these activities. The majority of video players I've used support the following:

- Space Pause video playback (or resume if currently paused).
- Left Arrow Go back 10 seconds.
- Right Arrow Go forward 10 seconds.

For switching between applications such as browser and code editor, use Command + Tab for Mac, or Alt + Tab for Windows.

## Expect Issues

Sometimes you'll run into an issue where your code doesn't produce the same result as the instructor's or errors, doesn't compile etc. Don't shrug and skip over this. It's important to investigate why your result is different. Here are some possible reasons:

**Bug in your code:** Review your code carefully and compare it to instructors for any typos. This is the root cause of many issues I've encountered in my years of learning from screencasts.

**Version mismatches:** It's possible that you have a different version of the language, library, framework etc. than what the instructor has installed. Go back to the beginning of the course and check if it mentions what version(s) are being used, then make sure to install those on your system. Many languages have version managers to make it easy to switch between projects using different versions such as [nvm](https://github.com/nvm-sh/nvm), [pyenv](https://github.com/pyenv/pyenv), [rbenv](https://github.com/rbenv/rbenv), etc. Use these wherever possible.

**Operating system mismatch:** You'll be able to tell what operating system the instructor is using from the video recordings of their screen. Windows and Mac are the most common, with the occasional instructor using Linux. It can happen that some code could be operating-system specific such as file paths and line endings. If you encounter this, update the code for your OS.

**Bug in course:** The last possibility is a bug in the course. For example, some video editing may have caused a few lines or an entire file that are needed to make the code work get missed from the recording. So even if you've copied the video code exactly, it still may not work. Some course platforms provide the code exercises as downloads. In this case, compare the downloaded solution files to your code to see if something's missing. It may also be possible to contact the instructor to ask about this, for example, Pluralsight integrates the Disqus commenting system for questions and answers. However, it could take a few days to receive an answer. You can also try to do a web search and solve the problem yourself, your solution may end up being different than what was in the course, but it will still be a valuable learning experience to solve the problem.

After the issue is fixed, add some ==notes about what you encountered== and how you fixed it in the `README.md`. Most importantly, ==try not to get frustrated== about encountering an issue. ==This is part of the learning experience. It's similar to real world development, where sometimes the most learning occurs from fixing a bug rather than when all goes smoothly.==

## Tangents

One of the benefits of asynchronous learning over real-time/in-classroom, is the ability to ==explore something that piques your curiosity in more detail==, but isn't the main topic. This could be an API that's used, or maybe the course only covers the happy path and you want to see what happens during some exceptional conditions.

Some examples from my experience - a Rails course I took was using the SQLite database, and added a length constraint to one of the fields but didn't test it. When I tried it, the length limit wasn't enforced. Doing some research revealed that ==although SQLite supports the SQL syntax for setting length limits on `VARCHAR` fields, it's not enforced==.

Another course I took invoked the `authenticate` method on a User model, which returns the user instance if authentication passed, or false otherwise. I got curious about where this method is defined as we hadn't written any code for it. Digging into this I learned about the ==`inspect` method to find more information about a method in Ruby==, and eventually traced through the location in the Rails source code.

==When finished exploring a tangent, make sure to add the results of this exploration to the `README.md`==. This will solidify what you've just learned.

## Publish (Optional)

This step is optional, but I recommend saving/publishing your notes somewhere they'll be easily searchable across devices. This could be any cloud storage such as Dropbox, OneDrive, Google Drive etc. My preference is to push the entire course folder to a Github repository. This is especially a good option when writing the notes in Markdown as they'll be automatically rendered on Github.

For example, given the following directory structure:

```bash
courses

└── idiomatic-ruby-pluralsight

    ├── README.md

    ├── doc-images

    └── exercises
```

I would create a new *empty* Github repository named `idiomatic-ruby-pluralsight` on [Github](https://github.com/), with no generated files such as readme or license). It's up to you if you want to make the repo public or private.

Then from the terminal:

```bash
cd idiomatic-ruby-pluralsight

# Create a local git repository

git init

git add .

gc -m "Initial commit"

# Connect it to the remote repository on Github

git remote add origin git@github.com:your-github-username/idiomatic-ruby-pluralsight.git

git branch -M main

git push -u origin main
```

You don't need to wait until you're finished the course to publish your notes. I work on small amounts at a time and publish as I go (more on this in the next section). This is to avoid the catastrophic situation of a hard drive crash and losing all the precious notes.

## Break it Up

I do not advise attempting to complete a course in a single session. For example, many courses on Pluralsight are approximately 2 to 3 hours in duration. ==This sounds like it could be completed in a morning or afternoon. However, remember you're going to be stopping to take notes, do the exercises, go on tangents, and fix issues.== Not only does this extend the time to complete the course, it consumes significantly more mental energy than passively watching.

There's also a limit to how much new information the brain can absorb all at once. This varies by person, but ==I've found that doing one or at most two subsections in a single learning session is just the right amount to optimize absorbing new information==. This avoids exhaustion so I'm looking forward to returning for a session another day. More on this in the next section on habits.

## Make it a Habit

One problem that can occur when the videos can be watched at any time, is that after an initial bout of enthusiasm, learning drops off. Somehow there's never enough time in the day to get around to sitting down with the videos and writing your notes. Or you wait to feel inspired but by the time it occurs to you to do some learning, its late and you're tired. The solution to this is to make learning a *habit*:

> A habit is a routine or practice performed regularly; an automatic response to a specific situation.

Here are a few techniques for cultivating the habit of learning.

### Small amounts regularly

It can be overwhelming to find an hour or more in a typical day to fit in learning. Instead, start with a very small amount, even 5 - 10 minutes, and commit to this several days a week. ==For example, Tuesday, Wednesday, and Thursday of each week, after dinner, you'll sit down for just 10 minutes with your code editor and the video course to listen and take notes.== That's just an example, pick whichever days and times work for you, as long as its regularly occurring.

You might be thinking what difference could 10 minutes possibly make? The key here is making the ==learning activity happen regularly==. Those small increments will add up surprisingly quickly. ==For example, 10 minutes a day, 3 times per week is a half hour. In a year (let's say approximately 50 weeks, accounting for some vacation), that's 25 hours.== Furthermore, with enough repetition, you may find that 10 minute session stretch out to 20 minutes of even a half hour, especially if you're enjoying what you're learning. That would get you to 75 hours per year! Imagine how much learning you can cover in that time.

==It's fine if you don't get through an entire subsection. Simply add a line to your notes== such as `Left off at 2:35 of Map: Transforming Collections`. This makes it easy to pick up again in your next learning session.

### Make it easy

Speaking of making things easy, this is another key to habit formation, if you have to overcome too many ==hurdles to start the activity==, it won't get done. Think of trying to start an exercise program but the gym is an hour's drive away and your workout clothes are in the bottom of the laundry hamper, vs an at home workout or a park in your neighborhood and clean workout clothes ready to go. Similarly with screencast video learning, there's a few things you can do to make it easier to get each learning session started.

==Leave your editor open== with the course folder you've started. On a Mac, next time your computer boots up, the editor will be open waiting for you. For Windows users, remembering open apps and files is not a native feature, although you could check out some [suggestions](https://www.pcworld.com/article/410688/how-to-have-windows-re-open-active-windows-and-programs-on-reboot.html).

==Leave the course url open in a browser tab==, and enable remember previously open tabs in your browser so the videos will always be there waiting for you. An alternative if you don't want to always have the tab open is to bookmark the course url, then [index your browser bookmarks](https://danielabaron.me/blog/how-to-access-chrome-bookmarks-via-keyboard) to load it quickly via keyboard.

### Habit Stacking

This is a technique where you ==identify a current habit you already do each day, and then "stack" a new habit on top.== The general form of this is:

"After I `CURRENT_HABIT`, I will `NEW_HABIT`."

For example, someone trying to establish a gratitude habit might say: "After I sit down to dinner, I will say one thing I'm grateful for that happened today".

In this case, `NEW_HABIT` will be learning from screencasts. For me, I identified `CURRENT_HABIT` as making coffee first thing in the morning, which I've been doing for over 20 years! This leads to: =="After I make coffee each morning, I will set down my mug at my desk, and have coffee while doing some screencast learning".==

==This works because it's tying a desired new behaviour== (learning from video courses) to something you already do every day, such as making coffee. Think about a typical day in your schedule, identify `CURRENT_HABIT`, then stack it with the learning habit.

## Conclusion

This post has covered a number of active learning techniques to get the most out of video screencast courses, and why that's more beneficial than passive learning. It's also covered some advice to make learning a habit. If you only get one thing out of this, it's to write down what you're learning. Writing helps you remember what you've learned, provides a medium for faster recall than video, and is a useful reference even if you no longer have access to the course videos.

# References
- [maximize learning from screencasts article](https://danielabaron.me/blog/learning-from-screencasts/?ref=writesoftwarewell.com)
