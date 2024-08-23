Reminder app for personal us e, taken from the erlang for a great good.
The app will spawn processes for each reminder.

run copiled code with 
erl -pa ebin/

api

evserv:start().
evserv:subscribe("Bday", "Party", {{Y,M,D},{H,M,S}}).
evserve:listen(5000).

