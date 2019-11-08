# Football

This project is about finding who was the best midfielder in liverpool's 2018/19 season. 
These are the below codes used in excel file to find the insights


How many big chances are created by Jordan Henderson/Gini Widjnaldum/Naby Keita/Fabinho?

select count(big_chances_created) from gw
where big_chances_created !=0
select count(big_chances_created) from Gini
where big_chances_created !=0
select count(big_chances_created) from Naby
where big_chances_created !=0
select count(big_chances_created) from Fabinho
where big_chances_created !=0
select count(big_chances_created) from milner
where big_chances_created !=0

How many passes completed by Jordan Henderson/Gini Widjnaldum/Naby Keita/Fabinho?

select sum(cast(completed_passes AS INT))total_completed_passes_Jordan, SUM(cast(minutes AS INT))total_minutes_Jordan, 
round(cast(sum(cast(completed_passes AS Float))/SUM(cast(minutes AS INT)) AS Float),2)'Pass_Minute_Ratio_Jordan' FROM gw 
select sum(cast(completed_passes AS INT))total_completed_passes_Naby, SUM(cast(minutes AS INT))total_minutes_Naby, 
round(cast(sum(cast(completed_passes AS Float))/SUM(cast(minutes AS INT)) AS Float),2)'Pass_Minute_Ratio_Naby' FROM naby 
select sum(cast(completed_passes AS INT))total_completed_passes_Gini, SUM(cast(minutes AS INT))total_minutes_Gini, 
round(cast(sum(cast(completed_passes AS Float))/SUM(cast(minutes AS INT)) AS Float),2)'Pass_Minute_Ratio_Gini' FROM gini
select sum(cast(completed_passes AS INT))total_completed_passes_Fab, SUM(cast(minutes AS INT))total_minutes_Fab, 
round(cast(sum(cast(completed_passes AS Float))/SUM(cast(minutes AS INT)) AS Float),2)'Pass_Minute_Ratio_Fab' FROM Fabinho
select sum(cast(completed_passes AS INT))total_completed_passes_Mil, SUM(cast(minutes AS INT))total_minutes_Mil, 
round(cast(sum(cast(completed_passes AS Float))/SUM(cast(minutes AS INT)) AS Float),2)'Pass_Minute_Ratio_mil' FROM milner


How many erros leading to goal/goal attempt did Jordan Henderson/Gini Widjnaldum/Naby Keita/Fabinho make?

select sum(cast(errors_leading_to_goal_attempt as INT)) total_erors_goal_attempt_jordan from gw
select sum(cast(errors_leading_to_goal_attempt as INT)) total_erors_goal_attempt_naby from naby
select sum(cast(errors_leading_to_goal_attempt as INT)) total_erors_goal_attempt_gini from gini
select sum(cast(errors_leading_to_goal_attempt as INT)) total_erors_goal_attempt_fab from Fabinho
select sum(cast(errors_leading_to_goal_attempt as INT)) total_erors_goal_attempt_fab from milner


How many big chances are missed by Jordan Henderson/Gini Widjnaldum/Naby Keita/Fabinho?

select sum(cast(big_chances_missed as INT)) big_chances_missed_jordan from gw
select sum(cast(big_chances_missed as INT))big_chances_missed_gini from Gini
select sum(cast(big_chances_missed as INT)) big_chances_missed_naby from Naby
select sum(cast(big_chances_missed as INT))big_chances_missed_fab from Fabinho
select sum(cast(big_chances_missed as INT))big_chances_missed_fab from milner


How many key passes/minute are given by Jordan Henderson/Gini Widjnaldum/Naby Keita/Fabinho?

select sum(cast(key_passes AS INT))total_key_passes_Jordan, SUM(cast(minutes AS INT))total_minutes_Jordan, 
round(cast(sum(cast(key_passes AS Float))/SUM(cast(minutes AS INT)) AS Float),3)'Pass_Minute_Ratio_Jordan' FROM gw 
select sum(cast(key_passes AS INT))total_key_passes_Naby, SUM(cast(minutes AS INT))total_minutes_Naby, 
round(cast(sum(cast(key_passes AS Float))/SUM(cast(minutes AS INT)) AS Float),3)'Pass_Minute_Ratio_Naby' FROM naby 
select sum(cast(key_passes AS INT))total_key_passes_Gini, SUM(cast(minutes AS INT))total_minutes_Gini, 
round(cast(sum(cast(key_passes AS Float))/SUM(cast(minutes AS INT)) AS Float),3)'Pass_Minute_Ratio_Gini' FROM gini
select sum(cast(key_passes AS INT))total_key_passes_Fab, SUM(cast(minutes AS INT))total_minutes_Fab, 
round(cast(sum(cast(key_passes AS Float))/SUM(cast(minutes AS INT)) AS Float),3)'Pass_Minute_Ratio_Fab' FROM Fabinho
select sum(cast(key_passes AS INT))total_key_passes_Mil, SUM(cast(minutes AS INT))total_minutes_Mil, 
round(cast(sum(cast(key_passes AS Float))/SUM(cast(minutes AS INT)) AS Float),3)'Pass_Minute_Ratio_Fab' FROM milner


