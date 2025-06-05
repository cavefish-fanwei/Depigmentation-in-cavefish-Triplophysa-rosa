# T_total =  Divergence time between cavefish and surface fish (million years ago)
# omega_c =  Omega value for the cavefish lineage
# omega_s =  Omega value for the surface fish lineage
# omega_n =  Omega value for the surface fish lineage in neutral evolution, =1

# Define the function to estimate colonization time and evolutionary periods

estimate_cave_colonization_time <- function(T_total, omega_c, omega_s, omega_n = 1) {
  # Calculate the functional period using the given formula
  T_f <- T_total * (omega_n - omega_c) / (omega_n - omega_s)
  # Calculate the neutral evolution period as the remainder of total divergence time
  T_p <- T_total - T_f
  # Return a list containing the functional period, neutral evolution period, and estimated colonization time in million years ago (mya)
  return(list(
    functional_period = T_f,
    neutralevolution_period = T_p,
    cave_colonization_time_mya = T_p
  ))
}

# Input parameters for the estimation
result <- estimate_cave_colonization_time(
  T_total = 21.3, 
  omega_c = 0.413,  
  omega_s = 0.215   
)

# Print the result containing the calculated periods and colonization time
print(result)
