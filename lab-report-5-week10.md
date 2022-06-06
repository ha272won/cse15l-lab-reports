## How you found the tests with different results?

Modify the bash script as below:
![Screen Shot 2022-05-31 at 12 07 16 AM](https://user-images.githubusercontent.com/103228431/171113911-fd044259-5df8-4844-955e-fa262130868a.png)

run `bash script.sh > results.txt` after compiling the MarkdownParser.java. This allows to save the result file in the repository. Also, do the same for my markdownparse repository. Then, comeback to the main and run `diff` command to compare two txt file.

## Provide a link to the test-file with different-results
[test-file 487](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/487.md)
[test-file 504](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/504.md)

## Describe which implementation is correct, or neither if both give the wrong output

For both #487 and #504, the provided repository gives the right output. 

#487 : It shows that my code does not check the characters between parentheses that manage the link. In the case of #407, the special character: / is inserted, but this special character cannot be filtered out and are exposed in my code.

#504 : Same as #487, my code cannot check special character. When #487 has a problem because it cannot detect '/', for #504, it cannot detect other characters too: '""', '''', '()'. 

## Indicate both actual outputs (provide screenshots) and also what the expected output is (list the links that are expected in the output).
Test-file #487
provided repository
![Screen Shot 2022-06-04 at 9 21 25 PM](https://user-images.githubusercontent.com/103228431/172034939-7924e9df-8b32-4c33-84b1-bdad11bd0a00.png)

my repository
![Screen Shot 2022-06-04 at 9 20 09 PM](https://user-images.githubusercontent.com/103228431/172034934-38d5f947-3490-4f2b-8c3c-7e79124bb09e.png)

Test-file #504
provided repositoy
![Screen Shot 2022-06-04 at 9 21 20 PM](https://user-images.githubusercontent.com/103228431/172034937-0f459d49-096b-45c0-ad5a-85e98df0dd6c.png)

my repository
![Screen Shot 2022-06-04 at 9 19 57 PM](https://user-images.githubusercontent.com/103228431/172034930-ccd2802d-8789-4e1d-a0bb-218683a8e469.png)

For #487 : we expect
For #504 : we expect

## Decide on what it should produce (i.e., expected output) by using either VScode preview or the CommonMark demo site.
For test-file 487.md:
![Screen Shot 2022-06-04 at 4 28 58 PM](https://user-images.githubusercontent.com/103228431/172028728-64ca2780-9271-4d62-a51f-738527827eb5.png)

For test-file 504.md:
![Screen Shot 2022-06-04 at 4 29 10 PM](https://user-images.githubusercontent.com/103228431/172028730-db6d58ec-c9aa-4a8b-9a70-c292ef50ded4.png)

## For the implementation that’s not correct (or choose one if both are incorrect), describe the bug (the problem in the code) in about 2-3 sentences. 

My MarkdownParser.java is like below:
![Screen Shot 2022-06-04 at 9 22 08 PM](https://user-images.githubusercontent.com/103228431/172034952-a25e84ef-fa9d-463e-94a0-b9c28377ebef.png)
![Screen Shot 2022-06-04 at 9 23 38 PM](https://user-images.githubusercontent.com/103228431/172034964-0f5985ad-9dba-4b86-b470-b60322878db2.png)


For both #483 and #504, to correct this, the code in the if statement must be modified. Instead of directly adding a substring to a variable to be returned within an if statement, we can fix the code in #487 if we add a condition to the temporary variable to store the substring for further verification
