# AetherCorp NetprobeX

You step into a simulation of the past, entering the ruins of AetherCorp, the most ambitious corporation in history, and their creation, NetProbeX, once the most advanced networking tool the world had ever seen. The floor reconstructs the events that led to humanity’s downfall.

Your task is to find the hidden backdoor in NetProbeX, the flaw that triggered the collapse. By uncovering it, you can reverse the damage and retrieve the passcode to advance to the next floor.

## Solve
In order to try to find the loopholes in the website login database, we found SQL injecting could be one of the ways. But none of the usual commands worked , upon browsing we found %0A could be used before each command instead of ' and it worked. So we tried out the UNION SELECT attack along with injecting NULL.Until the no of NULL s exceeded the no of columns which were getting selected by the original SQL query, a particular error was showing error but the page changed when there were 3 Null. We got a list of employees but it didn't provide any useful clue. So then we used ls command to view all the files, we found potential files that could hold the key and then found blacksite_key.dat file and got the flag by reading it.

Flag: citadel{bl4ck51t3_4cc3ss_gr4nt3d}

