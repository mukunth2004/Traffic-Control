# Traffic-Control
Initialization: 
   -The game sets up the window size, the frame rate, and initializes pygame.
Loading Images: 
   - It loads images of cars for the game.
Classes:
   - Car Class: Represents each car in the game. It defines how cars move, turn, and interact with signals and other cars.
   - Signal Class: Represents traffic signals. Signals can be red (stop) or green (go).
Game Loop:
   - The game runs in a loop where it constantly updates and redraws the screen.
   - It checks for user input (like pressing keys or clicking the mouse) to control the game.
   - Cars and signals are updated in each iteration to reflect changes in their state or position.
Traffic Logic:
   - Cars move according to their direction (north, south, east, west) unless they encounter a red traffic signal or another car in their path.
   - Signals can be controlled using the keyboard (up arrow for green, down arrow for red). The active signal determines which direction of traffic can move.
   - Cars turn when they reach the center of the screen, simulating a junction.
Adding Cars:
   - You can add cars to the game by clicking the mouse in specific areas of the screen.
   - Cars are randomly assigned a spawn direction and a turn direction.
   - Ambulance Class:
   - There isn't a separate class specifically for ambulances, but the logic is integrated into the existing Car class.
   - When a new car is created, it has a chance to be designated as an ambulance based on a random condition.
Emergency Bypass:
   - Ambulances behave like regular cars most of the time, following traffic signals and stopping at red lights.
   - However, if an ambulance has its emergency lights on (not explicitly shown in the code but implied), it can bypass red lights.
Traffic Signal Interaction:
   - When an ambulance approaches a red traffic signal, it checks if its emergency lights are on.
   - If the emergency lights are on, the ambulance ignores the red signal and proceeds through the intersection.
   - This behavior is implemented in the `update` method of the Car class where it checks for signal states and collisions.
Impact on Traffic Flow:
   - All other cars (non-ambulance) must obey traffic signals, so they may have to wait at a red light while an ambulance passes through.
   - This simulates real-world scenarios where emergency vehicles are given priority to reach their destinations quickly.
Gameplay Effect:
   - The ambulance logic adds an element of urgency and priority to the traffic simulation.
   - Players can observe how traffic flow changes when an emergency vehicle is on the road, affecting their decisions in managing traffic and signals.
Game End:
   - The game ends when the user closes the window.


