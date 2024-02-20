<h1>ExpNo 1 :Developing AI Agent with PEAS Description</h1>
<h3>Name: Daniel C</h3>
<h3>Register Number: 212223240023</h3>

# AIM:
To find the PEAS description for the given AI problem and develop an AI agent.


# Theory
# Vaccum Cleaner agent:
The VacuumCleanerAgent is a Python class that simulates the behavior of a basic vacuum cleaner in a two-location environment ("A" and "B"). The agent can perform four actions: move left, move right, suck dirt, and do nothing. Its state includes the current location and dirt status in each location. The agent's initial state is at location "A" with no dirt. Actions like moving and sucking dirt can change its state, and the print_status method displays the current location and dirt status. This agent provides a foundation for simple vacuum cleaner simulations and can be adapted for more complex scenarios.

# PEAS DESCRIPTION:
![image](https://github.com/Daniel-christal/19AI405ExpNo1/assets/145742847/8872fcf5-628e-4c90-a346-647460001f0e)

# DESIGN STEPS
# STEP 1:Identifying the input:
Location.

# STEP 2:Identifying the output:
move_left: Moves the agent to the left if it is currently at location "B.".
move_right: Moves the agent to the right if it is currently at location "A."
suck_dirt: Sucks dirt in the current location if there is dirt present.
After sucking dirt, the dirt status in that location is updated to indicate cleanliness.
do_nothing: Represents a passive action where the agent remains idle.

# STEP 3:Developing the PEAS description:
PEAS description is developed by the performance, environment, actuators, and sensors in an agent.

# STEP 4:Implementing the AI agent:
Clean the room and Search for dirt and Suck it.

# code:

class VacuumCleanerAgent:
    def _init_(self):
        # Initialize the agent's state (location and dirt status)
        self.location = "A"  # Initial location (can be "A" or "B")
        self.dirt_status = {"A": False, "B": False}  # Initial dirt status (False means no dirt)

    def move_left(self):
        # Move the agent to the left if possible
        if self.location == "B":
            self.location = "A"

    def move_right(self):
        # Move the agent to the right if possible
        if self.location == "A":
            self.location = "B"

    def suck_dirt(self):
        # Suck dirt in the current location if there is dirt
        if self.dirt_status[self.location]:
            self.dirt_status[self.location] = False
            print(f"Sucked dirt in location {self.location}")

    def do_nothing(self):
        # Do nothing
        pass

    def perform_action(self, action):
        # Perform the specified action
        if action == "left":
            self.move_left()
        elif action == "right":
            self.move_right()
        elif action == "suck":
            self.suck_dirt()
        elif action == "nothing":
            self.do_nothing()
        else:
            print("Invalid action")

    def print_status(self):
        # Print the current status of the agent
        print(f"Location: {self.location}, Dirt Status: {self.dirt_status}")

#Example usage:
agent = VacuumCleanerAgent()

#Move the agent, suck dirt, and do nothing
agent.perform_action("left")
agent.print_status()

agent.perform_action("suck")
agent.print_status()

# OUTPUT:
![image](https://github.com/Daniel-christal/19AI405ExpNo1/assets/145742847/0bb0262e-9e73-484a-8d65-cc969b70c776)

# RESULT:
Thus, an AI agent is developed.
