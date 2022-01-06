# Train Game
*A requirement engineering project of a train game scenario.*

- Category: Requirement Engineering
- Keyword: 
  - requirement elicitation
  - requirement analysis
  - UML diagrams
  - use case diagrams
  - risk analysis
  - review process
  - inspection checklist
  - requirement tests
  - traceability matrix
- Date: October, 2021

- Content

## Scenario

The scenario involves developing the requirements for a competitive, turn-based two-player game that entails routing passenger trains between different North American cities.
Players are given goals (e.g., “Send a train from Toronto to Cincinnati”) and deploy resources in order achieve these goals as efficiently as possible, thus maximizing the score that is attained.
The player with the highest score after completion of all goals is considered to be the winner.

The game will ultimately have the following capabilities:
- A graphical user interface that shows a map with cities and train routes between these cities. The GUI will also show progress each player is making towards achieving their goals (for example, if a player is sending a train from Boston to Cleveland, and the train is part-way to its destination, this should be shown on the interface in some way).
- The ability to describe a route from one city to another city, via any number of intermediate stops (other cities) or junctions (points where train tracks intersect).
- The ability to observe unsafe situations/warnings, e.g., due to trains being on a collision course, or due to equipment failure (for example, signals at a junction may fail, meaning that no train can proceed safely through that junction until a repair has been made).
- The ability to calculate a score, based on achievement of goals.

The basic operation of your game will be as follows. In each turn, each player will:
- Acquire a train goal (e.g., “send a diesel train from Kansas City to Lake Tahoe”). Each player may have no more than 3 goals at a time. Each goal is associated with a certain number of points; in general, a longer or more complicated goal should be awarded more points that a shorter or simpler goal.
- Acquire 2 game resources. A game resource might be a train of a particular type (e.g., diesel, electric, steam), or of a particular capability (e.g., a train that can travel at up to 125mph). Power-ups may be considered valid resources. A player can have no more than 7 resources at a time.
- Optionally, specify a routing (e.g., “Send an electric train from Saskatoon to Edmonton”) using specific resources. Note that the player may have some choice in specifying the routing (e.g., different routes, different resources that can be deployed).
- Run any specified routings (in random order). A routing may complete successfully (e.g., the electric train from York may end up in London), or it may not complete due to obstacles encountered during the journey. Obstacles may be due to an equipment failure at a junction, a collision, or other game scenarios.

After each turn, the game shall do the following:
- After any routing has executed, check to see if any goals have been achieved; if so, allocate appropriate points to the player.
- Remove any resources that the player has used in that turn. If a goal has not yet been achieved (e.g., the train is part-way between York and London), the resources remain with the player, and the overall total number of resources that the player holds does not change (that is, resources in-use count towards the player’s total number of resources).

Variation Points:
- Your game must include at least 5 cities. You are welcome to invent your own city names and locations. Use of humour in your requirement specification is recommended.
- Your game must support at least 10 different kinds of goals. Goals may be absolute (e.g., “send a train from Toronto to Hamilton”) or quantifiable (e.g., “send a diesel train from Edmonton to Vancouver in less than 6 hours”)
- Your game must support at least 10 different resources (as above).
- Every city must be connected to the train network.
- There must be at least two routes between at least two cities.
- There must be at least two junctions (i.e., train routes that cross).
- There must be at least two different types of obstacle that can arise in the game. Obstacles must be funny, for example, Godzilla.

## Elicitation

*Identify stakeholders for this scenario, and assume using interviewing as elicitation strategy, design a interview for each stakeholder.*

- Developers / designers. 

**Description**: Developers and designers turn the requirement to the product and constrain the requirement indirectly. There might be some modifications to the original requirements made by then due to implementation difficulties.

**Purpose**: The purpose is to understand the technological and design constraints regarding the current requirements. We need to be aware of any features in the existing requirements that are impossible to implement.

**Style**: It should be comprehensive and open-ended. We let them review the requirement and ask for professional suggestions and revisions. The efficiency is crucial because we’d like to gain as much valuable information as possible to avoid failure. Besides, it is open-ended we also need constructive opinions based on their perspective to make the game complete.

**Example question**: What are the technological difficulties faced regarding the current requirement?

**Explanation**: In the requirements stage, we want to forecast any difficulties in implementation, and modify the requirement. It can reduce the cost comparing with making modifications in future stages, and avoid the failure that the game being impossible to develop/design.

