`18/07/25` Added two mods ([Very Many Players](https://modrinth.com/mod/vmp-fabric) and [Packet Fixer](https://modrinth.com/mod/packet-fixer)) to try to help fix connection issues related to chunk packets sent to the client. Didn't appear to work very well at first, then thought that the trouble was with the server warming up to accepting players when it's not already running yet. At first, it was very choppy over ethernet, and a few minutes after i switched to Wi-Fi, the ping test `ping -t 8.8.8.8` showed consistent results and the gameplay was very smooth. It might be a combination of both chunk issues and network issues. I increased the `server.properties` viewdistance back up to 16, but haven't seen if that works well yet.
***
`20/07/25` set the render distance back up to 16; no problems from that so far, might even raise it higher to 20 or 24. MSPT spiked a few times today, mostly when all 3 of us were in different places so no common chunks were loaded, but also in normal situations where all of us were in the same place for some reason. Best I can do is throw more mods at the problem to try to fix it.
***
`24/07/25` Added mods --  
* ImmediatelyFast (client)
* Clumps
* Alternate Current
***
`/attribute f4fd9da9-6482-4235-900c-f3489ad0a66f minecraft:scale base set 0.1`
***
`07/11/25` Look into using Docker for the server? What are the advantages?
https://www.youtube.com/watch?v=eIHiRW4QH6I
https://docker-minecraft-server.readthedocs.io/en/latest/
https://docker-minecraft-server.readthedocs.io/en/latest/types-and-platforms/server-types/fabric/
***
Pillager farm https://www.youtube.com/watch?v=i6yG44CCSm4 
***
1052, -41, -498