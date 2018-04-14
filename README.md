# Atari Reinforcement Learning Leaderboard

This is a leaderboard comparing world record human performance to state of the art
reinforcement learning algorithms across Atari games.

I decided to put this together after noticing two things:

- Many Atari RL papers are selective in what algorithms they compare to.
- Top human scores are orders of magnitude better than the benchmarks
reported in Dueling DQN paper.

| Game | Top Human Score | Top Machine Score | Best | Best Machine | Learning Type |
| --- | --- | --- | --- | --- | --- |
| Alien | 255265 | 9491 | Human | Rainbow | Q-gradient |
| Amidar | 104159 | 5131 | Human | Rainbow | Q-gradient |
| Assault | 8647 | 14497 | Machine | A3C | Policy-gradient |
| Asterix | 1000000 | 428200 | Human | Rainbow | Q-gradient |
| Asteroids | 10004100 | 5093 | Human | A3C | Policy-gradient |
| Atlantis | 10604840 | 2311815 | Human | PPO | Policy-gradient |
| Bank Heist | 82058 | 1611 | Human | Dueling DDQN | Q-gradient |
| Battle Zone | 1545000 | 62010 | Human | Rainbow | Q-gradient |
| Beam Rider | 999999 | 26172 | Human | Prioritized DDQN | Q-gradient |
| Berzerk | 1057940 | 2545 | Human | Rainbow | Q-gradient |
| Bowling | 300 | 135 | Human | HyperNEAT | Genetic Policy |
| Boxing | 102 | 99 | Human | Rainbow, ACER | Q,Policy-gradient |
| Breakout | 864 | 766 | Human | A3C | Policy-gradient |
| Centipede | 1301709 | 25275 | Human | HyperNEAT | Genetic Policy |
| Chopper Command | 999999 | 16654 | Human | Rainbow | Q-gradient |
| Crazy Climber | 219900 | 183135 | Human | Prioritized DDQN | Q-gradient |
| Defender | 5443150 | 233021 | Human | A3C | Policy-gradient |
| Demon Attack | 1556345 | 115201 | Human | A3C | Policy-gradient |
| Enduro | 118000 | 2260 | Human | Distribution DQN | Q-gradient |
| Fishing Derby | 71 | 46 | Human | Dueling DDQN | Q-gradient |
| Freeway | 38 | 34 | Human | Rainbow | Q-gradient |
| Frostbite | 1832730 | 9590 | Human | Rainbow | Q-gradient |
| Gopher | 829440 | 70354 | Human | Rainbow | Q-gradient |
| Gravitar | 999950 | 1419 | Human | Rainbow | Q-gradient |
| HERO | 1000000 | 55887 | Human | Rainbow | Q-gradient |
| Ice Hockey | 36 | 10 | Human | HyperNEAT | Genetic Policy |
| Kangaroo | 1424600 | 14854 | Human | Dueling DDQN | Q-gradient |
| Krull | 1245900 | 12601 | Human | HyperNEAT | Genetic Policy |
| Kung Fu Master | 1000000 | 52181 | Human | Rainbow | Q-gradient |
| Montezuma Revenge | 1219200 | 384 | Human | Rainbow | Q-gradient |
| Ms Pacman | 2654680 | 6283 | Human | Dueling DDQN | Q-gradient |
| Name This Game | 25220 | 13439 | Human | Prioritized DDQN | Q-gradient |
| Phoenix | 4014440 | 108528 | Human | Rainbow | Q-gradient |
| Pitfall | 114000 | 0 | Human | Several | Q-gradient |
| Pong | 21 | 21 | Draw | Several | Several |
| Private Eye | 118000 | 15172 | Human | Distribution DQN | Q-gradient |
| Qbert | 2400000 | 33817 | Human | Rainbow | Q-gradient |
| Road Runner | 2038100 | 73949 | Human | A3C | Policy-gradient |
| Robotank | 76 | 65 | Human | Dueling DDQN | Q-gradient |
| Seaquest | 999999 | 50254 | Human | Dueling DDQN | Q-gradient |
| Skiing | -3272 | -6522 | Human | Vanilla GA | Genetic Policy |
| Space Invaders | 621535 | 23864 | Human | A3C | Policy-gradient |
| Star Gunner | 69400 | 164766 | Machine | A3C | Policy-gradient |
| Time Pilot | 112100 | 27202 | Human | A3C | Policy-gradient |
| Tutankham | 5384 | 280 | Human | ACER | Policy-gradient |
| Venture | 913200 | 1107 | Human | Distribution DQN | Q-gradient |
| Video Pinball | 35197952 | 533936 | Human | Rainbow | Q-gradient |
| Wizard of Wor | 864500 | 18082 | Human | A3C | Policy-gradient |
| Yars Revenge | 15000105 | 102557 | Human | Rainbow | Q-gradient |
| Zaxxon | 772400 | 24622 | Human | A3C | Q-gradient |


## Win Counts

It will be surprising to some that humans win by a long way here. Machines win on two and
draw on one. The Dueling DDQN papers report superhuman performance, but this is compared
to casual baseline. An expert comparison, like in chess and go, is more appropriate, since
these algorithms play 1000s of games each.

Excluding humans, per-algorithm win count are as follows (two way ties friendly, three or
more unfriendly):

| Algorithm | Type | Wins |
| --- | --- | --- |
| Rainbow | Q-gradient | 18 |
| A3C (FF and LSTM) | Policy-gradient | 11 |
| Dueling DDQN | Q-gradient | 6 |
| HyperNEAT | Genetic Policy | 4 |
| Distribution DQN | Q-gradient | 3 |
| Prioritized DDQN | Q-gradient | 3 |
| ACER | Policy-gradient | 2 |
| PPO | Policy-gradient | 1 |
| Vanilla GA | Genetic Policy | 1 |
| Noisy DQN | Q-gradient | 0 |
| Vanilla ES | Genetic Policy | 0 |


## Methodology

Reference papers vary in:

- Start type (no-op, random-op, human-op)
- Number of test trials (from 30-200)

I take the approach here of favouring no-op starts over random ones (they usually have
higher scores anyway), and treating all sample sizes equally.

Games for which there exists no human WR are excluded. I exclude A3C since those
results are only available with human op starts, and A2C covers the general method.


## References

- [Human](www.twingalaxies.com)
- [A2C](https://arxiv.org/pdf/1707.06347.pdf)
- [ACER](https://arxiv.org/pdf/1707.06347.pdf)
- [Distribution DQN](https://arxiv.org/pdf/1710.02298.pdf)
- [Dueling DDQN](https://arxiv.org/pdf/1710.02298.pdf)
- [HyperNeat](https://arxiv.org/pdf/1703.03864.pdf), also checked against original paper
- [Rainbow](https://arxiv.org/pdf/1710.02298.pdf)
- [Prioritized DDQN](https://arxiv.org/pdf/1710.02298.pdf)
- [Proximal Policy Optimization](https://arxiv.org/pdf/1707.06347.pdf)
- [Vanilla Evolution Strategies](https://arxiv.org/pdf/1703.03864.pdf)
- [Vanilla Genetic Algorithm](https://arxiv.org/pdf/1712.06567.pdf)