- Technical experts.

**Description**: Technical experts may offer constraints to our system since the game map is based on NA region, and we might need to consult experts in transportation field to refine our map to make it more sophisticated and rational.

**Purpose**: By collecting critiques and suggestions on the requirements of the game, we can make our game rational and avoid misconceptions. In this case, we want our “real” cities locates correctly on the map, and most routes are well planned.

**Style**: This interview should be consultative. We could show our game map and briefly introduce it, then expect some critiques and research suggestions (on geography/transportation). It should be asking questions, and we avoid topic extensions and professional opinions because we consider the suggestions as a reference instead of a requirement.

**Example question**: Is the train network and city map deigned rational in terms of a routing game?

**Explanation**: We need critiques from experts in geography and urban planning fields to make the game more rational, but our creative parts (funny cities/obstacles) should not be constrained.

- Government / regulatory bodies.

**Description**: They play a part in the regulation of games, and they can restrict or ban any illegal or inappropriate games. We need to avoid any potential regulatory issues to publish the game.

**Purpose**: The purpose is to make sure our game doesn’t violate any regulations, so that we can release and sell it legally, and avoid any potential regulatory issues.

**Style**: This interview should be precise and serious. Regulations are precise, so we want to be as accurate as possible, and we must take it seriously. We want them to proof reading the requirement, for any related concerns, we need to clarify and solve them in the interview.

**Example question**: What are the potential regulatory issues regarding the current requirement?

**Explanation**: We want to understand any regulatory constraints, then remove any potential violations to make sure the game could be approved.

- Game publishers / distributors.

**Description**: Game publishers are who we publish our game with, and distributors are who sell our game to public after it is officially released. We want our game to be launched at a proper time and be marketed to the target customer groups to maximize profits and minimize risks, so we need to consider their interests and opinions.

**Purpose**: The purpose is to understand the releasing and marketing policies. Based on their wants and needs, we might modify our game for commercial and profitable purposes.

**Style**: The interview should be open and informative. We want them to talk more about the game industry and customer preferences, and similarities of those successful games. Thus, we should be open for information and learn from it.

**Example question**: What are the similarities of your best sellers?

**Explanation**: They have seen substantial games in the industry and have idea about properties of successful and profitable games. Our game could learn from their successes.

- Players.

**Description**: Players are the clients of our game product, and they are who we develop the game for. We want the game to be popular and profitable, players’ requirements will directly influence our product requirements since we want to analyze and satisfy their needs.

**Purpose**: The purpose is to their expectations and preferences in the train-routing games. Besides, we want to know their opinions about competitors on details such as operations, cities maps, scenes and pricings.

**Style**: This interview should be chill and organized. Since plays might not have interview experiences, we need to start from some simple questions, and we must organize our questions. We want each player to concentrate on limited number of questions only.

**Example question**: What is your favorite transport routing game, and why?

**Explanation**: The game is designed for players, and we want to gather information about their preferences. Identifying the popular properties (element/operation/feature…) first, then we can revise our current features to meet their requirements.

- Media.

**Description**: Media indicate those who release game news and rate/rank new published games. They are involved because customers decide whether to buy the game based on game reviews on the media. If the game is high-ranked and highly appraised by media, it is more likely to be a profitable and success game.

**Purpose**: The purpose is to know the report preferences and target groups. We’d like to avoid negative influences on our game caused by misleading news. We also want filter out media having similar target groups with our game for future collaborations.

**Style**: The interview should be open-ended and well-worded. We want to gather more information from different platforms, while we don’t want to spoil too much about our game before it is released so the majority questions should be open. Besides, wording is important for media industry, so we have to pay extra attention.

**Example question**: What are your target groups portraits?

**Explanation**: This question is crucial because we may need to focus on media having common target groups with us. Their information has more reference value.

## Analysis

*Represent the system in this scenario in different diagrams.*

- Specify the data required for the system using UML class diagrams.

- Specify system operation and interaction using a use case diagram.

- Represent one example of information flow through the system using UML activity diagrams.


## Specification

*State some functional requirements and non-functional requirements in using a relevant requirements IEEE specification standard. Then, identify risks and analyze them.*

### Functional requirements

| ID           | FR-1 |
|--------------|-----|
| Name         | Invite the other player    |
| Description  | The system shall allow the player to invite the other player in the main menu of the game, and the system shall not allow any new invitations until the game ends once the other player accepts the invitation.    |
| Fit criteria | The system shall provide an option for players to invite the other player. The system of the other player shall receive the invitation. The invitation option for both players shall be disabled the once the invitation is accepted.    |

