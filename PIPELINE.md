Which events will trigger your CI, and why?

push to main -> automatically runs the workflow when pushed to main , workflow_dispatch -> allow manual triggering of the pipeline ,
PR -> validates code changes before merging into main 

Which jobs will you create? Draw the job graph (which run in parallel, which wait for which).

test -> independent , lint -> independent and parrellel with test  , package depend on test


What is the artifact this pipeline produces?



Is this pipeline CI, Continuous Delivery, or Continuous Deployment? Justify in one sentence.

CI -> because it auto builds and runs tests on code changes 

What should happen to the package job when tests fail, and why is that what you want?

should be skipped so the broken code is never packaged or released 