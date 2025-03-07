## Rust Nation UK 2025 Recap
### **Today’s Issue:** Become a Better Rust Engineer, Writing a Rust SQL Parser in One Week, and Don’t Run Any Cargo Commands on Untrusted Projects

![Ferris the crab mascot - Image courtesy of tweedegolf](https://substackcdn.com/image/fetch/w_1456,c_limit,f_webp,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F57096f41-1b75-4618-8e90-60467d00a5ab_1200x628.jpeg)

Hello Rustaceans! 🦀 

Welcome to another edition of *Rust Bytes*.

In this issue, we will look at the recap of Rust Nation UK 2025 conference, challenge you to implement a solution for finding pairs summing to a target, spotlight an amazing Rust project, and share some incredible links of the week.

Here’s issue 57 for you!

---

### A Message for You 🎂
This Wednesday, March 12, marks the 36th anniversary of the World Wide Web (WWW). We've gone from dial-up to doomscrolling, and we wouldn't have it any other way. 

Huge thanks to Tim Berners-Lee for giving us something to do while we avoid eye contact with strangers.

Now onto our main discussion.

---

## THE MAIN THING
### Rust Nation UK 2025 Recap

Last week, the recordings from the Rust Nation UK 2025 conference were made public. This year’s conference spanned two days and took place at The Brewery in the UK.

The conference featured 18 talks on various Rust-related topics, delivered by an impressive lineup of speakers.

If, like me, you didn’t attend the conference and were too lazy busy to watch the recordings of the talks, here’s a recap of what you missed.

Celina G. Val from AWS kicked off the event with her talk, Ensuring Rust Safety: Strategies for Managing Unsafe Rust. She explained the concepts of safe and unsafe Rust, discussing strategies for designing, testing, and verifying unsafe code. 

Celina explained how to use unsafe traits to create safe generic abstractions. She also covered techniques for testing unsafe code and introduced the Mid-level Intermediate Representation (MIRI), highlighting its role in detecting Rust-specific memory violations. She concluded her presentation by addressing methods for proving code safety.

Kailan Blanks from Fastly gave a talk titled Rust at the Edge. He introduced how Rust, combined with WebAssembly, can be used to create unique customer experiences without compromising performance. It was an excellent talk.

Greg Johnston, the creator of Leptos, gave a lightning talk on using Rust to build interactive web applications. He introduced various Rust web frameworks, discussed their current limitations, and shared future projections for Rust in web development.

His talk was so compelling that it nearly convinced me to rewrite our company project in Rust. He concluded by envisioning a bright future for interactive web applications.

Adam Harvey’s talk, Crate Security in 2025, shed light on the current state of crate security on crates.io. Last year, we witnessed significant security breaches in open-source projects, and Rust crates were no exception—name squatting being one example. Adam discussed ongoing efforts to enhance crate security and highlighted tools currently available to help developers understand and evaluate dependencies for security.

Another fascinating talk was Techniques Learned from Five Years of Finding a Way for Rust in Python by David Hewitt. David shared insights gained while contributing to PyO3, a project focused on integrating Rust with Python. He concluded by discussing the challenges he encountered and potential future solutions.

Mark Russinovich delivered the closing talk of the conference, titled How Microsoft Is Getting Rusty. His presentation was excellent in demonstrating how big tech companies are benefiting from Rust. 

He discussed Microsoft’s efforts to port various projects to Rust, including Rust in Office and Rust in Azure. Additionally, he highlighted the strengths and challenges of Rust, addressing some of its rough edges, such as C-to-Rust interoperability, tooling, crate stability, and more.

If their was one thing that kept popping up in the presenters' talks at the conference was WASM. Could this be the year WebAssembly takes center stage? It’s the question on everyone’s mind.

Want to binge-watch the Rust Nation UK 2025 conference talks? [Check out the recordings here](https://www.youtube.com/watch?v=fmtykJT1acM&list=PL1AoGvxomykSSFFL4Qav3wKzL-dsi9I5L&index=1)! 

---

## RUST CHALLENGE 🦀
In the previous issue, we challenged you to implement a solution for the valid parentheses problem. 

Kudos to [Gopal](https://play.rust-lang.org/?version=stable&mode=debug&edition=2021&gist=55e70d0413a5ab5b871ece914e564b4e), and others who took on the challenge.

Let's move on to this weeks challenge.

### Find Pairs Summing to Target
Given a vector of integers and a target sum, return all unique pairs of indices whose corresponding elements add up to the target. 

The same number cannot be used twice in a pair, and the pairs should be returned in ascending order of the first index.

**Example:**
```rust
assert_eq!(find_pairs(vec![2, 7, 11, 15], 9), vec![(0, 1)]);
assert_eq!(find_pairs(vec![3, 2, 4, 1, 5], 7), vec![(0, 2), (1, 4)]);
assert_eq!(find_pairs(vec![], 5), vec![])
```

Test your solution on [Rust Playground](https://play.rust-lang.org/?version=stable&mode=debug&edition=2021&gist=3564760b109f4cde82b542a8186c355f). Once completed, please share your code on [Twitter](https://x.com/intent/user?screen_name=rustaceans_rs), or reply to this email.

---

## PROJECT SPOTLIGHT 💡 
### Gleam

![Gleam Mascot, Lucy](https://github.com/gleam-lang/gleam/raw/main/images/lucy.png)

Gleam is a modern, friendly programming language written in Rust, designed to make building type-safe, scalable systems easier.

It brings the power of Erlang's battle-tested virtual machine (BEAM) and a functional programming style to developers, all wrapped in an approachable, expressive syntax.

By combining the reliability and concurrency features of the Erlang runtime with a clean, modern design, Gleam is positioned as a great tool for building reliable, scalable systems that are easy to maintain and extend.

In essence, Gleam solves the challenge of building dependable, high-performance systems without sacrificing developer happiness or productivity.

Here’s a quick look at what makes Gleam stand out:

- **Highly Concurrent Systems.** Gleam allows developers to spawn thousands or even millions of concurrent tasks without sacrificing performance. It’s designed for modern multi-core processors and can handle loads with ease.
- **Type-Safety and Clear Errors.** Gleam’s type system ensures that many errors are caught early, reducing the number of bugs that can make their way into production.
- **Erlang’s Scalability.** The BEAM runtime brings concurrency (e.g., spawning 200,000 tasks with task.async) and fault tolerance, backed by a concurrent garbage collector that never halts your app.
- **Developer-Friendly Tools.** Gleam comes with built-in tools like a compiler, formatter, build tool, editor integrations, and a package manager.

Gleam’s modern syntax, developer-friendly tools, and growing ecosystem offers a unique solution for building reliable and high-performance systems. 

Whether you're building server-side applications or client-side JavaScript, Gleam provides a solid foundation to ensure your code is safe, scalable, and easy to maintain.

Check out the project on [GitHub](https://github.com/gleam-lang/gleam).

---

## AWESOME LINKS OF THE WEEK 🔗

1. [Rustup v1.28.0](https://blog.rust-lang.org/2025/03/02/Rustup-1.28.0.html) is now available with huge improvements.
2. Wojciech Daniło released [eval-macro](https://github.com/wdanilo/eval-macro), a crate that enables you write write inline Rust code that gets evaluated at compile time to generate Rust code.
3. Sergey 'Shnatsel' Davidoff cautioned against [running Cargo commands on untrusted projects](https://shnatsel.medium.com/do-not-run-any-cargo-commands-on-untrusted-projects-4c31c89a78d6), explaining how doing so might expose you to security risks.
4. The innovative minds at Metacraft Labs released [CodeTracer](https://github.com/metacraft-labs/codetracer) – A new time-traveling debugger implemented in Nim and Rust.
5. Vitaly Bragilevsky from JetBrains appeared on the [The Rustacean Station Podcast](https://rustacean-station.org/episode/vitaly-bragilevsky-rustrover/), and talked about RustRover. [podcast]
6. Guillaume Endignoux authored an interesting article on [The power of interning: making a time series database 2000x smaller in Rust](https://gendignoux.com/blog/2025/03/03/rust-interning-2000x.html).
7. The talented Rustaceans at Clockwork Labs released [SpacetimeDB](https://spacetimedb.com/blog/introducing-spacetimedb-1-0), a relational database system that lets you upload your application logic directly into the database by way of fancy stored procedures called "modules.
8. The LakeSail Team wrote about [Writing a Rust SQL Parser in One Week](https://lakesail.com/blog/sql-parser-in-one-week/).
9. The EuroRust 2025 conference has been announced, and the [call for papers is now open](https://www.papercall.io/eurorust-2025) for prospective speakers. This year's event will be held at the Cité des Sciences et de l'Industrie in Paris on October 9th and 10th. Hurry before the deadline (May 15).
10. Kane Rogers-Wong has a cool  tutorial on [Shipping a Game with Vulkan and Rust in 100 Days](https://www.youtube.com/watch?v=EB-ARcAnZY4). [video]

---

## [CodeCrafters: Become a Better Rust Engineer](https://app.codecrafters.io/join?via=rust-bytes)
CodeCrafters created amazing [Rust courses](https://app.codecrafters.io/join?via=rust-bytes) that push your skills beyond the basics.

You’ll have fun building real-world projects from scratch, including Git, Docker, Redis, SQLite, Grep, BitTorrent, HTTP Server, an Interpreter, and DNS.

The courses are self-paced, so you can learn at your own speed. 

If you’re itching to level up your Rust skills, these courses are perfect for you. 

Here’s what makes CodeCrafters stand out:

- Learn by building projects that challenge you beyond just implementing CRUD features.
- Strengthen your fundamentals by working on awesome low-level projects.
- Get really good at reading and writing idiomatic Rust code.
- Join a community of talented engineers from MAANG companies and learn best practices from the pros.
- Plus, take part in monthly contests for a chance to win exciting prizes.

Don't take our word for it. [See what others have to say](https://app.codecrafters.io/join?via=rust-bytes). [affiliate](#)

---

## SUPPORT RUST BYTES 👋 
You're *Rust Bytes* biggest fans, and we love to see it.

Here’s how you can help spread the word:

- ❤️ Recommend *Rust Bytes* to your friends.
- 🤳 Connect with us on our socials: [X](#), [Rustaceans Publication](#).
- 📨 Email us at rustaceanseditors@gmail.com for sponsorship, feedback or ideas.
- ☕️ Buy us coffee to support our editors.

I moved to a new place this week and am starting to adjust to the environment and people. Wishing you a productive week ahead.

That's all for now, Rustaceans. 

*John & Elley.*