Who was the best defensively among Jordan Henderson/Gini Widjnaldum/Naby Keita/Fabinho?

select sum(cast(clearances_blocks_interceptions AS INT))total_blocks_Jordan, SUM(cast(minutes AS INT))total_minutes_Jordan, 
round(cast(sum(cast(clearances_blocks_interceptions AS Float))/SUM(cast(minutes AS INT)) AS Float),3)'Blocks_Per_Minute_Ratio_Jordan' FROM gw 
select sum(cast(clearances_blocks_interceptions AS INT))total_blocks_Naby, SUM(cast(minutes AS INT))total_minutes_Naby, 
round(cast(sum(cast(clearances_blocks_interceptions AS Float))/SUM(cast(minutes AS INT)) AS Float),3)'Blocks_Per_Minute_Ratio_Naby' FROM naby 
select sum(cast(clearances_blocks_interceptions AS INT))total_blocks_Gini, SUM(cast(minutes AS INT))total_minutes_Gini, 
round(cast(sum(cast(clearances_blocks_interceptions AS Float))/SUM(cast(minutes AS INT)) AS Float),3)'Blocks_Per_Minute_Ratio_Gini' FROM gini
select sum(cast(clearances_blocks_interceptions AS INT))total_blocks_Fab, SUM(cast(minutes AS INT))total_minutes_Fab, 
round(cast(sum(cast(clearances_blocks_interceptions AS Float))/SUM(cast(minutes AS INT)) AS Float),3)'Blocks_Per_Minute_Ratio_Fab' FROM Fabinho
select sum(cast(clearances_blocks_interceptions AS INT))total_blocks_mil, SUM(cast(minutes AS INT))total_minutes_mil, 
round(cast(sum(cast(clearances_blocks_interceptions AS Float))/SUM(cast(minutes AS INT)) AS Float),3)'Blocks_Per_Minute_Ratio_Fab' FROM milner


Who was the best in recovering the ball by Jordan Henderson/Gini Widjnaldum/Naby Keita/Fabinho?

select sum(cast(recoveries AS INT))total_recoveries_Jordan, SUM(cast(minutes AS INT))total_minutes_Jordan, 
round(cast(sum(cast(recoveries AS Float))/SUM(cast(minutes AS INT)) AS Float),3)'recoveries_Per_Minute_Ratio_Jordan' FROM gw 
select sum(cast(recoveries AS INT))total_recoveries_Naby, SUM(cast(minutes AS INT))total_minutes_Naby, 
round(cast(sum(cast(recoveries AS Float))/SUM(cast(minutes AS INT)) AS Float),3)'recoveries_Per_Minute_Ratio_Naby' FROM naby 
select sum(cast(recoveries AS INT))total_recoveries_Gini, SUM(cast(minutes AS INT))total_minutes_Gini, 
round(cast(sum(cast(recoveries AS Float))/SUM(cast(minutes AS INT)) AS Float),3)'recoveries_Per_Minute_Ratio_Gini' FROM gini
select sum(cast(recoveries AS INT))total_recoveries_fab, SUM(cast(minutes AS INT))total_minutes_Fab, 
round(cast(sum(cast(recoveries AS Float))/SUM(cast(minutes AS INT)) AS Float),3)'recoveries_Per_Minute_Ratio_Fab' FROM Fabinho
select sum(cast(recoveries AS INT))total_recoveries_mil, SUM(cast(minutes AS INT))total_minutes_mil, 
round(cast(sum(cast(recoveries AS Float))/SUM(cast(minutes AS INT)) AS Float),3)'recoveries_Per_Minute_Ratio_mil' FROM milner

Who had the most influence on the game per the minutes played among Jordan Henderson/Gini Widjnaldum/Naby Keita/Fabinho?

