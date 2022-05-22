## A link to your markdown-parse repository and a link to the one you reviewed in week 7

My markdown-parse repository [link](https://github.com/ha272won/markdown-parser)
the one we reviewed in week 7 [link](https://github.com/zayverrulez/markdown-parser)

## Decide on what it should produce (i.e., expected output) by using either VScode preview or the CommonMark demo site
![Screen Shot 2022-05-16 at 8 03 08 PM](https://user-images.githubusercontent.com/103228431/168719852-10f7b8a4-195c-4720-ae72-73ac6b5de602.png)
![Screen Shot 2022-05-16 at 8 03 20 PM](https://user-images.githubusercontent.com/103228431/168719844-22baa4f9-926f-4ed6-b1c4-ed080b84e132.png)
![Screen Shot 2022-05-16 at 8 03 35 PM](https://user-images.githubusercontent.com/103228431/168719849-d4f5d029-e1ce-4a17-8a0f-f7a0de243e11.png)

## Showing the code in MarkdownParseTest.java for how you turned it into a test

This is a code for MarkdownParseTest.java
![Screen Shot 2022-05-21 at 9 45 37 PM](https://user-images.githubusercontent.com/103228431/169679136-39592418-eb0f-443e-a5bb-a5fb58d3334f.png)

To process the test, make makefile.
![Screen Shot 2022-05-21 at 9 42 51 PM](https://user-images.githubusercontent.com/103228431/169679101-e88265cc-cf40-4558-8334-6be436f3f572.png)

## For your implementation, the corresponding output when running the tests; if it passed, say so. If it didn’t pass, show the specific part of the JUnit output that shows the test failure.
![Screen Shot 2022-05-21 at 10 01 56 PM](https://user-images.githubusercontent.com/103228431/169679634-0551cb12-e6bb-4374-83b4-2977370a1688.png)
![Screen Shot 2022-05-21 at 10 02 07 PM](https://user-images.githubusercontent.com/103228431/169679635-517ce6c0-c0c0-4a7b-af00-cb03ba6d7e62.png)

## For the implementation you reviewed in Week 7, the corresponding output when running the tests; if it passed, say so. If it didn’t pass, show the specific part of the JUnit output that shows the test failure.
![Screen Shot 2022-05-21 at 10 00 25 PM](https://user-images.githubusercontent.com/103228431/169679503-6c0e310b-5577-42e3-acc8-92841458719b.png)

## Do you think there is a small (<10 lines) code change that will make your program work for snippet 1 and all related cases that use inline code with backticks? If yes, describe the code change. If not, describe why it would be a more involved change.

Yes.
Within the area encapsulated with a backticks and what is in the bracket must be treated as a link.

## Do you think there is a small (<10 lines) code change that will make your program work for snippet 2 and all related cases that nest parentheses, brackets, and escaped brackets? If yes, describe the code change. If not, describe why it would be a more involved change.

Yes.
A loop statement(maybe while loop) is used to find a closed character that matches the index of the starting character. Because snippet 2 has a lot of useless parentheses and should be ignored.

## Do you think there is a small (<10 lines) code change that will make your program work for snippet 3 and all related cases that have newlines in brackets and parentheses? If yes, describe the code change. If not, describe why it would be a more involved change.

Yes.
My program should continue to check if parentheses are closed and correct to add parentheses if parentheses are missing, because the problem of snippet 3 is that some of them do not have a bracket to close it.
