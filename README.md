# FV2019
Danish general election prediction competition

This is for submitting entries for predictoin the distribution of legal votes in the upcoming Danish election. The rules of the competition is as follows:

*   The competition is about predicting the votes given to each of the parties eligible for the Danish parliament.
*   The deadline for submitting entries is **May 31st 2019 at midnight (CET)**.
*   A submission consists of a pull request to this repository. 
*   Each person should only submit one entry
*   A prediction consists of a data frame with two columns: `party` and `percent`. The `percent` column will subsequently be scaled such that it sums to 100.

    A blueprint for an `R` object to submit is
    
    ```
    myprediction <- data.frame(party=c("A", "B", "C", "D", "E", "F", "I", "K", "O", "P", "V", "OE", "AA"),
                                percent=rep(1/13, 13))
    ```

*    Each prediction is score by the Brier score: the mean squared prediction error when comparing to the actual distribution of votes after the election.
