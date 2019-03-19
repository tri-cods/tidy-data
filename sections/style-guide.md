# Style Guide

## Structure

Three structural elements are important for an effective DRI session: scoping, scaffolding, and purpose. Scoping is the art of choosing what—and especially what *not*—to include in a session. Scaffolding is the process of building later skill development on prior skill development. Purpose provides an answer to the participant who asks, "Why should I care about this?"

### Scope

When leading a session, it's tempting to want to comprehensively cover all important aspects of a tool, method, or skill. After all, this is an area you're expert in, and every topic left out of the session is likely something you use frequently and find indispensable. However, in most cases, students will come away having learned more if a lesson is carefully scoped—that is, covering only carefully selected material. This allows the session to account for unexpected delays, which occur approximately 100% of the time. It also allows for review, question and answer, unstructured practice, and challenges. These approaches don't need to be present in every lesson, but they can often improve outcomes for students.

People tend to underestimate how long tasks will take in practice and to overestimate how much material it's feasible to cover in a lesson. There's a name for this phenomenon: the [planning fallacy](https://en.wikipedia.org/wiki/Planning_fallacy). For this reason, you should err on the side of planning to cover less material in a session. To make this easier, build in some challenges or unstructured activities to your lesson, ones that can be omitted or shortened if you're running out of time. Often, you'll find you don't have time for these, but including them can increase your confidence in a well-scoped lesson.

### Scaffolding

Scaffolding is the art of structuring lessons so that students begin with more fundamental concepts or tasks and work towards increasingly difficult learning goals. With technical sessions, this often means finding ways to introduce concepts in isolation, so that students can come to terms with them without distraction from additional new or unfamiliar concepts. New methods and new vocabulary should be introduced explicitly rather than implicitly, and students should have time to integrate new knowledge before moving on to new information.

When thinking about the structure of your lesson, consider what jargon or terms of art will be essential for students to know and plan where and how you'll introduce those words or concepts. Don't use jargon terms before introducing them.

When planning a lesson, try to make your tooling and setup look as close to your students' as possible. For example, if you have shell modifications, disable them before teaching. If that's not possible, explain any differences students might be seeing. Remember that students are trying to match patterns in an unfamiliar and cognitively taxing environment and may not know what differences are significant and which are merely cosmetic.

Try to incorporate review into your lesson organically. If a concept won't be used repeatedly throughout your lesson, you might consider leaving it out altogether. Challenges or unstructured practice can also provide opportunities for review.

### Purpose

The most common question in DRI sessions is, "How does this relate to my research?" Researchers are more motivated to learn when they know that a tool or method can be used directly to advance their own goals. One way to help researchers to understand the purpose of a tool or method is to structure the lesson around a "deliverable"—a website, a piece of persuasive writing, a cleaned data set, an application, a visualization, or any other useful product. Even if the result does not relate directly to a participant's research, it's often easier to extrapolate usefulness from a concrete product than from a series of loosely coupled actions or skills.

Working toward creating a specific artifact in your lesson can also help with scaffolding and scoping. If you know exactly what students will need to learn to create, for example, a course website, that makes it easier to leave out concepts that don't directly relate to that goal. It also suggests discrete steps and challenges that students must engage before completing the deliverable, often leading to a more intuitive lesson structure.

## Markdown Guidelines

### On Markdown

Markdown is a plain text markup format that is easy to read for both computers and humans. This is in contrast to, for example, HTML, which in its unrendered form is not enjoyable for humans to read. Compare the same document in HTML and markdown:

HTML:

```html
<h1>My Book Report</h1>
  <p><i>Persuasion</i> is an <strong>excellent</strong> book that I highly recommend for three reasons:</p>
  <ul>
	<li>It's a comeback story.</li>
	<li>It has a catchy title.</li>
	<li>It's written by Jane Austen.</li>
  </ul>
  <p>You can buy the book <a href="http://www.bookmonopoly.com/persuasion">here.</a></p>
```

Markdown:

```markdown
# My Book Report

*Persuasion* is an **excellent** book that I highly recommend for three reasons:

- It's a comeback story.
- It has a catchy title.
- It's written by Jane Austen.

You can buy the book [here](http://www.bookmonopoly.com/persuasion).
```

When rendered by a browser, both of these documents look identical. However, the markdown document is considerably easier to read in its source form. While HTML is optimized to be readable by the computer, markdown is more balanced between the human and the machine.

### Why Use Markdown?

The Fellows use markdown for tutorials for a number of reasons:

- It's exportable to other formats, such as HTML, PDF, and GitBook.
- It can be kept under version control—with Git, for example.
- It's rendered automatically on GitHub.
- It can be read locally with a text editor.
- As plain text, it's maintainable.
- It's easy to embed code and images.
- It plays well with the tools we teach at the DRI.

Many of markdown's advantages come from the fact that it's plain text. Tools that work well with code, such as version control, editors, and grep, also work well with markdown.

### Markdown Formatting

Most formatting guidelines here are designed to make markdown source files more readable. Others are designed to preserve semantics, which allow markdown to be rendered the same in different contexts.

1. Seperate paragraphs with a blank line.
2. Place blank lines between elements whenever possible. For example, put a blank line between a heading and a paragraph, and between a paragraph and an image link.
3. Use headings consistently, and use them only to denote new sections. For example, do not use headings for emphasis.
4. Use other markdown elements for their intended purpose. Use lists for lists and emphasis for emphasis. For example, do not use emphasis in place of a heading.
5. Unless a raw URL is part of the tutorial, don't leave raw URLs in your document. Incorporate the link into the flow of your prose.
6. If code segments are short, indicate them by indenting. If they're longer, use the ````` syntax.
7. When introducing new commands or code, put them on a new line so they stand out from the rest of the text.
8. When including images, don't leave the alt text segment `[]` blank. Fill it in with information that would be useful if the image could not be seen or rendered.

## Attribution

## Free and Open Source Code

In general, it's not necessary to provide in-line citations in the materials for a technical workshop unless you're using someone else's exact prose or you're replicating a significant, non-trivial section of code. For example, code segments found on Stack Overflow do not need to be cited unless you think it's pedagogically helpful. However, if you build your session around replicating a significant portion of a particular application, you must consider the license under which that software is released and consider providing attribution, even if attribution is not required under the terms of the license. In general, free and open source code licenses do not require attribution, but using a large portion of the code may require replicating the license. Check a summary of the terms of the license (or the license itself, if you're feeling adventurous) if you decide to replicate a significant portion of an open-source project in your session.

## Citing Fellows and Other Academics


