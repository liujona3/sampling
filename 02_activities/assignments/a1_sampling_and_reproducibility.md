# ASSIGNMENT: Sampling and Reproducibility in Python

Read the blog post [Contact tracing can give a biased sample of COVID-19 cases](https://andrewwhitby.com/2020/11/24/contact-tracing-biased/) by Andrew Whitby to understand the context and motivation behind the simulation model we will be examining.

Examine the code in `whitby_covid_tracing.py`. Identify all stages at which sampling is occurring in the model. Describe in words the sampling procedure, referencing the functions used, sample size, sampling frame, any underlying distributions involved, and how these relate to the procedure outlined in the blog post.

Run the Python script file called whitby_covid_tracing.py as is and compare the results to the graphs in the original blog post. Does this code appear to reproduce the graphs from the original blog post?

Modify the number of repetitions in the simulation to 100 (from the original 1000). Run the script multiple times and observe the outputted graphs. Comment on the reproducibility of the results.

Alter the code so that it is reproducible. Describe the changes you made to the code and how they affected the reproducibility of the script file. The output does not need to match Whitby’s original blogpost/graphs, it just needs to produce the same output when run multiple times

# Author: Jonathan Liu

```
Stages where sampling occurs:
    i) random sample of people attending events are infected using the code:
        infected_indices = np.random.choice(ppl.index, size=int(len(ppl) * ATTACK_RATE), replace=False)
        ppl.loc[infected_indices, 'infected'] = True
        - Attack rate was set to 10%, with the  1000 people being the sampling frame, and distribution is uniform random sampling without replacement, the sample size would be 100 people infected.
        - It aligns with the infection rate outlined in the blog post where each person has a 10% chance of being infected.

    ii) of the people infected, a random subset are successfully traced using the code:
        ppl.loc[ppl['infected'], 'traced'] = np.random.rand(sum(ppl['infected'])) < TRACE_SUCCESS
        - Success rate for tracing was set to 20%, with the people infected being the sampling frame, and the distribution is Bernouli, where the infected is traced or isn't traced, the sample size would be 20 people who are infected and traced
        - It aligns with the tracing rates outlined in the blog post, where each infection has a 20% chance of being traced to a source event.

    iii) If two infections are independently traced to the same source event (conditional), secondary contact traced using the code:
        event_trace_counts = ppl[ppl['traced'] == True]['event'].value_counts()
        events_traced = event_trace_counts[event_trace_counts >= SECONDARY_TRACE_THRESHOLD].index
        ppl.loc[ppl['event'].isin(events_traced) & ppl['infected'], 'traced'] = True
        - Once an event reaches the threshold (2), every person from that event is sampled into the secondary traced group, with the sampling frame being everyone infected, the distribution being conditional, the same size would be all infected individuals at the venets where traced cases were greater than or equal to 2.
        - This is the core source of bias mentioned by the author, where weddings can trigger the threshold and be over represented in tracing data. 


The original script does seem to produce the graphs from the original blog post.

When the repititiona are changed from 1000 to 100, the outputted graphs the overall trend is still present BUT the results vary more and the graphs are more 'skewed' and reproducibility is reduced as the results are more variable and tend change more compared to 1000 repititions. 

To make the code reproducible, I added a line of code to set a random seed (44) before any random functions. This sets the randomness to a fixed starting point so that the same series of 'random' events occur. 

```


## Criteria

|Criteria|Complete|Incomplete|
|--------|----|----|
|Altercation of the code|The code changes made, made it reproducible.|The code is still not reproducible.|
|Description of changes|The author explained the reasonings for the changes made well.|The author did not explain the reasonings for the changes made well.|

## Submission Information

🚨 **Please review our [Assignment Submission Guide](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md)** 🚨 for detailed instructions on how to format, branch, and submit your work. Following these guidelines is crucial for your submissions to be evaluated correctly.

### Submission Parameters:
* Submission Due Date: `23:59 - 09/04/2025`
* The branch name for your repo should be: `assignment-1`
* What to submit for this assignment:
    * This markdown file (a1_sampling_and_reproducibility.md) should be populated.
    * The `whitby_covid_tracing.py` should be changed.
* What the pull request link should look like for this assignment: `https://github.com/<your_github_username>/sampling/pull/<pr_id>`
    * Open a private window in your browser. Copy and paste the link to your pull request into the address bar. Make sure you can see your pull request properly. This helps the technical facilitator and learning support staff review your submission easily.

Checklist:
- [ ] Create a branch called `assignment-1`.
- [ ] Ensure that the repository is public.
- [ ] Review [the PR description guidelines](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md#guidelines-for-pull-request-descriptions) and adhere to them.
- [ ] Verify that the link is accessible in a private browser window.

If you encounter any difficulties or have questions, please don't hesitate to reach out to our team via the help channel in Slack. Our Technical Facilitators and Learning Support staff are here to help you navigate any challenges.
