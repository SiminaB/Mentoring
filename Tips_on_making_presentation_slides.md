Below is a non-exhaustive list of recommendation on making presentation slides, focusing on 
presenting biostatistics or bioinformatics projects. There are many amazing resources out there. I internalized much
of the advice given to me by many awesome official and unofficial mentors (Jeff Leek, Giovanni
Parmigiani, Josh Sampson, Tom Louis, @theeffortreport with Roger Peng and Elizabeth Matsui, and
@NSSDeviations with Hilary Parker and Roger Peng, to list a few) and the goal here is to
pass some of it along to my students rather than to come up with a comprehensive list.

My students tend to be from Biostatistics and Bioinformatics, so their projects involve both
scientific and statistical or computational aspects. This presents additional challenges,
given both the interdisciplinary nature of the work and the potential audiences.

#### Major guiding principles:

* Build the entire presentation by starting from the general scientific question you are trying 
to answer. Why are you studying this problem? Why is it interesting? Move from there into
the more technical aspects, but do so in a logical manner, still focusing on the
overall framework - Are you testing a specific hypothesis? Are you providing tools for exploratory
data analysis?
* Know your audience: If statistical, you may need to introduce biology terms like the different kinds of mutations
- e.g. missense, nonsense. If biomedical, do not assume knowledge of statistics past t-test or programming knowledge.
* You should go into technical details only after you introduce the big picture/framework. For example,
details like "We use grouped LASSO with 10-fold crossvalidation" or "We used the following
10 packages in R" do not need to be introduced up front. Methods and tools are very important but they should
not be introduced without making it clear why you are doing so. Otherwise, you risk confusing people or making them
think that you are confusing an approach with the tool used to implement it (e.g. "we use the coxph command" instead
of "we fit a Cox proportional hazard model")
* Always assume your audience is intelligent and educated, but don't be too worried about presentating things that
are too basic or "known by everyone," especially in the first few slides (also see _Know your audience_ above - folks
will know much more about their own fields than about others'.) They may either make people feel good that they
understand something or actually help them learn something new.
* Practice and iterate! Try not to take criticism personally during either the practice presentations (you want to improve!)
or during the actual presentation, although this can be hard.
* Think about things you really liked in some presentations and try to emulate them and also about things you really didn't like
and try not to be that presenter.
* Less can be more. Simplify, simplify, simplify! See below.

#### Less is often more:

During the iteration process, I try to always think about how to simplify everything and reduce the text. Maybe I'll
come up with a simpler table with fewer columns or even replace a few bullet points with a diagram. Some specific advice on this:
* Don't be the person who says: "I know you can't really read this text, but it says..." If it's not readable it's too small.
If it's too small it's probably because you're trying to cram too much in. Tables that are OK for reports/papers are usually
way too large to fit on slides or present in a way that keeps the audience engaged.
* Similarly, don't have a 4x4 grid of plots but say "You only really need to focus on these 2 plots." Only have those 2 plots then.
If you find that you're not able to get into a specific plot due to time constraints or relevants, then remove it.
Unless the plots are very closely related, it may be better to have them on separate slides.
* The outline slide debate: Some people feel very strongly that you should have an outline slide, others that you should not.
I fall into the second camp, though I'm not totally dogmatic about this. I prefer to have a slide introducing the project and the 
overall goals, then go right into the presentation. Especially for a 15-20 minute presentation, you probably don't want/need
to spend time on an outline slide where you say things like "I will start by introducing the problem," "I will check the results
via simulations," and definitely not "Finally, I will conclude with the conclusions."
* Try not to prepare more than one slide per minute (videos/demos are extra.) Be respectful of your audience's time and try to 
do a good job conveying the gist of your work in the assigned time (ending a couple of minutes is OK and way better than
ending 15 minutes late!)

#### Specific advice for individual slides:

* Give slides meaningful titles that are as self-contained as possible.
* Don't include large blocks of text and try not to have more than 3-4 bullet points. 
* Try not to have many/any equations for a biomedical or mixed audience. I do usually have some when presenting
for a statistical audience.
* Label plots clearly and present them by first saying what the plot is assessing/presenting. This should 
also be in the slide/plot title. You not need a plot title if the slide title is specific enough. In fact, this 
will help you save on space and allow you to make things bigger/more readable. 
* If using R to make the plots, change the x and y labels from the default variable names in R so that they're more easily understandable. 
For example, you don't want to distract the audience and spend extra time saying "Time.patient represents the overall survival time in weeks" - 
instead change that label to read "Overall survival time (in weeks)."
* Use large fonts and large labels on figures/tables (will probably need to increase font from defaults in R).
* Try to use high-resolution figures. Projectors often make things fuzzier!
* Try to be color-blind friendly by not using the red/green scheme. Colors can get messed up when projecting anyway, or
it may be better to use them sparingly and not have more than 3-4 different colors per plot. This depends a lot on your
application and may not always be possible, but again, think about where you can simplify!
* Do not show a large number of significant digits. It is almost never necessary to show more than 2. The difference
between p = 1.9 x 10^-19 and p = 1.942529058202 x 10^-19 is very small and the latter is very distacting.

#### You gotta start somewhere!

While you should consider the advice above, make sure it doesn't give you writer's block/analysis paralysis. I often
start out with a rough version by cutting/pasting from manuscripts/notes/R output, then think about how to focus it,
simplify it, and prettify it.

#### Practice and iterate many times!

This was already stated before, but cannot be overstated. It depends on the stage of your career and the type of talk as well,
of course (update to small group, final presentation for your degree, job interview etc), but in general it is very important.
Only by practicing can you that you are belaboring some things or that certain plots/tables don't fit in in their current form.
Make sure you give yourself enough lead time to be able to do this.




