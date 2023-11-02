This script is designed to optimize the parameters of a vehicle's braking system in order to achieve the maximum possible deceleration. The optimization takes into account the capabilities of the braking system as well as the physical limits of tire grip.

## Description

The code performs an optimization routine to find the set of parameters that yield the highest deceleration in g-forces without exceeding the maximum grip available from the tires. The parameters include mass, brake pad coefficient of friction (mu), caliper piston area, master cylinder bore area, brake bias, pedal force, pedal ratio, and tire radius.

## Assumptions

- **Tire Grip**: The script assumes a static coefficient of friction (mu) between the tire and the road. This value is critical as it determines the maximum potential grip. In real-world applications, this value is not constant and can vary with tire composition, road surface, temperature, and wear. To measure this coefficient in practice, skid tests or deceleration tests can be conducted in controlled conditions using the specific tire set and road surface in question.

- **Weight Transfer**: During braking, weight is transferred to the front wheels, increasing their grip potential and reducing the grip at the rear. The script assumes a simple physical model for weight transfer based on the vehicle's center of gravity, total weight, and wheelbase.

- **Vehicle Dynamics**: The script models the vehicle as a rigid body and assumes uniform deceleration. In reality, vehicle dynamics can be complex, and factors like suspension geometry, aerodynamic forces, and dynamic weight shifting can significantly influence braking performance.

- **Hydraulic Pressure**: The braking force generated is assumed to be proportional to the hydraulic pressure applied by the master cylinder on the brake calipers. This does not account for potential losses in the brake lines or variations in brake pad performance due to temperature changes.

- **Brake Bias**: The script assumes a fixed brake bias, which determines the ratio of front to rear braking force. While some vehicles have adjustable brake bias, this script uses a single value throughout the optimization process.

- **Uniform Brake Pad Mu**: The coefficient of friction of the brake pads (mu) is assumed to be uniform across all pads. In practice, this coefficient can vary due to temperature, pad material, and condition.

## How to Obtain/Mesure Values in Real Life

- **Coefficient of Friction (mu)**: This can be measured through testing using a device like a skid trailer, which measures the force required to slide a known weight on the tire across the road surface.
  
- **Weight Transfer**: Can be calculated or measured by sensors placed on the vehicle that measure the load on each tire during braking.
  
- **Hydraulic Pressure**: In a physical setup, hydraulic pressure can be measured using pressure sensors in the brake lines.
  
- **Brake Bias**: For vehicles with adjustable brake bias, the optimal setting can be found through testing and driver feedback.
  
- **Brake Pad Mu**: The friction level of brake pads can be measured using a tribometer in a controlled environment, often at different temperatures to simulate real-world conditions.

## Usage

To use this script, you will need to input the specific parameters of your vehicle and its braking system into the designated sections of the code. The script will then output the optimized values for the braking system parameters to achieve the maximum deceleration g-force.

Please ensure to replace the bounds and initial guesses with values that are realistic for your specific vehicle to ensure meaningful optimization results." > README.md
