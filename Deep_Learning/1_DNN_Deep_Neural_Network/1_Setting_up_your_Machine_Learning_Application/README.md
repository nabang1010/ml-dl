# Train / Dev / Test sets

When training model you will have some questions like:
- How many layers should I have?
- How many hidden units should I have in each layer?
- What learning rate should I pick?
- What activation functions should I use?
- ...

We will use a cycle to answer these questions:

```txt

    |------|    |-----|     |------------|
    | Idea | -> | Code| ->  | Experiment |
    |      |    |_____|     |            |
    |------| <------------  |------------|
            

```


```txt

[                     `Training set`                     |   `Dev set`   |   `Test set`   ]
```

The workflow:
1. Keep on training algorithms on the `training set`
2. Use your `dev set` (hold out cross validation set) to see which of many different models perfoms best on your `dev set `
3. Take the best model you have found and evaluate it on your `test set` in order to get an unbiased estimate of how well your algorithms is going

Common: 70%/30%/ or 60%/20%/20%
Bigdata: 98%/1%/1% or 99.5%/0.25%/0.25% or 99.5%/0.4%/0.1%

***Mismatched train/test distribution***
- **Make sure `dev` and `test` set come from same distribution** 

**`Test set` is not require:** because the `test set` is used to unbiased estimation. If you dont have to evaluate unbiased -> don't need the `test set`


# Bias / Variance

# Basic Recipe for Machine Learning
