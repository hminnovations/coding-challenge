# Thanks for applying to work with us!

As a member of the Healthy Minds development team, you’ll be working closely with our team of content producers to translate the Healthy Minds Program into several machine and human-readable formats. To work effectively in this environment, you’ll need to be able to quickly read and understand large JSON documents and to combine multiple files that partially describe a situation into one coherent whole.

## Your Challenge

Write a JavaScript or TypeScript (Node.JS version 12.18.0) program to combine a partial Healthy Minds Program description with a record of one user’s progress through the program and produce a human-readable CSV document that describes Alice’s progress through the program in an easy to understand way. 

Please use the following two mock API endpoints when building your solution

### Program Description Endpoint

```
https://raw.githubusercontent.com/hminnovations/coding-challenge-content/master/healthy-minds-description.json
```

### User Progress Endpoint

```
https://raw.githubusercontent.com/hminnovations/coding-challenge-content/master/alice-progress.json
```

Your output CSV should contain 1 row for each `"activity"` on the path and 6 columns:

1. Activity UUID: The value of the `"uuid"` field for the activity.
2. Module number and title: The number of the module that contains that activity and its `"title"`. The first module, for instance, should render here as `"1 - Getting Started"`.
3. Part number and title: The number of the part that contains the activity and its `"title"`. The first part in the first module, for instance, should render here as `"1 - Getting Started"`.
4. Series number and title: The number of the series that contains the activity and its `"title"`. The first series in the first part of the first module, for instance, should render here as `"1 - INTRODUCTION"`.
5. Task types: The set of task types contained in the activity, separated by commas. For the first activity, for instance, task types should render here as `"info, learn, survey"`.
6. Completion Status: A `1` or `0` indicating whether Alice has completed, or not completed (respectively) the activity.

Your output should look similar to `alice-progress.csv`

## How We Grade Solutions

Include instructions for running your program within your solution. It should be run with a terminal command, for example:

```bash
node your-solution.js output.csv
yarn start --output output.csv
npm run start --outFile output.csv
```

We’ll be running your app using Node.JS version 12.18.0.

Results will be verified by a human, so minor differences in casing and quoting style won’t necessarily disqualify you, but please try to mimic the format of `alice-progress.csv` as closely as possible to keep our test checkers happy. 🙂

## Other considerations

* Code organization
* Documentation
* Testing