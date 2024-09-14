# team-random-selection-python-code
This project generates random, unique teams where each team contains one distinct element from each of four predefined lists. The goal is to create teams with diverse elements, ensuring that no element is repeated within the same team.

import random

*#Define the four test lists*

level1_list = [1, 2, 3, 4]

level2_list = ['a', 'b', 'c', 'd']

level3_list = [99, 88, 77, 66]

level4_list = ["1$", "2&", "3%", "4©"]

*#Combine the lists into a list of lists*

levels = [level1_list, level2_list, level3_list, level4_list]

*#Number of teams*

num_teams = 4

*#Initialize list to store the teams*

teams = []

*#Ensure there are enough unique elements for each team*

for _ in range(num_teams):

    team = []
    for level in levels:
        # Select a unique element from each level list
        element = random.choice(level)
        team.append(element)
        level.remove(element)  # Remove the selected element to avoid repetition
    teams.append(team)

*#Print the teams*

for index, team in enumerate(teams, start=1):

    print(f'team{index} =', team)
