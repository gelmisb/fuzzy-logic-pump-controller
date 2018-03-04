# fuzzy-logic-pump-controller
## Assignment 1 for Computer Intelligence for Stephen Sheridan

### Computational Intelligence Assignment 1 - 20%
#### Gelmis Bartulis (B00080902)


 **InputVariable1**
![Alt text](images/level.png?raw=true "Inputvariable1 - Level")



 **InputVariable2**
![Alt text](images/demand.png?raw=true "Inputvariable2 - Demand")



 **Outputvariable**
![Alt text](images/command.png?raw=true "Outputvariable - Command")


**Rule Matrix**

| *Demand* |  |  | *Level* |  |  |
| --- | --- | --- | --- | --- | --- |
|   | `vlow` |	`low` |	`good` |	`high` |	`vhigh` |
| `vlow`	 |	good |	vlow |	vlow |	low	 |	low	 |
| `low`	 |	vlow	 |	low |	good |	high |	vhigh |
| `good`	 |	low |	good |	good |	high |	high |
| `high`	 |	high |	high |	high |	good |	vhigh|
| `vhigh`	 |	vhigh	 |	vhigh	 |	high	 |	good	 |	good |





**Translated rules**

```
if (level is vlow or level is low) then command is vhigh
if (level is good) then command is good
if (level is high or level is vhigh) then command is vlow

if (level is good and demand is vlow) then command is vlow
if (level is good and demand is low) then command is low
if (level is good and demand is good) then command is good
if (level is good and demand is high) then command is high
if (level is good and demand is vhigh) then command is vhigh

if (level is vlow and demand is vlow) then command is good
if (level is low and demand is low) then command is good
if (level is high and demand is high) then command is good

if (level is vlow and demand is vhigh) then command is vhigh
if (level is low and demand is vhigh) then command is high
if (level is high and demand is vhigh) then command is low
if (level is vhigh and demand is vhigh) then command is vlow

```

**Description**
*Your goal for this assignment is to design and implement a Fuzzy Logic pump controller for the
feedback system shown below.*
Your fuzzy logic pump controller must control the bidirectional pump shown in the diagram above
in order to keep the level in the water tank between 40% and 70% full. The level in the water tank
is effected by a demand for water from appliances further down the line and its level can also be
effected by rainfall. The appliances further down the line can consume water from the tank and
can also feed water bank into the tank.
You should use the following input and output variables as part of your design:
Each variable should be broken down into the appropriate terms and membership functions but
that part of the fuzzy logic design along with the inference rules are left up to you.
Deliverables
You should create a design document that details your decisions with regard to the creation of
linguistic variables, and rules terms. Your document should include diagrams for each linguistic
variable showing how each term is setup. You should also create a rule matrix and translate it into
rules for your system.
Your fuzzy logic controller should be able to maintain the level in the water tank so that the green
light remains on. You should use the pump, rain, and demand checkboxes to ensure your system
works under all conditions. You will need to submit a single zipped file containing your design
document and the java source code.



#### Deadline
**Friday March 9th 2018 at 18.00hrs.**
