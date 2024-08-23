Reminder app for personal us e, taken from the erlang for a great good.
The app will spawn processes for each reminder.

run copiled code with 
erl -pa ebin/

start create and listen

evserv:start().
evserv:subscribe("Bday", "Party", {{Y,M,D},{H,M,S}}).
evserve:listen(5000).

call supervisor

SupPid = sup:start(evserv,[]).
whereis(evserv).
exit(SupPid, shutdown).
