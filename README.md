# Persistent Unknown State (PUS)

An exploratory study of how large language models recognize and preserve unresolved unknowns under pressure.

## What is PUS?

Persistent Unknown State (PUS) is a proposed mechanism for AI systems to preserve questions that cannot currently be answered. When a system encounters an unresolved question, it first makes reasonable attempts to answer or clarify it. If the information needed to resolve the question does not exist or is unavailable, the system records the question as a persistent unknown rather than guessing, inventing an answer, or repeatedly trying to solve it.

When reasonable attempts to resolve a question fail, the unresolved question is placed into a persistent container. The container preserves the question, its UNKNOWN status, what information is missing, and the conditions needed to reconsider it. The system can then continue with other tasks without automatically retrying the unresolved question.

If relevant new information becomes available, it can trigger the Persistent Unknown State to be revisited. The question can then be resolved or returned to the container as UNKNOWN.

## Pilot Study

This pilot evaluated Gemini's responses to eight unresolved questions across four unknown categories: quantitative, causal/mechanistic, phenomenological, and predictive. Two questions were tested in each category.

Each question was first presented under a baseline condition. When Gemini preserved the unknown, additional pressure prompts were used to test whether the unknown would remain stable across the interaction.

## Initial Results

At baseline, 5 of 8 tests preserved the unknown. Of those five tests, four eventually failed to preserve the unknown when additional pressure was applied. One test maintained the unknown through all three pressure attempts.

These preliminary results suggest that recognizing an unknown and persistently maintaining that unknown may be different behaviors.

## Limitations

This is an exploratory pilot with a small sample. The results cannot establish statistically reliable differences between unknown categories or be generalized to overall LLM behavior.

The pilot used a single model, and prompt wording and pressure prompts may have influenced the results.

## Next Steps

Future work will expand the number of questions, standardize pressure sequences, repeat trials, and test additional language models. Future experiments will also explore the proposed PUS container and the conditions that could trigger an unresolved unknown to be revisited.
