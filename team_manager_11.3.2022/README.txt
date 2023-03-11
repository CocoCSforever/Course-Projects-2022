Summary:
    The project enables to create a coaching and management system for a dodgeball team. The system is intended for use by a manager/coach of the team. 
    The system enables the user to set the name of the team, check on the status of the team, and to manage the players on the team in various ways. 
    Dodgeball positions include catcher, corner, sniper, and thrower.
    
    
Implementation:
    The program introduces itself and asks you what you want to do. The options are 
        set team name
        show roster
        add player
        cut player
        check position is filled
        send player to bench
        get player from bench
        show bench, and done
    Any other command or mis-typed command will get the "I didn't understand that command" response.
    Whoever has been resting longest on the bench (i.e., whoever was sent to the bench earliest) will always be the first player returned from the bench. When a player is benched, that player should still remain on the team roster, even while they are on the bench.
    When we cut a player, we should also check whether he's on the bench and cut him from the bench. Should not allow a benched player to pop back onto the team after having been cut.


Run team_manager.py
// ----OUTPUT---- //
What do you want to do?
add player
What's the player's name?
Garcia
What's Garcia's number?
15
What's Garcia's position?
catcher
Added Garcia to Anonymous Team
What do you want to do?
set team name
What do you want to name the team?
Seattle Scorpions
What do you want to do?
add player
What's the player's name?
Wiggins
What's Wiggins's number?
55
What's Wiggins's position?
corner
Added Wiggins to Seattle Scorpions
What do you want to do?
add player
What's the player's name?
McCann
What's McCann's number?
99
What's McCann's position?
sniper
Added McCann to Seattle Scorpions
What do you want to do?
show roster
The lineup for Seattle Scorpions is:
15       Garcia          catcher
55       Wiggins         corner
99       McCann          sniper


What do you want to do?
check position is filled
What position are you checking for?
thrower
No, the thrower position is not filled


What do you want to do?
send player to bench
Who do you want to send to the bench?
McCann
What do you want to do?
send player to bench
Who do you want to send to the bench?
Garcia
What do you want to do?
show bench
The bench currently includes:
Garcia
McCann
What do you want to do?
get player from bench
Got McCann from bench
What do you want to do?
get player from bench
Got Garcia from bench
What do you want to do?
get player from bench
The bench is empty.


What do you want to do?
cut player
Who do you want to cut?
McCann
What do you want to do?
show roster
The lineup for Seattle Scorpions is:
15       Garcia          catcher
55       Wiggins         corner


What do you want to do?
done
Shutting down team manager