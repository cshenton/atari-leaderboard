# Atari Reinforcement Learning Leaderboard

I decided to put this together after noticing two things:

- HyperNEAT, a genetic algorithm predating DQN, still maintains state-of-the-art scores on several games.
- Top human scores are orders of magnitude better than those reported in Dueling DQN paper.

| Game | Top Human Score | Top Machine Score | Best | Best Machine | Learning Type |
| --- | --- | --- | --- | --- | --- |
| Air Raid | ???? |
| Alien | 255265 |
| Amidar | 104159 |
| Assault | 8647 |
| Asterix | 1000000 |
| Asteroids | 10004100 |
| Atlantis | 10604840 |
| Bank Heist | 82058 |
| Battle Zone | 1545000 |
| Beam Rider | 999999 |
| Berzerk | 1057940 |
| Bowling | 300 |
| Boxing | 102s |
| Breakout | 864 |
| Carnival | ??? |
| Centipede | 1301709 |
| Chopper Command | 999999 |
| Crazy Climber | 219900 |
| Defender | 5443150 |
| Demon Attack | 1556345 |
| Double Dunk | ??? |
| Elevator Action | ??? |
| Enduro | 118000 |
| Fishing Derby | 71 |
| Freeway | 38 |
| Frostbite | 1832730 |
| Gopher | 829440 |
| Gravitar | 999950 |
| HERO | 1000000 |
| Ice Hockey | 36 |
| James Bond | 45550 |
| Journey Escape | ??? |
| Kangaroo | 1424600 |
| Krull | 1245900 |
| Kung Fu Master | 1000000 |
| Montezuma Revenge | 1219200 |
| Ms Pacman | 2654680 |
| Name This Game | 25220 |
| Phoenix | 4014440 |
| Pitfall | 114000 |
| Pong | ??? |
| Pooyan | ??? |
| Private Eye | 118000
| Qbert | 2400000 |
| River Raid | 1000000 |
| Road Runner | 2038100 |
| Robotank | 76 |
| Seaquest | 999999 |
| Skiing | -3272 |
| Space Invaders | 621535 |
| Star Gunner | 69400 |
| Tennis | ??? |
| Time Pilot | 112100 |
| Tutankham | ??? |
| Up N Down | 75230 |
| Venture | 913200 |
| Video Pinball | 35197952 |
| Wizard of Wor | 864500 |
| Yars Revenge | 15000105 |
| Zaxxon | 772400 |


## Methodology

There are various numbers of trials used in reference papers, including different
amounts of no-op starts, etc. I take a generous approach here, the best score is
simply the best score averaged over at least a few runs, so the max is taken across
random-op, human-op, and no-op starts for the machine runs.

This is an imperfect method, but it in effect takes the stance that improvements to
start of the art should be substantial enough that the error introduced by this method
should be small in comparison.

All scores are taken from their original papers, which are referenced below, along with
a count of how many games that method is SOA in.

## References

- [Human](www.twingalaxies.com)
- A2C
- A3C
- HyperNEAT
- Rainbow
- ES
