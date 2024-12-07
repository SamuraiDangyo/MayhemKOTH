![logo](https://github.com/user-attachments/assets/4b9cc739-fc1f-4bd7-8746-c4cc5a9dfbcd)

# MayhemKOTH

Linux Xboard KOTH Chess Engine

## Supported commands

```
MayhemKOTH. Linux Xboard KOTH Chess Engine. Written in C++20 language

Supported commands:

help
  This help

ping [N]
  Responded by 'pong N'

protover 2]
  Only Xboard protocol 2 supported

level [movestogo] [time] [inc]
  Setup time control

random
  Add random element to eval

time [N]
  Setup time left for the engine

force
  Setup force mode. Act only after 'go' command

new
  Setup new game

list
  Show list of moves

play [ms = 5000]
  Watch a game

analyze
  Analyze position

undo
  Go back in history

.
  Respond ASAP

?
  Move ASAP

option
  Setup option in form of 'option hash=256'

variant
  Setup variant

setboard
  Setup board using FEN notation

logo
  Print ASCII art logo

p [fen = startpos]
  Print ASCII art board

perft [depth = 6] [fen = startpos]
  Calculate perft split numbers

bench [depth = 14]
  Show signature of the program

speed [ms = 5000]
  Show speed of the program

exit
  Exit the analyze mode

quit
  Quit the engine ASAP
```

## Tests

```
Score of MayhemKOTH 1.0 vs MayhemKOTH 1.0: 437 - 408 - 155  [0.514] 1000
...      MayhemKOTH 1.0 playing White: 266 - 189 - 45  [0.577] 500
...      MayhemKOTH 1.0 playing Black: 171 - 219 - 110  [0.452] 500
...      White vs Black: 485 - 360 - 155  [0.563] 1000
Elo difference: 10.1 +/- 19.8, LOS: 84.1 %, DrawRatio: 15.5 %
SPRT: llr 0 (0.0%), lbound -inf, ubound inf

Player: MayhemKOTH 1.0
   "Draw by 3-fold repetition": 154
   "Draw by insufficient mating material": 1
   "Loss: Black mates": 43
   "Loss: Black wins with king in the center": 146
   "Loss: White mates": 24
   "Loss: White wins with king in the center": 195
   "Win: Black mates": 34
   "Win: Black wins with king in the center": 137
   "Win: White mates": 47
   "Win: White wins with king in the center": 219
Player: MayhemKOTH 1.0
   "Draw by 3-fold repetition": 154
   "Draw by insufficient mating material": 1
   "Loss: Black mates": 34
   "Loss: Black wins with king in the center": 137
   "Loss: White mates": 47
   "Loss: White wins with king in the center": 219
   "Win: Black mates": 43
   "Win: Black wins with king in the center": 146
   "Win: White mates": 24
   "Win: White wins with king in the center": 195
Finished match
```

## Sample game

```
[White "MayhemKOTH 1.0"]
[Black "MayhemKOTH 1.0"]
[Result "1-0"]
[TimeControl "60+1"]
[Variant "kingofthehill"]
1. e4 {+0.69/16 3.3s} d5 {-0.68/16 3.3s} 2. exd5 {+0.59/16 3.3s}
e6 {-0.59/15 3.3s} 3. dxe6 {+0.79/16 3.2s} Bxe6 {-0.71/15 3.2s}
4. d4 {+0.99/15 3.1s} Nc6 {-0.96/14 3.1s} 5. Nf3 {+0.91/15 3.0s}
Nf6 {-0.84/13 3.0s} 6. Nc3 {+0.90/14 2.9s} Be7 {-0.85/13 2.9s}
7. Be3 {+0.84/14 2.9s} O-O {-0.96/14 2.9s} 8. h3 {+0.92/13 2.8s}
h6 {-0.84/13 2.8s} 9. a3 {+0.92/15 2.7s} Nd5 {-1.10/14 2.7s}
10. Nxd5 {+1.04/14 2.6s} Bxd5 {-1.20/14 2.6s} 11. c4 {+1.16/15 2.6s}
Bxf3 {-1.11/16 2.6s} 12. gxf3 {+0.76/16 2.5s} Re8 {-0.76/15 2.5s}
13. Be2 {+0.84/14 2.5s} Bh4 {-0.53/15 2.5s} 14. Qd2 {+0.78/15 2.4s}
Qe7 {-0.49/15 2.4s} 15. O-O {+0.67/15 2.4s} Bg5 {-0.72/14 2.4s}
16. d5 {+0.38/17 2.3s} Bxe3 {-0.38/16 2.3s} 17. fxe3 {0.00/16 2.3s}
Qxe3+ {-0.33/16 2.3s} 18. Qxe3 {+0.33/21 2.2s} Rxe3 {-0.45/19 2.2s}
19. dxc6 {+0.27/19 2.2s} Rxe2 {-0.28/18 2.2s} 20. Rf2 {+0.06/18 2.1s}
Re5 {-0.35/18 2.1s} 21. cxb7 {+0.35/17 2.1s} Rb8 {-0.32/18 2.1s}
22. Kg2 {+0.27/15 2.0s} Rg5+ {-0.24/16 2.0s} 23. Kf1 {+0.55/18 2.0s}
Rxb7 {-0.53/16 2.0s} 24. b4 {+0.65/17 2.0s} c5 {-0.39/16 2.0s}
25. Rd2 {+0.63/14 1.9s} Rg3 {-0.69/15 1.9s} 26. Kf2 {+0.92/16 1.9s}
Rxh3 {-0.93/17 1.9s} 27. Rad1 {+1.03/16 1.8s} f5 {-1.09/15 1.8s}
28. Rd7 {+1.35/16 1.8s} Rb8 {-1.40/17 1.8s} 29. Rxa7 {+1.37/15 1.8s}
f4 {-1.43/17 1.8s} 30. Rdd7 {+1.43/17 1.8s} Rh2+ {-1.49/18 1.8s}
31. Kg1 {+1.40/18 1.7s} Ra2 {-1.40/17 1.7s} 32. Rxg7+ {+1.54/17 1.7s}
Kh8 {-1.59/17 1.7s} 33. Rh7+ {+1.59/16 1.7s} Kg8 {-1.59/1 0s}
34. b5 {+1.45/16 1.6s} Rxa3 {-1.27/17 1.7s} 35. Rag7+ {+1.56/17 1.6s}
Kf8 {-1.27/1 0s} 36. Rg4 {+1.75/17 1.6s} Rd8 {-1.77/17 1.7s}
37. Rxf4+ {+2.05/18 1.6s} Kg8 {-2.07/18 1.7s} 38. Rxh6 {+2.07/17 1.6s}
Rd2 {-2.07/16 1.7s} 39. Rg6+ {+2.40/19 1.5s} Kh7 {-2.54/19 1.6s}
40. Rg2 {+2.37/18 1.5s} Rxg2+ {-2.36/17 1.6s} 41. Kxg2 {+2.63/19 1.5s}
Kg6 {-2.63/18 1.6s} 42. Kg3 {+4.80/19 1.5s} Rd3 {-3.77/17 1.6s}
43. Rf8 {+11.92/18 1.5s} Rd4 {-6.47/16 1.5s} 44. b6 {+23.90/16 1.4s}
Kg5 {-104.85/15 1.2s} 45. b7 {+104.85/14 0.24s} Rd1 {-104.85/13 0.21s}
46. b8=Q {+104.85/12 0.057s} Rg1+ {-104.85/11 0.037s}
47. Kf2 {+104.85/10 0.016s} Rf1+ {-104.85/9 0.011s} 48. Kxf1 {+104.85/8 0.003s}
Kg6 {-104.85/7 0.004s} 49. Kf2 {+104.85/5 0.004s} Kh5 {-104.85/6 0.001s}
50. Ke3 {+104.85/3 0s} Kg5 {-104.85/2 0s}
51. Ke4 {+104.85/1 0s, White wins with king in the center} 1-0
```
