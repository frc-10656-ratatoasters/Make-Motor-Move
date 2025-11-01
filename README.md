# Make-Motor-Move
make motor move

package frc.robot;

import com.ctre.phoenix6.hardware.TalonFX;
import edu.wpi.first.wpilibj.TimedRobot;

public class Robot extends TimedRobot {
    // Create a TalonFX object for the Kraken
    private TalonFX krakenMotor = new TalonFX(1); // Use your motor's CAN ID here

    @Override
    public void teleopPeriodic() {
        // Spin the motor at 50% power
        krakenMotor.set(0.5);
    }

    @Override
    public void disabledInit() {
        // Stop the motor when robot is disabled
        krakenMotor.set(0);
    }
}
