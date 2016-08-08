# Resources

> If you hire average developers without an adequate supply of senior developers to monitor commits and mentor them, you are slowing down the productivity of your whole development team. I'm not just talking about a short-term effect that lasts the duration of the developer's employment. I'm talking about lasting effects: technical debt that will still be causing your team pain potentially long after the average developers move on.
> 
> The trouble is, the average developer may close tickets quickly. Managers sometimes confuse them for 10x developers because they blindly charge forward and get things done: but they leave serious damage in their wake.

* [**Dev Freecasts**](http://devfreecasts.org/)
* [**Structure 101**](http://structure101.com/)
* [List of programming screencast series](http://devblog.avdi.org/2013/06/21/a-list-of-programming-screencast-series/)
* [VisuAlgo](http://www.comp.nus.edu.sg/~stevenha/visualization/index.html)
* [Quickly learn X programming language](http://learnxinyminutes.com/)
* [Beautiful Open Source projects](http://beautifulopen.com/)
* [Awesomeness Awesomeness](https://github.com/bayandin/awesome-awesomeness)
* Architect for change. Make change less expensive. Able to evolve overtime.
* Software always becomes iterative. Architecture also becomes iterative.
* Architecture is a snapshot of a process.
* Architecture is coupled to process (esp. continuous delivery).
* [Sorting - Visualized](http://sorting.at/)
* [What is Software Design?](http://www.developerdotstar.com/mag/articles/reeves_design.html)
* [Imperative vs Declarative](http://latentflip.com/imperative-vs-declarative/)
* [Your syntax highlighter is wrong](https://medium.com/web-dev/6f83add748c9)
* [Technical debt 101](https://medium.com/@joaomilho/festina-lente-e29070811b84)
* [The big rewrite](http://chadfowler.com/blog/2006/12/27/the-big-rewrite/)
* [Quality Assurance tools](https://sifterapp.com/academy/resources/tools/)
* [Thoughtbot Guides](https://github.com/thoughtbot/guides)
* [Producing open source software](http://producingoss.com/en/producingoss.html)
* [Deep???](http://engineering.flipboard.com/2015/05/scaling-convnets/)
* [A Little Structure](http://blog.cleancoder.com/uncle-bob/2015/09/23/ALittleStructure.html)

## Agile

* [Agile and Cybernetics](http://blog.laessig.com/2013/09/14/agile-and-cybernetics/)

## Abstraction

* Visual/Spatial reasoning - Squint test, boxes and arrows
* Linguistic reasoning - Rubber duck on your desk
* Sequence diagram - Find out which class is bossy
* Metaphor - Body syntonic reasoning, East-oriented code (Tell, don't ask), Code smells
* Feature envy, refused bequest, primitive obsession, duplicated code, long method, large class, too many parameters.

Always look for first-try, first-reaction bias.

See [Cognitive shortcuts: Models, Visualization, Metaphors, and other lies](http://www.youtube.com/watch?v=__qEkyJipX0)


## Architect (Feasibility)

1. **Leadership and communication** - Effective communication. Collaboration. Clarity. Listen to business and translate.
2. **Technical knowledge** - as a Ruby architect, everything you see is a Ruby solution :( Technical breadth is important.
3. **Business domain knowledge** - Trend in HR.
4. **Methodology and strategy** - Once you know, how do you get there?

Techniques for change:

1. **Reduce dependencies** - De-couple components. Faster to deploy due to decoupling. Components can evolve independently. Use messaging, service bus, adapter or even architectural patterns.
2. **Leverage standards** - allow to integrate easier.
3. **Create product-agnostic architectures** - No vendor lock-in. Surround it with message bus, adapters, etc. Anti-corruption layer in DDD.
4. **Create domain-specific architectures** - Don't make generic or too broad architecture. Focus on domain-specific. Limit the scope. Follow business direction and industry trends. Business requirements -> Business goals -> Business direction + Industry trends = Domain-specific architecture.


## From CI to CD

* **Continuous Integration** - Fast, automated feedback on the correctness of your application every time there is a change to code.
* **Continuous Deployment**
* **Continuous Delivery** - Fast, automated feedback on the production readiness of your application every time there is a change - to code, infrastructure, or configuration

Get your Continuous Delivery early and often. Do it first!

Releases occur according to business needs, not operational constraints.

1. Commit stage - Compile, unit test, build.
2. Acceptance stage - Puppet to configured environment. Deploy and smoke test. Again acceptance test one final time?

## Metrics

Don't let people "gain metric" through over-reaction.

* Kiviat metric
* Cyclomatic complexity
* Size and complexity pyramid
* Vuze - Quality pyramid
* Efferent coupling
* Afferent coupling

## API Design

* [API design principles](http://qt-project.org/wiki/API-Design-Principles)

## Videos

* [Three flaws in software design - Code Simplicity](https://www.youtube.com/watch?v=JOAq3YN45YE)