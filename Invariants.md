# Invariants

## 1. Trains only travel one direction per each track. - Safety Hazard if violated
## 2. An approach signal will always precede a depart signal.
## 3. An alarm will always sound after an approach event
## 4. While a train is present there shall be an alarm and barrier engaged. - Safety Hazard if violated
## 5. While a train is approaching, an alarm shall sound and a barrier shall lower after 10 seconds. - Safety Hazard if violated
## 6. While trains are absent, no barrier will be engaged.
## 7. If multiple trains are present, the barrier will not disengage until the last train departs - Safety Hazard if violated

![alt text](https://github.com/uofu-emb/Thomas_Todd_Lab_9/blob/dev/Orig_FSM.png)

## Table
| number | arms_down | alarm_on | northbound_present | southbound_present | north_approach | south_approach | north_depart | south_depart | Elapsed | safety_hazard |
|--------|-----------|----------|--------------------|--------------------|----------------|----------------|--------------|--------------|---------|---------------|
| 0      | 0         | 0        | 0                  | 0                  |        6       |       5        |       17     |     17       |    20   |               |
| 1      | 0         | 0        | 0                  | 1                  |                |                |              |              |         |      19       |
| 2      | 0         | 0        | 1                  | 0                  |                |                |              |              |         |      19       |
| 3      | 0         | 0        | 1                  | 1                  |                |                |              |              |         |      19       |
| 4      | 0         | 1        | 0                  | 0                  |        6       |       5        |       17     |     17       |    0    |               |
| 5      | 0         | 1        | 0                  | 1                  |        7       |       5        |       17     |     17       |    13   |               |
| 6      | 0         | 1        | 1                  | 0                  |        6       |       7        |       17     |     17       |    14   |               |
| 7      | 0         | 1        | 1                  | 1                  |        7       |       7        |       17     |     17       |    15   |               |
| 8      | 1         | 0        | 0                  | 0                  |                |                |              |              |         |      21       |
| 9      | 1         | 0        | 0                  | 1                  |                |                |              |              |         |      19       |
| 10     | 1         | 0        | 1                  | 0                  |                |                |              |              |         |      19       |
| 11     | 1         | 0        | 1                  | 1                  |                |                |              |              |         |      19       |
| 12     | 1         | 1        | 0                  | 0                  |                |                |              |              |         |      19       |
| 13     | 1         | 1        | 0                  | 1                  |       15       |       23       |       23     |      4       |    19   |               |
| 14     | 1         | 1        | 1                  | 0                  |       23       |       15       |       4      |      23      |    19   |               |
| 15     | 1         | 1        | 1                  | 1                  |       23       |       23       |       15     |      15      |    19   |               |

| number | invariant                                                            |
|--------|----------------------------------------------------------------------|
| 16     |  Trains only travel one direction per each track                     |
| 17     |  An initial approach signal will always precede a depart signal.     |
| 18     |  An alarm will always sound after an approach event                  |
| 19     |  While a train is present there shall be an alarm and barrier engaged|
| 20     |  While a train is approaching, an alarm shall sound and a            |
|        |  barrier shall lower after 10 seconds                                |
| 21     |  While trains are absent, no barrier will be engaged                 |
| 22     |  If multiple trains are present, the barrier will not disengage      |
|        |  until the last train departs                                        |
| 23     |  A depart signal will always follow an approach event in the same    |
|        |  track direction                                                     |



![alt text](https://github.com/uofu-emb/Thomas_Todd_Lab_9/blob/dev/FSM.png)




