# us-2020-potus-model (output)

This .zip folder contains the output data from [_The Economist's_ 2020 presidential election forecast](https://projects.economist.com/us-2020-forecast/president). What follows is a brief description of all the files and labels for the variables within them.


*`state_polls.csv`*: A file containing all the state polls fielded so far.

Column | Description
--- | ---
`state` | The state the poll is from
`pollster` | The pollster that conducted the poll
`sponsor` | If a poll was conducted for a media or other organization, the name of the organization, otherwise empty
`start_date` | The first fielding date for the poll
`end_date` | The last fielding date for the poll
`entry_date_time_et` | The time the poll was entered into our model, in US Eastern Time
`number_of_observations` | The sample size for the poll
`population` | Whether the poll was conducted among registered or likely voters, or all adults
`mode` | Whether the poll was conducted via live interviews over the phone, online or some other method
`biden` | Biden's vote share in the poll
`trump` | Trump's vote share in the poll
`biden_margin` | Biden's vote margin in the poll
`other` | The vote share for third-party candidates, if reported
`undecided` | The share of voters who say they're undecided, if if reported
`url` | The url where you can read the poll
`include` | A dummy variable indicating whether the poll should be included in the model (almost always yes) 
`note` | Other notes
`biden_two_party` and `trump_two_party` | Biden and Trump's share of the two-party vote


*`national_polls.csv`*: A file containing all the national polls fielded so far. The columns and descriptions are the same as for the state polls.


*`state_correlation_matrix.csv`*: A file containing the pairwise correlations between simulated state-level Biden vote shares across all of the model's simulations. The column and row names correspond to each state.


*`state_averages_and_predictions_topline.csv`*: A file containing each state's adjusted polling average today and its predicted vote on election day, with confidence intervals and win probabilities.

Column | Description
--- | ---
`state` | The name of the state
`dem_average_low` | The lower bound of the uncertainty interval for the Democratic share of the two party vote _in polls today_
`dem_average_high` | The upper bound of the uncertainty interval for the Democratic share of the two party vote _in polls today_
`dem_average_mean` | The average Democratic share of the two party vote _in polls today_
`projected_vote_low` | The lower bound of the uncertainty interval for the projected Democratic share of the two party vote _on election day_
`projected_vote_high` |  The upper bound of the uncertainty interval for the projected Democratic share of the two party vote _on election day_
`projected_vote_mean` |  The average projected Democratic share of the two party vote _on election day_
`projected_win_prob` | The projected chance the Democratic candidate wins the state
`date` | The date this forecast was made


*`national_predicted_popular_vote.csv`*: A file containing the model's projected Democratic and Republican shares of the national two-party vote on each day remaining in the campaign.

Column | Description
--- | ---
`date` | The date for each forecast, from today to November 3rd, 2020
`party` | Which party's vote share is in this row of data
`projected_vote_high` | The upper bound of the uncertainty interval for the projected _x party_ share of the national two-party vote _on day x_
`projected_vote_low` | The lower bound of the uncertainty interval for the projected _x party_ share of the national two-party vote _on day x_
`projected_vote_mean` | The average projected _x party_ share of the national two-party vote _on day x_
`election_day` | A dummy variable indicating if the day is election day


*`national_polling_averages_over_time.csv`*: A file containing the model's estimates of the national popular vote _if the election were held today_, for each day the model ran so far.

Column | Description
--- | ---
`date` | The date for each forecast, from today to November 3rd, 2020
`party` | Which party's vote share is in this row of data
`poll_average_high` | The upper bound of the uncertainty interval for the estimated _x party_ share of the national two-party vote _if the election were held today_
`poll_average_low` | The lower bound of the uncertainty interval for the estimated _x party_ share of the national two-party vote _if the election were held today_
`poll_average_mean` | The average estimated _x party_ share of the national two-party vote _if the election were held today_


*`national_ec_popvote_topline.csv`*: A file containing information about the topline electoral college and popular vote predictions for the latest day the model ran.

Column | Description
--- | ---
`mean_dem_ev` | The average projected Democratic number of electoral votes on election day in our simulations
`median_dem_ev` | The median projected Democratic number of electoral votes on election day in our simulations
`mode_dem_ev` | The modal projected Democratic number of electoral votes on election day in our simulations
`upper_90_dem_ev` | The upper bound of the 95% uncertainty interval for the possible Democratic number of electoral votes on election day in our simulations
`lower_90_dem_ev` | The lower bound of the 95% uncertainty interval for the possible Democratic number of electoral votes on election day in our simulations
`lower_60_dem_ev` | The lower bound of the 60% uncertainty interval for the possible Democratic number of electoral votes on election day in our simulations
`lower_60_dem_ev` | The lower bound of the 60% uncertainty interval for the possible Democratic number of electoral votes on election day in our simulations
`dem_win_prob` | The probability of the Democratic candidate winning 270 or more electoral votes
`rep_win_prob` | The probability of the Republican candidate winning 270 or more electoral votes
`mean_dem_vote` | The average projected share of the national two-party vote going to the Democratic candidate on election day
`median_dem_vote` | The median projected share of the national two-party vote going to the Democratic candidate on election day
`mode_dem_vote` | The modal projected share of the national two-party vote going to the Democratic candidate on election day
`upper_90_dem_vote` | The upper bound of the 95% uncertainty interval for the possible Democratic share of the two-party vote on election day
`lower_90_dem_vote` | The lower bound of the 95% uncertainty interval for the possible Democratic share of the two-party vote on election day
`upper_60_dem_vote` | The upper bound of the 60% uncertainty interval for the possible Democratic share of the two-party vote on election day
`lower_60_dem_vote` | The lower bound of the 60% uncertainty interval for the possible Democratic share of the two-party vote on election day
`dem_vote_win_prob` | The probability of the Democratic candidate winning the two-party popular vote
`rep_vote_win_prob` | The probability of the Republican candidate winning the two-party popular vote
`dem_popvote_dem_ec` | The probability of the Democratic candidate winning the popular vote and winning the electoral college
`dem_popvote_rep_ec` | The probability of the Democratic candidate winning the popular vote and losing the electoral college
`rep_popvote_rep_ec` | The probability of the Republican candidate winning the popular vote and winning the electoral college
`rep_popvote_dem_ec` | The probability of the Republican candidate winning the popular vote and losing the electoral college
`date` | The date this forecast was made on
`dem_poll_average_low` | The lower bound of the uncertainty interval for the estimated Democratic share of the national two-party vote _if the election were held today_
`dem_poll_average_high` | The upper bound of the uncertainty interval for the estimated Democratic
share of the national two-party vote _if the election were held today_
`dem_poll_average_mean` | The average estimated Democratic share of the national two-party vote _if the election were held today_"


*`electoral_college_votes_over_time.csv`*: A file containing the model's projected Democratic and Republican estimated electoral-vote tallies for each day the model ran so far.

Column | Description
--- | ---
`date` | The date of the model run that produced the row's predictions
`party` | Which party's electoral vote tally is in this row of data
`lower_95_ev` | The lower bound of the 95% uncertainty interval for the possible _x party_ number of electoral votes on election day in our simulations
`lower_60_ev` | The lower bound of the 60% uncertainty interval for the possible _x party_ number of electoral votes on election day in our simulations
`median_ev` | The median of the estimated possible electoral-vote outcomes for _x party_
`upper_60_ev` | The upper bound of the 60% uncertainty interval for the possible _x party_ number of electoral votes on election day in our simulations
`upper_95_ev` | The upper bound of the 95% uncertainty interval for the possible _x party_ number of electoral votes on election day in our simulations


*`electoral_college_simulations.csv`*: A file containing our model's most recent simulations for what could happen on election day.

Column | Description
--- | ---
`draw` | The simulation number
`dem_ev` | The number of votes the Democratic candidate wins in this simulation
`natl_pop_vote` | The share of the national two-party popular vote the Democratic candidate wins in this simulation
`AK....WY` | The share of the state-level two-party popular vote the Democratic candidate wins in this simulation, for each state


*`electoral_college_probability_over_time.csv`*: A file containing our model's estimated electoral-college win probabilities for each candidate for each day the model has run so far.

Column | Description
--- | ---
`date` | The date of the model run
`party` | Which party's electoral college win probability is in this row
`win_prob` | The chance that _x party_ wins the electoral college.


*`chance_casting_decisive_vote.csv`*: A file containing a record for each state of how likely a voter in that state is to tip the outcome of the election. Not used in the forecast, but generated for [this piece](https://www.economist.com/graphic-detail/2020/08/15/how-americas-electoral-college-favours-white-voters) about the electoral college.


# Licence

This software is published by _[The Economist](https://www.economist.com)_ under the [MIT licence](https://opensource.org/licenses/MIT). The data generated by _The Economist_ are available under the [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/).

The licences include only the data and the software authored by _The Economist_, and do not cover any _Economist_ content or third-party data or content made available using the software. More information about licensing, syndication and the copyright of _Economist_ content can be found [here](https://www.economist.com/rights/).