| ID           | FR-2 |
|--------------|-----|
| Name         | Synchronize game data    |
| Description  | The system shall connect two players and synchronize their game processes and data once the invitation is accepted.    |
| Fit criteria | The game data (including data of turns, goals, maps and resources) shall be the same for both players. The system of one player shall update game data once changes are made by the system of the other player.    |

| ID           | FR-3 |
|--------------|-----|
| Name         | Calculate score    |
| Description  | The system shall calculate points for each goal based on factors (complexity, route length, number of junctions, time limit, etc.). The system shall offer an efficiency bonus if player completes the goal, and the system shall give 0 points for failing to achieve the goal.    |
| Fit criteria | The calculated score shall match the result of pre-defined formulas.    |

| ID           | FR-4 |
|--------------|-----|
| Name         | Display score board    |
| Description  | The GUI shall show the score board to display points of each player on the screen once the game starts. The system shall use different colors to distinguish players and their points.    |
| Fit criteria | The players shall be able to see their usernames and points on the screen during the entire game period (after the game starts and before the game ends), and score of each player shall be in different colors.    |

| ID           | FR-5 |
|--------------|-----|
| Name         | Update score board    |
| Description  | The system shall update the score board after each turn. The system shall display the calculated score on the board after the name of that player.    |
| Fit criteria | The players shall be able to see their score on the score board after their turn. The displayed score on the score board shall match the calculated score (reference FR-3).    |

| ID           | FR-6 |
|--------------|-----|
| Name         | Determine the winner    |
| Description  | The system shall determine the winner (the player with the higher final score), then display a congratulations message with pictures to the winner’s screen, and comforting words for the loser.    |
| Fit criteria | The player with higher sum of all displayed scores (reference FR-5) shall be the winner. Both players shall see a message (winner sees congrats message and loser see cheer up message) once the game ends.    |

| ID           | FR-7 |
|--------------|-----|
| Name         | Display mini map    |
| Description  | The GUI shall display a mini map that contains intermediate cities and junctions along the route and supports basic operations (scroll up to zoom in, scroll down to zoom out, drag to move, press “M” to switch between full-screen map and mini map) in the corner of the screen during the game period.    |
| Fit criteria | The mini map shall match the game map accurately on intermediate cities and junctions, and players shall be able to see it during the game period. The GUI shall response to user interactions on specified basic operations properly as specified in the requirement.    |

| ID           | FR-8 |
|--------------|-----|
| Name         | Highlight goal on mini map    |
| Description  | The GUI shall highlight the route that corresponds to the selected goal, and the map shall update the train’s spatial position accordingly on the route.    |
| Fit criteria | The highlighted route shall match the route in the selected goal. The actual position of train shall match the position on the map.    |

### Non-functional requirements

| ID           | NFR-1 |
|--------------|-----|
| Name         | Reliability    |
| Description  | The game shall be reliable by providing stable connections for both players during the game period.    |
| Fit criteria | The connection holds at least 99% of the game period for each player. The disconnection shall not happen more than twice per game.    |
| Justification | The specified quantified measure of reliability can be divided into two components. The connection percentage is easy to monitor and record during the game period, and if the server works for at least 99% of the game period, it means that in a 15 min game, the total disconnected time would be no more than 10 seconds for both players. Since the disconnection shall not happen more than twice per game, each disconnection will be fixed within 5 seconds. This figure can be considered as reliable because it is totally acceptable for an online coop game with all game data operated and synchronized on the server. Besides, players will not be uncomfortable with a short disconnection if it can be restored quickly. Therefore, the given fit criteria can measure the reliability performance of the game. |

| ID           | NFR-2 |
|--------------|-----|
| Name         | Usability    |
| Description  | The game shall be easy to play by the general public.    |
| Fit criteria | At least 80% of a representative sample group shall be able to understand the operations and finish a turn after watching the tutorial. Furthermore, at least 95% of them shall be able to play after watching the tutorial and complete the game once with embedded instructions.    |
| Justification | Our game product is developed for the general public, so we need sampling from them. Once we have the representative sample groups, we can measure the percentage of players in each group that are able to understand the operations and finish a turn after watching the tutorial. If we can achieve more than 80%, most players can start their own game immediately. Besides, we also consider the slow learners with the criteria “at least 95% of them shall be able to play after tutorial and embedded instructions”. This allows players in different levels to be able to play. Therefore, it is reasonable to use it as a measure for usability. |

