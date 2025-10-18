> [!WARNING]
> DEPRECATED! i no longer will longer Maintain this Version of this AC6-Music Exploit, you can find the new version [here](https://github.com/Roblox-HttpSpy/AC6-Music-Exploit/), Reason for depreciation is because this one had messy code and a bad UI so i decided to Recreate it entirely, but feel free to keep using this one...

---

# FE AC6-MUSIC-EXPLOIT
(or just Ac6-Exploit for short)
Is a **Roblox-LUAU** Script, more specifically a **LocalScript** meant for **Executors**~
(no need to add extra details-)

# What Does it do?
the **Ac6-Exploit** Is able to Play music **Server-Sided** (meaning other clients will be able to hear it)...

# How Does it work?
easy & pretty simple... it abuses a [RemoteEvent](https://create.roblox.com/docs/reference/engine/classes/RemoteEvent)-
a specific [RemoteEvent](https://create.roblox.com/docs/reference/engine/classes/RemoteEvent) belonging to the **AC6** Script
(short story the AC6 is a roblox Luau script used by developers of said games `mostly Owners of Roblox car games` to make there car Realistic by adding stuff like advanced car Sound system and lightning),
and in the AC6 it has a lil Remote nammed **AC6_FE_Sounds**, its mostly ment for creating realistic Car Sound noises, BUT a exploit been found that "tricks" the server into creating a New **Audio** Instance inside the games folders (like said Services [Workspace](https://create.roblox.com/docs/reference/engine/classes/Workspace)/[Lighting](https://create.roblox.com/docs/reference/engine/classes/Lighting)/[ReplicatedFirst](https://create.roblox.com/docs/reference/engine/classes/ReplicatedFirst), and more...)
on how it "tricks the server" these are the augments that are passed between the client and server (or for this case bieng sent from you to server)
```lua
local args = {
[1] = "newSound",
[2] = Name,
[3] = Workspace,
[4] = rbxassest://,
[5] = 0,
[6] = 1,
[7] = true
}
```
total of **7** Aurgements!
lets explain what all they do

**[1]** = NewSound (this is the "command" to create a NewSound)

**[2]** is what will the name of the audio, (not useful that much)

**[3]** is where ill be parented to

**[4]** the music ID

**[5]** the pitch of the audio

**[6]** the volume of the audio

**[7]** makes the audio looped or un 
looped (true = looped / false = unlooped)
all send to the server,
After all that it sends
```lua
FireServer("playSound", "Audios Name")
```
to play to play the sound and thats it that simple,

# NOTES
- Not all games have a vulnerable AC6, the script may flag there's a AC6 but you wont be able to play music on it

- Some games do have vulnerable AC6 but simply Renamed the remote,
if you a person that knows what there doing, you should: Execute [RemoteSpy](https://github.com/78n/SimpleSpy) and get on a car, if a remote is bieng fired with similar args of AC6 or atleast has the "PlaySound" or a rbxassest:// in one of the args, on AC6 Source replace "AC6_FE_Sounds" with the name of the suspected Remote Name and ReExecute..

**ALSO** if you want to ask something or whatever open a **discussion** by clicking the 3 dots **...** on this repository, DO NOT open a issue if a game has ac6 but nothing is playing..


# RequireMents.
the Script can Run in low/Weak Executors including [Solara](https://getsolara.dev/) and [Xeno](https://www.xeno.onl//) even [JJExploits](https://wearedevs.net/d/JJSploit) (i think)...

_it may be able to even run inside roblox studio but will need modifications like changing coregui to playerGui and remove loadstrings and ect_

you can find verified safe executors here: https://pulsery.net/
or every known executor here:
https://voxlis.net/roblox/

_(not mine website btw, i didnt get paid to promote them just a cool website with all verified links to official Executor sites)_

### Misc.

[![License: MIT](https://img.shields.io/badge/License%3A-MIT-green?style=plastic)](https://github.com/Roblox-HttpSpy/my-Garbage/blob/main/LICENSE)

[![Scripting Language: LUAU](https://img.shields.io/badge/Scripting%20Language%3A-LUAU-blue?style=plastic)](https://github.com/luau-lang/luau)
