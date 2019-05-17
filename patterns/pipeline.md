# Pipeline Pattern

Keywords: collection, pipeline, filter, map, reduce

- A good introductions: <https://martinfowler.com/articles/collection-pipeline/>
  - Rich of examples in different languages
  - Focused on elementary things: filter, map, reduce, etc.
  - Talks about comprehension (a language feature)
- Pipeline Pattern in action (PHP): <https://matthewdaly.co.uk/blog/2018/10/05/understanding-the-pipeline-pattern/>
- Pipeline utilities in python:
  - A great list: <https://github.com/pditommaso/awesome-pipeline> (already forked)
    - Many features cluster integration. Some prefers clouds (AWS, etc.), 
      few supports SGE/Slurm, even fewer supports both SGE and Slurm.
    - Interesting for me: [Pyflow], [sciluigi], [Ruffus], [martian], and [clusterjob].
      - [Pyflow] has a good website. 
      - [Ruffus] is simple.
      - [sciluigi] and [martian] are serious project, things I should really try.
      - [clusterjob] is useful for submitting cluster jobs.

[Pyflow]: http://illumina.github.io/pyflow/
[sciluigi]: https://github.com/pharmbio/sciluigi
[Ruffus]: http://www.ruffus.org.uk/
[martian]: https://martian-lang.org/
[clusterjob]: http://clusterjob.org/