### Risk analysis

- The player is temporarily disconnected with the server for few seconds (or network fluctuation), the system might consider the player has quitted then terminate the game for both players.

**Likelihood**: The likelihood of occurrence is high for players with low-quality internet, and is low for those with good internet. However, this might destroy the engagement and player’s experience if the system couldn’t handle it.

**Mitigation**: The system shall have a disconnection protection that can hold the game for up to 30 sec. If one player is temporarily disconnected, the system shall hold the game (if it is his turn, hold the turn; if not, let the other player keep playing) until the player re-connect to the server.

**Justification**: Considering the instantaneous disconnection will not last longer than 30 sec to be re-connected, the protection should be reasonable. Compared with terminating the game for both players, a short waiting time is acceptable for players. This is also friendly for players with bad internet because disconnection has a bad impact in most competitive games, this mitigation will make our game more playable and relatively stable.

- The system might allow a player to fail to achieve all goals due to the probability of encountering obstacles (the player encounter fatal obstacles in every turn).
  
**Likelihood**: The likelihood of occurrence is very low, but it will negatively influence the engagement and joy of players.

**Mitigation**: The system shall have a guard to make sure that if a player has failed all turns before the last one due to obstacles, the last turn must have no fatal obstacle.

**Justification**: This is reasonable because if a player encounter obstacles, then fails in every turn, they might never want to play the game again. Considering the probability of fatal obstacles is very low, this guard will not influence the balance of the game because will remain other obstacles unchanged. It can improve the player’s experience without influence other players.


## Validation

*Propose a review / inspection process for the specification. Then design a test for some functional requirements with the traceability matrix.*

### Review process

1.	Preparation
-	Scheduling the review meeting and confirming the details (such as online/in person meeting, agenda etc.).
-	Determining the reviewing team and the role of each team member (including domain experts). Each reviewer should know his role in the review process, and which part of the document they’re responsible for.

2.	Discussing the reviewed materials
-	Identifying the requirement to be reviewed (including the document production process and reviewing process), and reviewers should spend some time being familiar with the system and the scenario. 
-	Establishing a common standard (for example, what is the definition of consist /unambiguous in this document), and each reviewer should use the same criteria for the part of document they’re assigned.
-	Eliminate any system/scenario related confusion before starting the actual review.

3.	Review
-	Proceeding through the assigned document and identifying the problems.
-	Addressing conflicts and recording any problems that found in the review process. If there are different opinion or undecidable issues, record all of them.
-	At the end of review, discuss those undecidable issues and try to consensus. Making sure that each reviewer is in agreement with the document as edited. 
-	Addressing the remained unresolvable problems.

4.	Follow-up
-	Applying any changes and updates made in the review session.
-	Considering and discussing whether to have the second review session.
-	At the end of the review process, record that each reviewer agrees with the final result and any problems related.

**Explanation**: The preparation stage is necessary to a review because we need to know what to review and the corresponding criteria. Otherwise, the review process would be invalid and inefficient. Since the game scenario is relatively unfamiliar to the reviewers, the discussion of materials and game concepts are necessary before the actual review session. It helps the reviewers to understand the game system and concepts. Then, the review session is the most crucial part that find problems and improve the requirement specification and game domain experts may involve helping. Finally, the follow-up stage can wrap up the process, and an optional second review can resolve more problem and further improve the specification.

References websites:
- https://www.dummies.com/business/business-strategy/how-to-conduct-a-requirements-review-for-business-analysis/
- https://www.bridging-the-gap.com/requirements-review/

### Inspection checklist

A checklist is an assurance that the document is inspected, and it also provides reviewers with hints and guidelines for finding problems. We need find as much problems as we can, and reviewers can make sure that they find problems in every aspect according to the checklist and record them. It also improves the consistency and efficiency of the review process because each reviewer of the same part of document can have an explicit goal and standard. Besides, it keeps track of the review process and benefits managers.

-	The naming convention of terms in the document is consistent. (yes/no)
-	Each functional requirement is stated unambiguously and concisely. (yes/no)
-	Each requirement has reasonable fit criteria, and it is testable. (yes/no)
-	Design/implementation level details are not included in each requirement. (yes/no)
-	Conflicts exist among the requirements in the document. (yes and address them/no)