select sum(cast(influence AS Float))total_influence_Jordan, SUM(cast(minutes AS Float))total_minutes_Jordan, 
round(cast(sum(cast(influence  AS Float))/SUM(cast(minutes AS Float)) AS Float),3)'influence_Jordan' FROM gw 
select sum(cast(influence  AS Float))total_influence_Naby, SUM(cast(minutes AS Float))total_minutes_Naby, 
round(cast(sum(cast(influence  AS Float))/SUM(cast(minutes AS Float)) AS Float),3)'influence_Naby' FROM naby 
select sum(cast(influence  AS Float))total_influence_Gini, SUM(cast(minutes AS Float))total_minutes_Gini, 
round(cast(sum(cast(influence  AS Float))/SUM(cast(minutes AS Float)) AS Float),3)'influence_Gini' FROM gini
select sum(cast(influence  AS Float))total_influence_Fab, SUM(cast(minutes AS Float))total_minutes_Fab, 
round(cast(sum(cast(influence  AS Float))/SUM(cast(minutes AS Float)) AS Float),3)'influence_Fab' FROM Fabinho
select sum(cast(influence  AS Float))total_influence_mil, SUM(cast(minutes AS Float))total_minutes_mil, 
round(cast(sum(cast(influence  AS Float))/SUM(cast(minutes AS Float)) AS Float),3)'influence_Fab' FROM milner


Who had the highest ICT index on the game among Jordan Henderson/Gini Widjnaldum/Naby Keita/Fabinho?

select sum(cast(ict_index AS Float))total_ict_index_Jordan, SUM(cast(minutes AS Float))total_minutes_Jordan, 
round(cast(sum(cast(ict_index  AS Float))/SUM(cast(minutes AS Float)) AS Float),3)'ict_index_Jordan' FROM gw 
select sum(cast(ict_index  AS Float))total_ict_index_Naby, SUM(cast(minutes AS Float))total_minutes_Naby, 
round(cast(sum(cast(ict_index  AS Float))/SUM(cast(minutes AS Float)) AS Float),3)'ict_index_Naby' FROM naby 
select sum(cast(ict_index  AS Float))total_ict_index_Gini, SUM(cast(minutes AS Float))total_minutes_Gini, 
round(cast(sum(cast(ict_index  AS Float))/SUM(cast(minutes AS Float)) AS Float),3)'ict_index_Gini' FROM gini
select sum(cast(ict_index  AS Float))total_ict_index_Fab, SUM(cast(minutes AS Float))total_minutes_Fab, 
round(cast(sum(cast(ict_index  AS Float))/SUM(cast(minutes AS Float)) AS Float),3)'ict_index_Fab' FROM Fabinho
select sum(cast(ict_index  AS Float))total_ict_index_Fab, SUM(cast(minutes AS Float))total_minutes_mil, 
round(cast(sum(cast(ict_index  AS Float))/SUM(cast(minutes AS Float)) AS Float),3)'ict_index_Fab' FROM milner

Who had the most tackles per minute among Jordan Henderson/Gini Widjnaldum/Naby Keita/Fabinho?

select sum(cast(tackles AS Float))total_tackles_Jordan, SUM(cast(minutes AS Float))total_minutes_Jordan, 
round(cast(sum(cast(tackles  AS Float))/SUM(cast(minutes AS Float)) AS Float),3)'tackles_Jordan' FROM gw 
select sum(cast(tackles  AS Float))total_tackles_Naby, SUM(cast(minutes AS Float))total_minutes_Naby, 
round(cast(sum(cast(tackles  AS Float))/SUM(cast(minutes AS Float)) AS Float),3)'tackles_Naby' FROM naby 
select sum(cast(tackles  AS Float))total_tackles_Gini, SUM(cast(minutes AS Float))total_minutes_Gini, 
round(cast(sum(cast(tackles  AS Float))/SUM(cast(minutes AS Float)) AS Float),3)'tackles_Gini' FROM gini
select sum(cast(tackles  AS Float))total_tackles_Fab, SUM(cast(minutes AS Float))total_minutes_Fab, 
round(cast(sum(cast(tackles  AS Float))/SUM(cast(minutes AS Float)) AS Float),3)'tackles_Fab' FROM Fabinho
select sum(cast(tackles  AS Float))total_tackles_mil, SUM(cast(minutes AS Float))total_minutes_mil, 
round(cast(sum(cast(tackles  AS Float))/SUM(cast(minutes AS Float)) AS Float),3)'tackles_Fab' FROM milner

