- CircleCI provides CI/CD orchestration
- Continuous integration (CI) is the act of working in a shared repository, and the triggering of automated tests and builds that support that
	- Enables collaboration whilst ensuring it done safely
- Continuous delivery (CD) is a practice that produces reliable releases to a chosen environment

### Units
- The smallest unit in CircleCI is a step
	- A step is a single execution of a task, and CircleCI has predefined steps
	- The most broad step is the `run` step, which allows you to run a command in a shell
	- Other steps are listed [here](https://circleci.com/docs/reference/configuration-reference/#steps)
- The next smallest unit is a job
	- A job is composed of one or more steps
- The next unit is a workflow
	- A workflow is composed of one or more jobs
	- A single workflow can run different jobs concurrently, or can be orchestrated to run jobs sequentially, or both at the same time
- The next unit is a pipeline
	- This, in my opinion, is badly named as it's just a single execution of a workflow - a more appropriate name would be `workflow run`
	- Pipelines can have parameters that can be used in smaller units, enabling us to run a single workflow for different use cases
