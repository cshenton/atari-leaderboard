# Atari Reinforcement Learning Leaderboard

I decided to put this together after noticing two things:

- Most RL papers only report a handful of comparison algorithms, not state of the
art for each game, making true comparisons difficult.
- Top human scores are orders of magnitude better than those reported in Dueling DQN paper.

| Game | Top Human Score | Top Machine Score | Best | Best Machine | Learning Type |
| --- | --- | --- | --- | --- | --- |
| Alien | 255265 | 9491 | Human | Rainbow | Q-gradient |
| Amidar | 104159 | 5131 | Human | Rainbow | Q-gradient |
| Assault | 8647 | 14198 | Machine | Rainbow | Q-gradient |
| Asterix | 1000000 | 428200 | Human | Rainbow | Q-gradient |
| Asteroids | 10004100 | 4814 | Human | Noisy DQN | Q-gradient |
| Atlantis | 10604840 | 2311815 | Human | PPO | Policy-gradient |
| Bank Heist | 82058 | 1611 | Human | Dueling DDQN | Q-gradient |
| Battle Zone | 1545000 | 62010 | Human | Rainbow | Q-gradient |
| Beam Rider | 999999 | 22430 | Human | Prioritized DDQN | Q-gradient |
| Berzerk | 1057940 | 2545 | Human | Rainbow | Q-gradient |
| Bowling | 300 | 74 | Human | Distribution DQN | Q-gradient |
| Boxing | 102 | 99 | Human | Rainbow, ACER | Q,Policy-gradient |
| Breakout | 864 | 612 | Human | Distribution DQN | Q-gradient |
| Centipede | 1301709 | 9015 | Human | Distribution DQN | Q-gradient |
| Chopper Command | 999999 | 16654 | Human | Rainbow | Q-gradient |
| Crazy Climber | 219900 | 183135 | Human | Prioritized DDQN | Q-gradient |
| Defender | 5443150 | 55105 | Human | Rainbow | Q-gradient |
| Demon Attack | 1556345 | 111185 | Human | Rainbow | Q-gradient |
| Enduro | 118000 | 2260 | Human | Distribution DQN | Q-gradient |
| Fishing Derby | 71 | 46 | Human | Dueling DDQN | Q-gradient |
| Freeway | 38 | 34 | Human | Rainbow | Q-gradient |
| Frostbite | 1832730 | 9590 | Human | Rainbow | Q-gradient |
| Gopher | 829440 | 70354 | Human | Rainbow | Q-gradient |
| Gravitar | 999950 | 1419 | Human | Rainbow | Q-gradient |
| HERO | 1000000 | 55887 | Human | Rainbow | Q-gradient |
| Ice Hockey | 36 | 1 | Human | Distribution DQN | Q-gradient |
| Kangaroo | 1424600 | 14854 | Human | Dueling DDQN | Q-gradient |
| Krull | 1245900 | 11451 | Human | Dueling DDQN | Q-gradient |
| Kung Fu Master | 1000000 | 52181 | Human | Rainbow | Q-gradient |
| Montezuma Revenge | 1219200 | 384 | Human | Rainbow | Q-gradient |
| Ms Pacman | 2654680 | 6283 | Human | Dueling DDQN | Q-gradient |
| Name This Game | 25220 | 13439 | Human | Prioritized DDQN | Q-gradient |
| Phoenix | 4014440 | 108528 | Human | Rainbow | Q-gradient |
| Pitfall | 114000 | 0 | Human | Several | Q-gradient |
| Pong | 21 | 21 | Draw | Several | Several |
| Private Eye | 118000 | 15172 | Human | Distribution DQN | Q-gradient |
| Qbert | 2400000 | 33817 | Human | Rainbow | Q-gradient |
| Road Runner | 2038100 | 69524 | Human | Dueling DDQN | Q-gradient |
| Robotank | 76 | 65 | Human | Dueling DDQN | Q-gradient |
| Seaquest | 999999 | 50254 | Human | Dueling DDQN | Q-gradient |
| Skiing | -3272 | -6522 | Human | Vanilla GA | Genetic Policy |
| Space Invaders | 621535 | 18789 | Human | Rainbow | Q-gradient |
| Star Gunner | 69400 | 108528 | Human | Rainbow | Q-gradient |
| Time Pilot | 112100 | 12926 | Human | Rainbow | Q-gradient |
| Tutankham | 5384 | 280 | Human | ACER | Policy-gradient |
| Venture | 913200 | 1107 | Human | Distribution DQN | Q-gradient |
| Video Pinball | 35197952 | 533936 | Human | Rainbow | Q-gradient |
| Wizard of Wor | 864500 | 17862 | Human | Rainbow | Q-gradient |
| Yars Revenge | 15000105 | 102557 | Human | Rainbow | Q-gradient |
| Zaxxon | 772400 | 22209 | Human | Rainbow | Q-gradient |


## Win Count

Human's win by a long way here, so let's exclude them and count SOA games by
algorithm. Two way ties are friendly, any more way ties are not counted at all.

| Algorithm | Type | Wins |
| Rainbow | Q-gradient | 25 |
| Dueling DDQN | Q-gradient | 8 |
| Distribution DQN | Q-gradient | 7 |
| Prioritized DDQN | Q-gradient | 3 |
| ACER | Policy-gradient | 2 |
| PPO | Policy-gradient | 1 |
| Noisy DQN | Q-gradient | 1 |
| Vanilla GA | Genetic Policy | 1 |


## Methodology

There are various numbers of trials used in reference papers, including different
amounts of no-op starts, etc. I take a generous approach here, the best score is
simply the best score averaged over at least a few runs from, in decreasing order of
preference, no-op starts, random-op starts.

This is an imperfect method, but it in effect takes the stance that improvements to
start of the art should be substantial enough that the error introduced by this
method should be small in comparison.

All scores are taken from the papers referenced below, along with a count of how many
games that method is SOA in.

Games for which there exists no human WR are excluded. I exclude A3C since those
results are only available with human op starts, and A2C covers the general method.


## References

- [Human](www.twingalaxies.com)
- [A2C](https://arxiv.org/pdf/1707.06347.pdf)
- [ACER](https://arxiv.org/pdf/1707.06347.pdf)
- [Distribution DQN](https://arxiv.org/pdf/1710.02298.pdf)
- [Dueling DDQN](https://arxiv.org/pdf/1710.02298.pdf)
- [Rainbow](https://arxiv.org/pdf/1710.02298.pdf)
- [Prioritized DDQN](https://arxiv.org/pdf/1710.02298.pdf)
- [Proximal Policy Optimization](https://arxiv.org/pdf/1707.06347.pdf)
- [Vanilla Evolution Strategies](https://arxiv.org/pdf/1703.03864.pdf)
- [Vanilla Genetic Algorithm](https://arxiv.org/pdf/1712.06567.pdf)
