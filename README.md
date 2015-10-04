# Solving a Lab - OSX

## Overview

Once you've opened your lab locally, whether using the `git` CLI workflow of Forking and Cloning, or whether you used the `learn` CLI workflow using `learn open`, you're ready to solve the lab.

All of the labs on Learn are written with an RSpec test suite that you can use to confirm that you've fulfilled the requirements of the lab. RSpec is a testing library that ruby developers use everyday, so again, as you work on Learn, you're also learning the same tools and workflows that developers use.

## Test Driven Workflow

When you work on a lab, we recommend the following workflow:

### 1. Reading the README

Read the lab's README on Learn and get a sense of what the lab is about and what it is asking you to build. Read the entire README and then work on the lab and as you hit hurdles you'll have a context for where to look for clues and hints in the README.

### 2. Run the tests with `learn`

Before doing any work, run the test suite from your local clone with the `learn` CLI command. From your terminal, in a lab's directory, run `learn`, you'll see something similar to:

![Failing Test](https://dl.dropboxusercontent.com/s/0ik01a1urmuw7o6/2015-09-30%20at%207.46%20PM.png)

I know error messages or failure messages are intimidating, but try to read them. Developers are detectives, constantly sleuthing for the bug that's the culprit. Errors and failures are our clues, they illuminate the path forward.

We know that the idea of "things being broken" is frightening at first. Broken things are stressful and frustrating! But guess what? As an engineer, as a programmer, the default state of anything you work on is broken. The things you are programming are always broken. Get used to it. Your job is to fix broken things. You can do it. If your code isn't broken, if your code works, you are no longer programming, you're job is done, things work. Embrace the errors. The obstacle is the way.

### 3. Read the tests

Read the test suite in `spec/`. Open up the lab in your text editor, open the files in the `spec` directory that are not named `spec_helper.rb`. `spec_helper.rb` is a helper file to configure your tests which you can ignore. Any file in `spec` that ends in `_spec.rb` though is a test file and while testing code and RSpec are advanced, we believe the semantics are easy to understand, the meaning of the test is comprehensible, even if the code is not. For example, soon you'll be solving your first lab. The lab includes a file `spec/first_lab_spec.rb`. The contents will be:

```ruby
describe 'First Lab:' do
  it 'you made a change' do
    new_file_made = Dir["*"].size > 5
    file_edited = !File.read("./edit-me.txt").empty?
    expect((new_file_made || file_edited)).to be_truthy, "Make sure you have added a new file or edited edit-me.txt"
  end
end
```

You haven't even written a line of code yet and we're asking you to read some very abstract and complex code and try to reach for any footing or understanding. We believe in you. We believe you can infer and deduce and understand a bit of the code above, even with no experience. Your mind is  incredibly powerful. Challenge yourself confronting the unknown, that's how learning works.

Beyond all the syntax and code above, can you decipher what we're asking for? What the lab requires you to do? How the test works? Again, even if you only get 10% of the expectations of the test, that's still something. And while you do that, 4 things will happen.

1. You'll have 10% more understanding of how to solve the lab.

2. You'll get better at reading tests and we bet that the next test you read you'll get 12% of it and constantly see improvement through old fashion practice and determination.

3. Almost unconsciously, like Mr. Miyagi in the Karate Kid, you'll actually learn how to read and write tests proficiently, "Wax on, wax off" style.

![Wax On, Wax Off](https://38.media.tumblr.com/a5dc9f34d87226be8f31f5c982c8af7b/tumblr_mklzm4VeUq1rwt2uzo1_500.gif)

4. You'll have learned Test-Driven-Development, TDD, one of the most sought after skills of a professional developer.

This cycle, reviewing the README, running the tests, reading failure messages, reading the tests, editing your code, and trying it all again, is how you are supposed to code, it's what programmers do all day. We break things, we define the error with a test, we fix the code, we pass the test, we repeat.

### 4. Write Your Code

After forking and cloning the lab, opening the lab in a text editor, reading the README, running the test suite, reading the errors, and reading the tests themselves in `spec`, you're ready to code. You've armed yourself with every weapon available in the arsenal of your intellect and we know you can program triumphantly.

You should understand the point of the lab.

You should be able to identify the objectives and topics the lab is exercising so you can google for more information.

You should know the expected behavior or outcome of the solution.

You should know what files you need to create or edit.

You should know what those files and code should define, provide, and do.

You should constantly test your code with every significant change or attem.

You should read error messages and glean insight into the solution with every new failure.

You should keep on trying until you get it working. It doesn't matter how many times you fail as long as it is one less than the times you tried.

You should ask for help on Learn.

Programming is never about getting it all right at once. Programming is like solving a puzzle, you don't try to put it together immediately, you approach it one piece at a time. The workflow we're describing optimizes this process, trial and error, attempts and feedback, insight through failure. Most of our time as programmers is spent staring at error message and code wondering, "Hmm".

#### Programming in Movies vs Real Life
<iframe src="https://vine.co/v/hPXTA6l9AqQ/embed/simple" width="600" height="600" frameborder="0"></iframe>

### 5. Pass your local tests with `learn`

Follow this workflow, running tests, reading errors, writing code, running tests, reading errors, consulting the README, googling for more context on a topic, writing more code, running the tests again, reading errors, and repeat. You'll get it, you'll surprise yourself and find a confidence within you. And if you're just stuck or tired and just need some help, Ask a Question and the Learn community is here for you.

Eventually your local tests will pass and Learn.co will indicate your success.
![Pass](https://dl.dropboxusercontent.com/s/36nudmkxwmvrow9/2015-10-01%20at%2011.38%20PM.png)

On the left is a passing test run in the terminal, on the right is what the right column in Learn for a passing local test (which we currently call a "Local Build").

When your local tests are passing, you're ready to submit the lab.
