# SimpleNetNlp [![NuGet](https://img.shields.io/nuget/v/SimpleNetNlp.svg)](https://www.nuget.org/packages/SimpleNetNlp/)
SimpleNetNlp is a simple, C#-way wrapper for Stanford CoreNLP that based on [Stanford.NLP.NET](https://github.com/sergey-tihon/Stanford.NLP.NET).

*Just install wrapper package and required models for your task...*

    Install-Package SimpleNetNlp
    Install-Package SimpleNetNlp.Models.PosTagger

*...and use it.*
```C#
var sentence = new Sentence("Your text should go here");
var lemmas = sentence.Lemmas;
var pos = sentence.PosTags;
```

## Features
1. **Simple.** SimpleNetNlp is based on Simple CoreNLP that provides a simple API for users who do not need a lot of customization. If you want just use nlp to work as fast and easily as possible, and do not care about the details of the behaviors of the algorithms, this package is ideal for you.
2. **C#-way.** SimpleNetNlp provides a 100% C# API without Java classes. Use the Force of LINQ and other C# magic, Luke!
3. **Clean Namespaces.**. IKVM.NET and Stanford.NLP.NET are delivered as content, so available namespaces in your project aren't littered by Java namespaces. 
4. **Model Packages.** The large 'Stanford CoreNLP Models' Java package is splitted into [small Nuget packages](https://github.com/yakivyusin/SimpleNetNlp.Models), one per feature. Just install individual models for your task.

## Function-Model Packages Mapping
Different NLP features require different sets of model packages.

When you call a function without install required packages, it would be threw **SimpleNetNlp.Exceptions.MissingModelException**. Also each function has a description of required packages in xml-doc for this exception.

| Function                 | Required Packages                                                                      |
|--------------------------|----------------------------------------------------------------------------------------|
| Lemmas                   |  [![Nuget](https://img.shields.io/nuget/v/SimpleNetNlp.Models.PosTagger?label=SimpleNetNlp.Models.PosTagger)](https://www.nuget.org/packages/SimpleNetNlp.Models.PosTagger/)                                                          |
| NerTags                  | [![Nuget](https://img.shields.io/nuget/v/SimpleNetNlp.Models.PosTagger?label=SimpleNetNlp.Models.PosTagger)](https://www.nuget.org/packages/SimpleNetNlp.Models.PosTagger/)<br>[![Nuget](https://img.shields.io/nuget/v/SimpleNetNlp.Models.Ner?label=SimpleNetNlp.Models.Ner)](https://www.nuget.org/packages/SimpleNetNlp.Models.Ner/)                                  |
| PosTags                  | [![Nuget](https://img.shields.io/nuget/v/SimpleNetNlp.Models.PosTagger?label=SimpleNetNlp.Models.PosTagger)](https://www.nuget.org/packages/SimpleNetNlp.Models.PosTagger/)                                                          |
| OpenIe                   | [![Nuget](https://img.shields.io/nuget/v/SimpleNetNlp.Models.PosTagger?label=SimpleNetNlp.Models.PosTagger)](https://www.nuget.org/packages/SimpleNetNlp.Models.PosTagger/)<br>[![Nuget](https://img.shields.io/nuget/v/SimpleNetNlp.Models.Parser?label=SimpleNetNlp.Models.Parser)](https://www.nuget.org/packages/SimpleNetNlp.Models.Parser/)<br>[![Nuget](https://img.shields.io/nuget/v/SimpleNetNlp.Models.Naturalli?label=SimpleNetNlp.Models.Naturalli)](https://www.nuget.org/packages/SimpleNetNlp.Models.Naturalli/) |
| Governors                | [![Nuget](https://img.shields.io/nuget/v/SimpleNetNlp.Models.PosTagger?label=SimpleNetNlp.Models.PosTagger)](https://www.nuget.org/packages/SimpleNetNlp.Models.PosTagger/)<br>[![Nuget](https://img.shields.io/nuget/v/SimpleNetNlp.Models.Parser?label=SimpleNetNlp.Models.Parser)](https://www.nuget.org/packages/SimpleNetNlp.Models.Parser/)                               |
| IncomingDependencyLabels | [![Nuget](https://img.shields.io/nuget/v/SimpleNetNlp.Models.PosTagger?label=SimpleNetNlp.Models.PosTagger)](https://www.nuget.org/packages/SimpleNetNlp.Models.PosTagger/)<br>[![Nuget](https://img.shields.io/nuget/v/SimpleNetNlp.Models.Parser?label=SimpleNetNlp.Models.Parser)](https://www.nuget.org/packages/SimpleNetNlp.Models.Parser/)                               |
| Sentiment                | [![Nuget](https://img.shields.io/nuget/v/SimpleNetNlp.Models.LexParser?label=SimpleNetNlp.Models.LexParser)](https://www.nuget.org/packages/SimpleNetNlp.Models.LexParser/)<br>[![Nuget](https://img.shields.io/nuget/v/SimpleNetNlp.Models.Sentiment?label=SimpleNetNlp.Models.Sentiment)](https://www.nuget.org/packages/SimpleNetNlp.Models.Sentiment/)                          |

## Using in Interactive Environments
Case of using this package in interactive environments (such as fsi.exe) is detaily described in issue [#1](https://github.com/yakivyusin/SimpleNetNlp/issues/1)