### Requirements tests

| Test case #ID   | TC#001 |
|-----------------|-------|
| Assumption      | A game is started, and two players are in the game      |
| Input           | A player’s score is updated after a turn      |
| Expected output | The data is synchronized to the other player, and the updated score (with the correct score added to the corresponding player) is displayed to both players      |

| Test case #ID   | TC#002 |
|-----------------|-------|
| Assumption      | The game ends and the final score for players are calculated      |
| Input           | Two numbers as the final scores of two players are given to the system      |
| Expected output | The returned winner (determined by the system) is the player that has a higher score. If the given scores are the same, test whether the system determine a tie.      |

| Test case #ID   | TC#003 |
|-----------------|-------|
| Assumption      | The game is started      |
| Input           | None      |
| Expected output | A mini map that contains intermediate cities and junctions along the route is displayed for both players, and it matches the game map.      |

| Test case #ID   | TC#004 |
|-----------------|-------|
| Assumption      | The game is started, and the mini map is displayed      |
| Input           | A player drags and move the mini map on his screen      |
| Expected output | The GUI responses to user interactions, and the map (of the player) moves according to the movement of mouse dragging while the map of the other player remains unchanged.      |

| Test case #ID   | TC#005 |
|-----------------|-------|
| Assumption      | The game is started, and the player select a goal      |
| Input           | The goal is given to the system      |
| Expected output | The route that corresponds to the selected goal is highlighted on the map by GUI, and the highlighted route matches the route in the selected goal.      |

### Traceability matrix


## Security

*Describe how confidentiality and availability could be achieved for the system being developed in this scenario. Then, identify threats and design mitigation.*

### Confidentiality

- Improve (and frequently update) the detection of threat and attacks from the internet.

Since our game is based on internet connection, the system shall detect any potential threats/attacks to avoid unauthorized access to information. If new treats appear, the system detection should be updated in order to protect system data.

- Use multi-layers of protection for the game system and online data storage.

The data stored online should be protect, too. With the multi-layers security technique, the probability of confidentiality violation can be minimized.

- Develop a maintainable and revisable security protection.

Since our game need frequent updates and maintenance, the security protection shall adapt changeable system and new features. Therefore, the system could maintain confidentiality after every update/maintenance.

- Use sophisticated encryption techniques to avoid confidentiality violations.

Sophisticated encryption techniques can increase the difficulty of unauthorized access, then lower the risk of data being revealed.

- Improve the access control mechanism especially for the internet.

Strictly controlling the accesses through the internet can find potential violations, so the system shall classify the access accurately and determine whether to give the access permission.

### Availability

- Separate the protection of game server and ongoing game processes.

The game system includes the game server (which support game processes and other services) and many game processes (which is the individual game matches). Since the resources are limited, we need to prioritize the server because once the server is down, it requires more time and resources to recover comparing to a game match.

- Improve (and frequently update) the detection of DoS attacks.

The system shall detect any potential DoS attacks to prevent the situation where all resources are occupied by the attack requests and regular players can’t access the game system. If the system can detect and prevent DoS attacks, the system availability would be achieved.

- Improve the maintenance and recovery efficiency of the game server.

Since the maintenance and recovery will cause the downtime of the system and unavailability, improve the efficiency can reduce the downtime and achieve availability.

- Preparing a backup server is necessary.

Since the system requires continuous and stable connections, a backup server can provide required service when the main server is down. It helps for our online combat game system because server down will affect many players, a backup server can takeover and keep the availability of the system.

### Threat and mitigation

- **Threat**： Hackers might hack into the system connection of players and server to access the information (username, password, IP address …) of players.

**Mitigation**: Access control can mitigate against it because it can prevent unauthorized access to the connections. Once unauthorized access is detected, any further access would be blocked by the system. Hence the connection would not be hacked into. Besides, system can protect user information by encryption and hiding user information from the system connection.

- **Threat**： Unauthorized change/integrity violations of game data. (This is usually done by cheating software, and it hacks into the game server and change player’s data and game process.)

**Mitigation**: The system shall improve the third-party software detection and block any request from it. Besides, the system shall monitor any suspicious/unexpected changes (such as unexpected change of goals or unreasonably high scores) during the game process. Once suspicious action is found, the system shall block any actions from the external source to mitigate against the threat.
