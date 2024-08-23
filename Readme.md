Reminder app for personal us e, taken from the erlang for a great good.
The app will spawn processes for each reminder.

run copiled code with 
erl -pa ebin/

start create and listen

reminder_evserv:start().
reminder_evserv:subscribe("Bday", "Party", {{Y,M,D},{H,M,S}}).
reminder_evserve:listen(5000).

call supervisor

SupPid = reminder_sup:start(evserv,[]).
whereis(reminder_evserv).
exit(SupPid, shutdown).
