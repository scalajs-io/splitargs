SplitArgs API for Scala.js
================================
This is a Scala.js type-safe binding for [SplitArgs](https://www.npmjs.com/package/splitargs)

Splits strings into tokens by given separator except treating quoted part as a single token.

#### Build Requirements

* [ScalaJs.io v0.3.x](https://github.com/ldaniels528/scalajs.io)
* [SBT v0.13.13](http://www.scala-sbt.org/download.html)


#### Build/publish the SDK locally

```bash
 $ sbt clean publish-local
```

#### Running the tests

Before running the tests the first time, you must ensure the npm packages are installed:

```bash
$ npm install
```

Then you can run the tests:

```bash
$ sbt test
```

#### Examples

```scala
val line = "I said 'I am sorry.', and he said \"it doesn't matter.\""
val args = SplitArgs(line)
Assert.deepEqual(args, js.Array("I", "said", "I am sorry.,", "and", "he", "said", "it doesn\'t matter."))
```

#### Artifacts and Resolvers

To add the Moment binding to your project, add the following to your build.sbt:  

```sbt
libraryDependencies += "io.scalajs.npm" %%% "splitargs" % "0.3.0.3"
```

Optionally, you may add the Sonatype Repository resolver:

```sbt   
resolvers += Resolver.sonatypeRepo("releases") 
```
