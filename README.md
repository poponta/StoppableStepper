# StoppableStepper
For Arduino library. This module has inherited "Stepper" module at Arduino Libraries.

If you use this modules, you need to modify "Stepper.h" as below because of Inheritance.

    void step(int number_of_steps);

    int version(void);

//  private: <- comment out
  protected:  // <- add "protected:" keyword 
    void stepMotor(int this_step);

    int direction;            // Direction of rotation
    unsigned long step_delay; // delay between steps, in ms, based on speed
