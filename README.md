# Bond Futures Option

We present a pricing model for bond futures option. Assuming that the bond futures price at the maturity of the option is lognormal, the model adopts the Black’s analytical closed-form solution.  The futures price is taken directly from the market instead of being calculated from the bond futures calculator.

Let   be a price process of a given bond futures, and T be a payoff maturity date.  The bond futures option with the underlying BT is a European type derivative security whose matured payoff at the settlement date is given by

	 	(1)

where   (+1 for call, -1 for put) is the call-put index, X is the strike.  Assuming that the bond futures price at the maturity of the option is lognormal, the prices of bond futures options at time zero are given by using the Black’s formula, which are

	 	(2)
	 	(3)

where c and p are the call price and the put price,   is the discount factor, and   and   are given by

	 	(4)
	 .                     	(5)

The volatility  is defined so that   is the standard deviation of the logarithm of the bond futures price at the maturity of the option.  The above pricing formulae are based on the assumption that the futures price is a martingale, i.e., there is no drift term in the futures price dynamics.

There are closed-form solutions available for the Greek values for options described above.  GED adopts closed-form solutions for Deltas and Gammas, which are given by

	  for calls and   for puts,	(6)
	  for both calls and puts.	(7)

For Vega, Theta and Rho values, GED employs numerical differentiation.  Vega is calculated as

	 	(8)

where   is the option price corresponding to an upper 1% shift of futures price volatility, and   is the initial option price.  Theta is given by

	 	(9)

where   is the option value assuming one-day shift of value time while all else remains the same.  And rho is calculated as

	 	(10)

where   is the option value assuming 10 bp parallel shift of interest rates (see https://finpricing.com/lib/FxForwardCurve.html)
.

