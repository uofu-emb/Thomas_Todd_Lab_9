# Invariants

## 1. Trains only travel one direction per each track. - Safety Hazard if violated
## 2. An approach signal will always precede a depart signal.
## 3. An alarm will always sound after an approach event
## 4. While a train is present there shall be an alarm and barrier engaged. - Safety Hazard if violated
## 5. While a train is approaching, an alarm shall sound and a barrier shall lower after 10 seconds. - Safety Hazard if violated
## 6. While trains are absent, no barrier will be engaged.
## 7. If multiple trains are present, the barrier will not disengage until the last train departs - Safety Hazard if violated

![alt text](https://github.com/uofu-emb/Thomas_Todd_Lab_9/blob/dev/Orig_FSM.HEIC)

## Table
| number | arms_down | alarm_on | northbound_present | southbound_present | north_approach | south_approach | north_depart | south_depart | ringing | safety_hazard |
|--------|-----------|----------|--------------------|--------------------|----------------|----------------|--------------|--------------|---------|---------------|
| 0      | 0         | 0        | 0                  | 0                  | 0              | 0              | 0            | 0            | 0       | 0             |
| 1      | 0         | 0        | 0                  | 1                  | 0              | 0              | 0            | 0            | 0       | 1             | Alarm/Arms hazard
| 2      | 0         | 0        | 1                  | 0                  | 0              | 0              | 0            | 0            | 0       | 1             | Alarm/Arms hazard
| 3      | 0         | 0        | 1                  | 1                  | 0              | 0              | 0            | 0            | 0       | 1             | Alarm/Arms hazard
| 4      | 0         | 1        | 0                  | 0                  | 1              | 0              | 0            | 0            | 1       | 1             | if Elapsed Event
| 5      | 0         | 1        | 0                  | 1                  | 0              | 0              | 0            | 0            | 1       | 1             | Arms not down
| 6      | 0         | 1        | 1                  | 0                  | 0              | 0              | 0            | 0            | 1       | 1             | Arms not down
| 7      | 0         | 1        | 1                  | 1                  | 0              | 0              | 0            | 0            | 1       | 1             | Arms not down
| 8      | 1         | 0        | 0                  | 0                  | 1              | 0              | 0            | 0            | 1       | 1             | No alarm
| 9      | 1         | 0        | 0                  | 1                  | 0              | 0              | 0            | 0            | 0       | 1             | No alarm
| 10     | 1         | 0        | 1                  | 0                  | 1              | 0              | 0            | 0            | 0       | 1             | No alarm
| 11     | 1         | 0        | 1                  | 1                  | 0              | 1              | 0            | 0            | 0       | 1             | No alarm
| 12     | 1         | 1        | 0                  | 0                  | 0              | 1              | 1            | 0            | 1       | 0             |
| 13     | 1         | 1        | 0                  | 1                  | 1              | 1              | 0            | 1            | 1       | 0             |
| 14     | 1         | 1        | 1                  | 0                  | 0              | 0              | 1            | 1            | 1       | 0             |
| 15     | 1         | 1        | 1                  | 1                  | 1              | 1              | 1            | 1            | 1       | 0             |

| number | invariant                                                            |
|--------|----------------------------------------------------------------------|
| 16     |  Trains only travel one direction per each track                     |
| 17     |  An approach signal will always precede a depart signal.             |
| 18     |  An alarm will always sound after an approach event                  |
| 19     |  While a train is present there shall be an alarm and barrier engaged|
| 20     |  While a train is approaching, an alarm shall sound and a            |
|        |  barrier shall lower after 10 seconds                                  |
| 21     |  While trains are absent, no barrier will be engaged                 |
| 22     |  If multiple trains are present, the barrier will not disengage      |
|        |  until the last train departs                                        |


| number | state     |
|--------|-----------|
| 0      | 1         | idle
| 1      | 3         | present
| 2      | 3         | present
| 3      | 3         | present
| 4      | 2         | approach
| 5      | 3         | present
| 6      | 3         | present
| 7      | 3         | present
| 8      | 2         | approach
| 9      | 3         | present
| 10     | 2         | approach
| 11     | 2         | approach
| 12     | 2         | approach
| 13     | 2         | approach
| 14     | 2         | approach
| 15     | 2         | approach

![alt text](https://github.com/uofu-emb/Thomas_Todd_Lab_9/blob/dev/Numbered_FSM.HEIC)




