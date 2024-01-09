---
description: How to add hints and automated feedback to common problem components.
---

# Hints and Feedback

You can add hints and feedback to your questions. By using hints and feedback, you can provide learners with guidance and help them as they work on problems.

![Display of Feedback and Hints in question](<../../.gitbook/assets/Screen Shot 2020-07-06 at 09.28.34.png>)

###

### Add Hints

To ensure that your hints can assist learners with varying backgrounds and levels of understanding, you should provide multiple hints with different levels of detail.

For example, the first hint can orient the learner to the problem and help those struggling to better understand what is being asked. The second hint can then take the learner further towards the answer.

In problems that are not graded, the third and final hint can explain the solution for learners who are still confused.

To add _**Hints**_ to your question, add them between `||` or copy and paste the following code template at the bottom of your question:&#x20;

![Add hints underneath the question.](<../../.gitbook/assets/Screen Shot 2020-07-17 at 11.30.40.png>)

`||You can add an optional hint like this. Problems that have a hint include a hint button, and this text appears the first time learners select the button.||` \
`||If you add more than one hint, a different hint appears each time learners select the hint button.||`

{% hint style="info" %}
**Hints** are accessible for learners using the hint button. If no hint is added the _**Hint**_ button will not be visible to learners.&#x20;
{% endhint %}

### Add Feedback

The immediacy of the feedback available to learners is a key advantage of online instruction and difficult to do in a traditional classroom environment.

You can target feedback for common incorrect answers to the misconceptions that are common for the level of the learner (for example, elementary, middle, high school, college).

In addition, you can create feedback that provides some guidance to the learner about how to arrive at the correct answer. This is especially important in text input and numeric input problems, because without such guidance, learners might not be able to proceed.

You should also include feedback for the correct answer to reinforce why the answer is correct. Especially in questions where learners are able to guess, such as multiple choice and dropdown problems, the feedback should provide a reason why the selection is correct.

To add Feedback to your question, add them between `{{` and `}}` directly after each possible question response, or copy and paste the following templates :

{% hint style="info" %}
**Feedback** appears automatically after a learner selects and submits an answer.
{% endhint %}

####

#### Multiple choice Feedback

`( ) an incorrect answer  {{Specify optional feedback to appears after this answer is submitted.}}` \
`(x) the correct answer`\
`( ) an incorrect answer {{Specify optional feedback for none, a subset, or all of the answers.}}`&#x20;



#### Checkboxes Feedback

Checkboxes Feedback allows you to define what feedbacks should be displayed if the answer is _selected_ or _unselected_.

`>>Question text or prompt.||Optional tip or note.<<`\
\
`[x] a correct answer  {{ selected: Specify optional feedback that appears after the learner selects and submits this answer. }, { unselected: Specify optional feedback that appears after the learner clears and submits this answer.}}`\
`[ ] an incorrect answer` \
`[ ] an incorrect answer {{ selected: You can specify optional feedback for none, all, or a subset of the answers. }, { unselected: You can specify optional feedback for selected answers, cleared answers, or both.}}`\
`[x] a correct answer`\
\
`{{ ((A B D)) You can specify optional feedback for a combination of answers which appears after the specified set of answers is submitted.}}` \
`{{ ((A B C D)) You can specify optional feedback for one, several, or all answer combinations. }}`

####

#### Dropdown Feedback

`[[ an incorrect answer  {{Specify optional feedback to appears after this answer is submitted.}}` \
`(the correct answer)`\
`an incorrect answer {{Specify optional feedback for none, a subset, or all of the answers.}}` \
`]]`

####

#### Numerical input Feedback

`=100 +-5% {{Specify optional feedback to appears after this answer is submitted.}}`&#x20;

####

#### Text Input Feedback

`= the correct answer {{Specify optional feedback to appears after this answer is submitted.}}` \
`or= optional acceptal variant of the correct answer`\
`not= optional incorrect answer such as a frequent misconception {{Specify optional feedback for none, a subset, or all of the answers.}}`&#x20;
