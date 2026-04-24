# Experiments To Try

These small experiments help students understand how the model behaves.

## Change risk aversion

Increase `q` and observe whether the circuit favors safer portfolios. Then decrease `q` and observe whether return becomes more important.

## Change expected returns

Increase one value in `mu`. The portfolio containing that asset should become more attractive if risk does not dominate.

## Change covariance

Increase an off-diagonal value in `Sigma`. This makes two assets move together more strongly, which can make selecting both less attractive.

## Change QAOA depth

Try `p_layers = 1`, `2`, and `3`. More layers can improve expressiveness, but they also make the classical search harder.
