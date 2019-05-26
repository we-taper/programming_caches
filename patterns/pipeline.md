# Pipeline Pattern

Keywords: collection, pipeline, filter, map, reduce

- A good introduction: <https://martinfowler.com/articles/collection-pipeline/>
  - Rich of examples in different languages
  - Focused on elementary things: filter, map, reduce, etc.
  - Talks about comprehension (a language feature)
- Pipeline Pattern in action (PHP): <https://matthewdaly.co.uk/blog/2018/10/05/understanding-the-pipeline-pattern/>
- Pipeline utilities in python:
  - A great list: <https://github.com/pditommaso/awesome-pipeline> (already forked)
    - Many features cluster integration. Some prefer clouds (AWS, etc.), 
      few support SGE/Slurm, even fewer support both SGE and Slurm.
    - Interesting for me: [Pyflow], [sciluigi], [Ruffus], [martian], and [clusterjob].
      - [Pyflow] has a good website. 
      - [Ruffus] is simple.
      - [sciluigi] and [martian] are serious projects, things I should really try.
      - [clusterjob] is useful for submitting cluster jobs.

Notes:

*message passed*: 

The message passed between different steps of a pipeline will change its structure almost in all steps.
I feel this makes it hard to debug in complex situations. I thought I need something like a nested namedtuples (in case of python) so that I could easily use type hints to document and maybe debug a code. 

Some potential solutions:
- <https://github.com/brennv/namedtupled> : creates namedtuples from json files. But it does not support type hinting.
- Google's Protobuf: creates a class from a specification. It also does not support type hinting (maybe it [will](gpth) support in the future). The good things about protobuf are that it checks its contents' type and should run very fast.
- [JSON Schema](jsonschema) also looks good, although it still comes without default type hinting.
- Python 3.**7** introduces [dataclasses](https://docs.python.org/3/library/dataclasses.html).

[Pyflow]: http://illumina.github.io/pyflow/
[sciluigi]: https://github.com/pharmbio/sciluigi
[Ruffus]: http://www.ruffus.org.uk/
[martian]: https://martian-lang.org/
[clusterjob]: http://clusterjob.org/
[gpth]: https://github.com/protocolbuffers/protobuf/issues/2638
[jsonschema]: https://json-schema.org/understanding-json-schema/index.html
