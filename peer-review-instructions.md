# Slack CLI - Peer Review

## Learning Goals

- Apply code reading skills and code review skills to another codebase under a familiar problem
- Practice navigating someone else's code base
- Practice collaborating over GitHub with a pair
- Practice navigating GitHub's Pull Request feature to clone someone's repo

## Objective

Your Slack CLI needs a code review. You have the code, and a reviewer assigned! Spend time with your reviewer to make sure that **your reviewer pushes git commit(s) to your fork of the `slack-cli-reflection` repo with their code review of your project.**

At the same time, you should be reviewing your pair's Slack CLI project! You should spend time with your pair to make sure that **YOU push git commit(s) to the fork of your pair's `slack-cli-reflection` repo with your code review of their project.**

Follow the activity below to learn more.

Don't forget:

- This is not about seeing someone else's perfect code. This is about practicing reading code and giving meaningful feedback to them. Assume best intention while you review code!
- This is not about defending your code, or thinking that you are defined by your code; also assume best intention!
- You may be reviewing someone's project that isn't complete! That is 100% perfect and fine; continue to review their code as is.
- You may be getting reviewed and your project isn't complete! That is 100% perfect and fine; allow your code to be reviewed as is.
- Ada's philosophy on learning is focused on reflection, collaboration, and strength, so that everyone collectively improves in the future.

## Requirements

- Your reviewer must be added as a collaborator to this repo
- Your reviewer must make changes on this file on this repo
    - The changes should be answering the prompts below
    - The changes should be git commits and pushed to this repo

Don't forget: Everyone, including your instructors, are able to see the commit history and who commited what changes at what time!

## Suggested Structure

Because pairs will need to review each other's code, we suggest scheduling ~1 hour of time to collaborate with each other and follow the activity below.

## Peer Review Activity

### Instructions for the Reviewed (You)

1. Read through [Ada's guide for How to give a Code Review](https://github.com/Ada-Developers-Academy/textbook-curriculum/blob/master/03-leadership-and-inclusion/pair-feedback-and-code-reviews.md#how-to-give-a-code-review)
1. Read through the instructions below and the [Peer Review feedback file](feedback.md) before you get started
1. Coordinate with your pair so that they fill out [the Peer Review feedback file](feedback.md) for your Slack CLI submission, and commit and push those file changes before the due date.

### Instructions for the Reviewer (Your Pair)

1. Read through [Ada's guide for How to give a Code Review](https://github.com/Ada-Developers-Academy/textbook-curriculum/blob/master/03-leadership-and-inclusion/pair-feedback-and-code-reviews.md#how-to-give-a-code-review)
2. Pull in the branch for the student you are reviewing
    - Navigate to the Slack CLI [PR page](https://github.com/Ada-C13/slack-cli/pulls), and then...
        1. click on the pull request name
        2. then click on the name of the submission branch (i.e. criacuervos: master)
        
        ![PR](images/pr.png)

3. Clone this fork on your computer in a different directory then your own forked repository.
      - Don't clone your pair's Slack CLI project into your normal `projects` folder, because then your computer will say that a project named `slack-cli` already exists. Navigate to or make a different folder for this exercise.
4. Create a valid `.env` file that this new Slack CLI project can look at
      - After cloning your reviewee's repo, `$ cd slack-cli` into your reviewee's project
      - Create a `.env` file in this folder with `$ touch .env`
      - Find your own Slack CLI's `.env` file, and copy the contents. You should be copying text that looks like `SLACK_TOKEN=xxxx-xxxx-xxxx`
      - Go back to your reviewee's Slack CLI project, and paste your `SLACK_TOKEN=xxxx-xxxx...` text into that `.env` file
5. Complete the feedback rubric defined in `feedback.md` by testing the app and reviewing the code. You should be making changes to your reviewee's `feedback.md` file in their `slack-cli-reflection` repo. Alter the table cells that say `yes/no` to the appropriate `yes` or `no`.

Tip: Use VS Code's extension "Markdown Preview" in order to help you visualize the feedback table.

**At the end of this review, don't forget to commit and push your review. Otherwise, instructors won't be able to see your work.**


<details>
    <summary>
        For the curious: What's going on when we have to make a new valid .env file for our review?
    </summary>

Well, as you know, your Slack CLI projects are looking for the value `ENV[SLACK_TOKEN]`... and we didn't push our `.env` file to GitHub! Therefore, the reviewer is not pulling/cloning that `.env` file when they start reviewing it, so we need to provide valid credentials for them. However, there is no negative consequence to using your own token, even on your partner's project, since they're all accessing the same Slack API... just different workspaces. :)

In industry, the practice that we would do is share on a team a list of test credentials. We don't have those tools right now though!
</details>
