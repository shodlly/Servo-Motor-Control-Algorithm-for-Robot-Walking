

# Servo Motor Control Algorithm for Robot Walking

This README describes the algorithm for controlling servo motors to simulate walking motion for a robot. The robot's legs are controlled using servo motors attached to the hip, knee, and ankle joints.

## Initialization

The initialization phase sets up the servo motors and ensures they start at the default angle.

```cpp
// Initialization
Attach hipRight to pin 2
Attach kneeRight to pin 3
Attach ankleRight to pin 4
Attach hipLeft to pin 5
Attach kneeLeft to pin 6
Attach ankleLeft to pin 7
Set all servo angles to 90
```

## Main Loop

The main loop continuously executes the `WalkCycle` function to simulate walking.

```cpp
// Main Loop
Loop:
    Execute WalkCycle continuously
```

## Functions

### WalkCycle

The `WalkCycle` function coordinates the movement of both legs in a walking sequence.

```cpp
Function WalkCycle:
    LiftRightLeg
    MoveRightLegForward
    PlaceRightLegDown
    LiftLeftLeg
    MoveLeftLegForward
    PlaceLeftLegDown
```

### LiftRightLeg

Lifts the right leg by adjusting the knee and ankle servos.

```cpp
Function LiftRightLeg:
    Set kneeRight to 60
    Set ankleRight to 120
    Wait 500 milliseconds
```

### MoveRightLegForward

Moves the right leg forward by adjusting the hip servo.

```cpp
Function MoveRightLegForward:
    Set hipRight to 120
    Wait 500 milliseconds
```

### PlaceRightLegDown

Places the right leg down by resetting the knee and ankle servos.

```cpp
Function PlaceRightLegDown:
    Set kneeRight to 90
    Set ankleRight to 90
    Wait 500 milliseconds
```

### LiftLeftLeg

Lifts the left leg by adjusting the knee and ankle servos.

```cpp
Function LiftLeftLeg:
    Set kneeLeft to 60
    Set ankleLeft to 120
    Wait 500 milliseconds
```

### MoveLeftLegForward

Moves the left leg forward by adjusting the hip servo.

```cpp
Function MoveLeftLegForward:
    Set hipLeft to 120
    Wait 500 milliseconds
```

### PlaceLeftLegDown

Places the left leg down by resetting the knee and ankle servos.

```cpp
Function PlaceLeftLegDown:
    Set kneeLeft to 90
    Set ankleLeft to 90
    Wait 500 milliseconds
```

## Notes

- Ensure that all servos are properly calibrated before starting the walking cycle.
- Adjust timing and angles as needed based on the specific hardware and desired walking pattern.

