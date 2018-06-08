# 3D_MANIPULATION
The name of our scene is “Study”. We have all our assets inside the “World” object. Our scene is analogical to a “Reading Room” in the physical world. 
We have created the scene with the following assets in it: -
·	Book Racks
·	Books
·	Coffee Table
·	Sofa 
·	Chair
·	Table
·	LCD TV
·	Laptop
·	Soda Vending Machine
·	Fan
·	Door
·	Cup
·	Pencil
·	Eraser
·	Apple

Steering States
There are 3 meaningful steering states
1.	Not Steering
2.	Steering Forward
3.	Steering Backward

Not Steering is the state where the user remains stationary in the virtual environment. There are no space transformations and the visual is of the user standing still and upright. No buttons should be pressed for this state.

Steering forward is the state where the user moves ‘forward’ in the virtual environment. The ‘forward’ motion is dependent on the position of the right tracker. For this steering state, the user would have to press the touchpad as well as the touchpad button. The touchpad’s y co-ordinate needs to be greater than 0 along with the button pressed for this state to be activated. This would work when the initial state is Not Steering.

Steering backward is the state where the user moves ‘backward’ in the virtual environment. The ‘backward’ motion is dependent on the position of the right tracker. For this steering state, the user would have to press the touchpad as well as the touchpad button. The touchpad’s y co-ordinate needs to be less than 0 along with the button pressed for this state to be activated. This would work when the initial state is Not Steering.

Interaction states
There are 5 meaningful interaction states
1.Open
2.Closed
3.Touching
4.Holding
5.Destroy

Open is the state where the virtual hand does not hold or touch any object. This state is analogous to an open palm.

Closed is the state where the virtual hand is unable to hold anything and the virtual hand would be able to knock off interactive objects. This state is analogous to a fist which can be used to knock off objects. When the trigger button on the tracker is pressed, the state of the hand transitions from  Open to Closed.

Touching is the state where the virtual hand is in contact with an interactive object. This state is analogous to touching an object, without holding or assuming control over it. When the virtual tracker overlaps with an object in the virtual environment, the state of the hand transitions from  Open to Touching.

Holding is the state where the virtual hand is in control over an object; the virtual hand grasps the object and is able to rotate it or throw it away. When the virtual hand is in the touching state and the trigger button on the tracker is pressed, the state of the hand moves on from Touching to Holding.

Destroy is the state where the virtual object is destroyed using both hands. When the virtual dominant hand (the hand used for interactions) is holding on to an object, the non dominant hand(the hand not used for interactions) touches the same object and the trigger button on the non-dominant hand tracker is pressed, the object is destroyed. For this state, the hand used for interactions must be holding onto an object (Holding state) and the hand not used for interactions must touch the same object and the press the trigger button. Soon after the object is destroyed the state transitions to Open. This state is analogous to crushing an object with two hands.

Interactive Objects
There are 5 distinct interactive objects in our environment
1.	Books
2.	Apple
3.	Pencil
4.	Eraser
5.	Cup

NOTE:
In our demonstration,
The steering is controlled by the right tracker.
The interaction is controlled by the left tracker (except for the Destroy state, which uses both hands)
