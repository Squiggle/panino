*Pedantic Analysis for Numerical Inference and Negative Output*

The goal of this project is to create a service which identifies and corrects people on their poor use of pluralisation.

Extra success criteria include:

* Fluent syntax
* A range of integrations for input and output
* Adoption of neural network processing for identifying correct/incorrect usages of cardinality
* IObservable and realtime input/output

# Examples

Given suitable configuration (i.e. authentication to appropriate external services), the following are examples of the intended syntax:

**Example 1:** Command the service to analyse a twitter feed for misuse of language. Report any findings in a polite manner to a local text file.

```csharp
Scrutinize(Twitter.Posts.From("Squiggle"))
  .Output(Critique.To(File("ahem.txt");
```

**Example 2:** Command the service to analyse all StackOverflow chat messages from a named user. Report any findings in an abusive manner to the console.

```csharp
Scrutinize(StackOverflow.Chat.MessagesFrom("Dave"))
  .Output(StreamOfAbuse.To(Console));
```

