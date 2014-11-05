On Readme Driven Development – a transcript of my Devfest 2014 talk
===============
*I had the honor of opening one of Devfest's tracks and talk about documentation writing - not a developer darling per se, still the place was packed. The initial title for the talk was '(kick-ass) Documentation Driven Development', although really I talked about Readme Driven Development. Why was it important to make this distinction? A Readme does not equal documentation. A good README explains why the accompanying program is useful, shows some examples of how to use it, and points the user towards more detailed documentation. Readme’s have been with us for a long time, and ex-GitHub Tom Preston-Werner coined the term RDD August 2010. My interest for writing technical documentation developed from my need to connect and explain programming concepts. But let’s define the scope of RDD, or what I think the scope is.* 

We often only start writing documentation for our apps after we have developed them. Instead, when you start with writing down the requirements (BDD), intended usage and example use cases, documentation writing becomes a vital part in the decision making process - making damn sure we don't feature-freak. Plus: it won't be such a painful last-minute thing anymore. Which in turn translates to smarter software development, less killing darlings and more time for the important stuff in life: coding ALL the rubies (yes, I am one of those people).

#### Nobody puts baby in a corner
In building for instance a great API, the design and development processes demand equal attention. The problem is that popular development approaches don’t emphasize the design process. Readme or Documentation Driven Development brings back the design-driven way of thinking. 

Talking of RDD or DDD I often hear the same question: "what about BDD as Behaviour or Business Driven Development (isn't that writing enough)?". I promised the Devfest organizers I would not get into Ruby (that much) so to refrain from Ruby flavoured code slides: I can see how describing scenario’s in Cucumber that read like a storyboard of features and can be understood by all stakeholders of a project (not only the techy ones), would fit in a Documentation or Readme driven methodology. But not replace it. 

#### tl;dr
RDD should be considered a light version of DDD. By restricting your design documentation to a single file that is intended to be read as an introduction to your software, RDD keeps you safe from lengthy or overprecise specifications. You don’t want people to go through your entire documentation before they can even think about using your software. 

Starting with a Readme for your next project helps you to be crystal clear with all stakeholders including oneself about the intentions and to collect feedback before writing a single line of code. A bit similar to code sketching, and a great start for a TDD / BDD approach, detecting complexity early on. 

**pro tip:** Related to that, writing issues as documentation and implement on agreement will help you get your intentions right. It will save you time issuing and getting your pull request merged. And, as you’ve already written your issue down in such detail, if you can’t implement it – someone else might, with your instructions!

#### Until you've written about your software, you have no idea what you’re doing
If there’s one thing I want you to take away from this talk it is that when starting a new project write your Readme first. Really. Before you even start formatting your page, before you run your scaffolds. Before anything else. Don’t get me wrong, nothing needs to be documented in crazy detail, but there’s a middle way between that and using agile as the magic cover-up word for writing software fast and sloppy, for the sake of speed alone. Projects with short, badly written, or entirely missing documentation, are useless. 

*"A perfect implementation of the wrong specification is worthless. A beautifully crafted library with no documentation is also damn near worthless."*
Tom Preston Werner

If your software solves the wrong problem or nobody can figure out how to use it, there's something very bad going on. 

### benefits of RDD
1. RDD enables you to think through the project without the overhead of having to change code every time you change your mind about how your code should be structured or what features should be implemented. Remember that feeling when you first started writing automated code tests and realized that you caught all kinds of errors that would have otherwise snuck into your code base? That's kind of what it feels like.

2. As a byproduct of writing a Readme you'll have a very nice piece of reference for what in time will become your documentation sitting right in front of you.

**pro tip:** keep your readme open at all times as one of the few files, so you’ll be constantly reminded of its existance and don’t forget to put in library or gem specifications if you find out that only a certain version works for your purpose, for instance.  

3.You'll find that it's much easier to write this document at the beginning of the project when your excitement and motivation are at their highest. Retroactively writing a Readme is an absolute drag.

4. If you're working with a team of developers, a Readme means that everyone has access to information before you've completed the project. They can confidently start work on projects that will interface with your code. 

**free bonus feature:** The documentation gives the client team something to work from before the server team has even implemented the documented endpoints. That means: no teams just sitting there being pretty. 

**free bonus feature 2:** It helps shorten the onboarding process for newcomers to your team and even newcomers to programming (when they have an idea of what gem is used for tackling which problem and where to find more information). 

5. It's a lot simpler to have a discussion based on something written down. Writing can be amended in collaboration, misunderstandings on a language level can destroy a project. 

6. It has the ability to give a high level view of your code with the goal to gather insight and recommendations from your consumers early and all throughout the design process.

7. It’s markdown. You know markdown. You can do markdown.

8. Github showcases the Readme on the main project page and with that strongly encourages you to write one. A Readme summarizes the project as they are attached alongside the versioned code. They provide contex.

9. It’s totally Open Source compatible. A good Readme indicates where and how people could report bugs or suggestions and how people could contribute to the project.  

**Pro tip 1:** Looking to add RDD / DDD to your existing project? It can be as simple as just adding a step to your BDD or TDD:

- Write or update your documentation
- Write a failing test according to that documentation (red)
- Write code to pass the failing test (green)
- Refactor

**Pro tip 2:** When writing or updating documentation is a required first step of your development process, you ensure your documentation is always consistent with your code.

**Pro tip 3:** Treat your documentation like you treat your (peers) code: documentation changes should also be included in the code reviews.

### Pitfalls of RDD

… because of course there are some and it’s really a matter of shaping RDD to your team’s needs. As most software methodologies DDD or RDD is just an over-generalization of a good idea. Use it in a way that makes sense for your team. 

- One of the mistakes easily made, is have the readme present what you are aiming for, rather than what the code actually does. A Readme is not the place to display your aspirations of becoming an author of science-fiction novels.

- a Readme does not substitute proper documentation.

For those people counting: there are more plusses than minuses, which totally supports the RDD methodology. Who would have thought?

### What makes a good Readme?
**airbnb for cats**
Describe what problem your project solves. Use strong or emphasised text to give a short description of what the software does, such as “use bitcoin in your Rails app”. Provide code examples detailing how to use your library. Document the installation process. 

**formatting is key**
Your readers will most likely view your Readme in a browser, get familiar with markdown's formatting. Link to project pages for related libraries you mention. Link to Wikipedia or other websites for definitions for words a reader may not be familiar with. 

**rrrrr code samples**
Developers love to see code samples and a few lines of syntax highlighted source are worth a thousand words. Use them for good: what libraries does your code interface with, how can your software be used alongside popular gems?

**community and licensing details**
Add information about the maintainers, licensing, links to community platforms like IRC or a Google Group and make sure to mention where people could list issues and suggestions and how they could contribute to your project. 

**air your dirty laundry in public**
Be aware that sometimes the reason someone is visiting your project’s page is that they have a problem. If you know about persistent issues, call that out in a section of its own and provide a solution or workaround. 

**OMG badges**
Codeclimate and Travis badges are all the rage! Just remember that they reflect on your project. A passing build with high quality code attracts developers to your library, while a failing master build will likely drive them away.

#### Readmore:
[http://tom.preston-werner.com/2010/08/23/readme-driven-development.html](http://tom.preston-werner.com/2010/08/23/readme-driven-development.html ) 
[http://collectiveidea.com/blog/archives/2014/04/21/on-documentation-driven-development](http://collectiveidea.com/blog/archives/2014/04/21/on-documentation-driven-development)
