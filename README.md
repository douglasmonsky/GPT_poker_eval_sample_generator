# GPT_poker_eval_sample_generator

Python script that simulates and evaluates Texas Hold'em poker hands to calculate each player's winning and tie probabilities. The script generates hands with varying numbers of players (ranging from 2 to 9) and community cards (3, 4, or 5 cards). The resulting data is formatted as JSON Lines, which are carefully structured to create an effective prompt for GPT-based evaluation.

Each example hand consists of an "input" key containing a list of two dictionaries:

1.The first dictionary has a "role" key with the value "system" and a "content" key providing the task description. In this context, the task is to identify the player with the highest winning probability in a given Texas Hold'em hand.
2.The second dictionary has a "role" key with the value "user" and a "content" key presenting the hand details, which include each player's hole cards and the community cards. For example:
• Player 1 Hole: (2h, 4s)
• Player 2 Hole: (Qh, Jc)
• Community cards: 5d, 9s, Kc
The "ideal" key provides the index (1-based) of the player with the highest probability of winning the hand. In this example, the value is "2", indicating that Player 2 has the greatest chance of winning.
