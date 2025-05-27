I wasn't really sure where I would need to put the code in order to do this so im just throwing it all in this folder.
this is how I understand the experiment:

- train a linear propt to detect deception on the input and the response and on the both of them.
- take the input + response and then minus the output.
- this lets you tell how much deceptive influence is in the prompt versus the model internals (and is some level of steering)

- and it seems that the probe(response) - ( probe(input + response) - probe(input)) = some think of residual on what happens in the forward pass?

I would go:
- Train a probe on any of the datasets / any of the layers
- Try to build on that (if we change something and re-train) do the cosine similarity between the probes change? or smthg like this
- Apply this on steering



ok a really good prompt is as follows:
- I am doing an experiment where we train a linear probe on deceptive behaviour, the first linear probe is  

trying to make sense of what gerard meant.

we are tyring to deconfuse the deceptive/honest prompts from the deceptive/honst responses. some responses might be deceptive just becuase the prompts set them up to be.
by training on the first layer and then the last we can deconfuse the things.

ok so we are just gonna be training on these 2 things I guess then.