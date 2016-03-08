# Financial theory and corporate policy, 3rd ed.
### by Copeland/Weston

## Introduction

This book is a second course MBA or first course PhD in Economics. I'm reading it for a number of reasons:

1. I never understood economics as an academic field
2. I want to understand the basic terminology of economics
3. I want to understand what assumptions are made in basic economics
4. I want to understand how to model economically
	a. A person
	b. A company
	c. A set of companies
5. I want to understand different financial instruments, and how to price them
6. I want to write a domain specific language (DSL) that is able to model some of the above

## Chapter 1

Robinson Crusoe - one person, one-good economy. Consume vs. not consume. Not consume = investing => subjective interest rate.
Interest rate = price of deferred consumptions = rate of return of investment.

### Do "capital markets benefit society"?

*Assumptions:*
1. All outcomes from investment known with certainty
2. No transaction costs or taxes
3. Decisions made in one-period context (y_0, y_1)
4. Marginal utility of consumption is decreasing
5. Every individual prefer more consumption to less => marginal utility of consumption is positive

imagine plot of "sqrt(x)"

How much to consume now C_0 and how much at the end of period C_1?

Plot utility U on plane (C_0, C_1). Level-sets of this graph are called _indifference curves_.

For Robin Crusoe any point on an indifference curve gives the same utility.

The derivative at a point is called the _marginal rate of substitution_ (MRS) between consumption today and consumption tomorrow. We can think of it as an interest rate. We have MRS = -(1+r_i)

Let's assume we have productive opportunities (PO). It can be given by any function of investment that is decreasing (refer to 4. above).

Robin will make an investment in this productive opportunity if the return-rate is higher than the subjective rate of return r_i.

Look at PO and find B = max(dPO/dC_0). This is the _marginal rate of transformation_ (MRT). Now plot the curve U_2 for which we have the same tangent at B. This is the utility curve for which Robin with initial utility curve C_0 can move to by utilizing PO. This is because for Robin MRS = MRT.

Without the existance of capital markets, invividuals with different indifference curves *will choose different investments* (y_0, y_1) even if they have the same *endownment* and the same *investment opportunity* because they have different indifference curves. 

We now let Robin borrow at a market rate. For a given point A on his indifference curve U_1 we can now find a point B on a curve U_3 for which the tangent equals the market rate. If we also allow production in this setting, Robin is able to offset his U_2 determined by PO to an U_3 which is strictly larger than U_1. The separation of these two steps is called the _Fisher separation theorem_.

Answering the question "capital markets benefit society" amounts to showing that for a given indifference curve, we can always find a curve over a given indifference curve if the individuals can exchange intertemporal consumption amongst themselves.

By introducing PO and market rate borrowing, we have shown that Robin is better off.

It _also_ shows that even if two investors have different indifference-curves, they will choose the same investment strategy under this mode. As a result, all borrowers and lenders are better off with capital markets than without. This means that the manager of a firm will be able to single-handedly find the best investment strategy.

### Transaction costs

If transaction costs are non-trivial, we understand that a central market-place becomes important. The economical service provied by the market-place implies that *lending rates and borrowing rates _differ_*, thus invalidating the Fischer separation principle and the manager will no longer delegated the responsibiliry to decide the investment. Hence, perfect (friction-less) markets makes it much more convenient to model economical decisions but it is arguable a false assumption.

## Chapter 2

### Investment decisions

*Assumptions*
1. Intertemporal decisions made on knowledge of market-determined time value of money, ie interest rate.
2. Interest rate known with certainty in all time periods, ie non-stochastic.
3. All future payoff from current investment is known with certainty.
4. Perfect markets ie no transaction-costs.

### Synopsis

Main point is that the objective of the firm is to maximize the wealth of its shareholders = maximize present value of shareholders lifetime consumption = maximizing the price per stock.

This is also the same as the _discounted value of future expected cash flows_. The technique for project selection which is consistent with maximizing shareholder wealth is _net present value criterion_.

### Fisher separation

Since we have Fisher separation, we can let a manager optimize the investment decisions since even if we have different indifference curves between share hoders, we know that they will have maximal investment positions, ie they'd vote the same in a board meeting. This is called the _unanimity principle_.

Caveat: if there's a cost for investors to monitor the decisions made by the manager, this changes.

We now assume that managers always behave as to maximize the shareholders wealth. What methods can they use?

The discounted value after-tax cash-flows payed out is the same as the stream of dividends and is

S_0 = Sum(0, \infinify, Div_t / (1 + k_s)^t) where S_0 is the present value of shareholders wealth, and k_s is the market-determined rate of return on equity capital. Interestingly, capital gains are built into this formula. This means that the present value of the stock is the same whether an investor holds it forever of for a finite time. The value after that finite time is exactly the future dividends from that time on.

### Profit

In economics, porofits mean the rates of return in excess of the opportunity costs for funds employed in projects of _equal risk_. The main difference between accounting profits and economits' profits is that the former doesn't focus on cash-flows and when they occur. It only looks at net income and it doesn't maximze shareholders' wealth.

### Net Present Value (NPV)

We want the method to choose projects to satisfy:

1. All cash flows are considered
2. The cash flow should be discounted at the opportunity cost of funds
3. Should select from a set of mutually exclusive projects the one that maximizes shareholders' wealth, ie don't build a wooden and a steel bridge.
4. The value-additivity prinicple holds, ie one should be able to consider one project independently of the others.

The method that satisfies this is the Net present value:

NPV = Sum(1, N, NCF_t / (1 + k)^t - I_0), where NCF_t is the net cash flow in time period t, I_0 is initial cash outlay and k is the firm's weighted average cost of capital and N is the number of years in the project.

As long as NPV > 0 for a project, the manager should invest in it, as it is exactly the same as the increase in shareholders' wealth.

There's empirical evidence that the moment an industrial firm announces an investment, the stock prive is correlating with the expected gains and losses. For public firms there's no correlation since they are regulated and only earn their weighted average cost of capital.

## Chapter 3

Chapter 2 dealth with projects in the same scale and period.

### Project lengths

For projects with different lives the correct way to evaluate them is to assume that they are repeated indefinitely and in exactly the same way. One can show that the NPV is the correct method to use here as well, and there's a way to find the correct length of a project (for example when to harvest a forest) going on repeatedly using the same method.

### Capital constraints

Although a mangager should aways invest if the NPV > 0, for certain reasons, there can be contraints on the capital that the firm can use. For example two project could have 

Project | Cost    | NPV
--------+---------+-----
A       | $100000 | $100 
B       | $1000   | $50

Project A should always be choosen if there are no constraints, but $100000 is a lot of money! For example, the _Penrose effect_ might kick in, which says that it is not econmically feasible to grow aribtrarily because of management and personel costs. For example, it is not really feasible to grow more than 50% per year. But generally a firm can always raise capital if NPV is positive.

For a given set of projects, the manager should choose the subset that

1. is below the budget constraints
2. maximizes the NPV

This method is called the _present value index_ (PVI). 

If we have capital constraints and multiple periods, we look to _integer programming_ to find the optimal investment strategy. However, since capital constraints are difficult to motivate to begin with and due to that linear programming models have difficulty to incorporate uncertainty, it is less popular than imagined (written 1992).

### Inflation

With inflation affecting cash outflows differently than cash inflows a project with a positive NPV might be rejected after corrections for inflation. There's some controversy on what models to use here. It does not automatically affect the NPV negatively however, just more accurately.

### Uncertainty (term structure of interest rates)

(Kind of skipping here)

If we cannot assume interest rate to be constant, it gets more complicated:

1. Buy and sell bonds on expected interest rate (arbitrage)
2. Risk averse investors will require higher yields in order to hold longer-term bounds. The extra yield is calld the _liquidity premium_ (LP). Empirically one can statistically observe LP up to 8-9 months. The high variability therafter made it impossible to draw conclusions.
3. Market segmentaion: different firms have different loan-demands. Ie long-term projects need long-term debt. Firms want to match their capital payments according to their cash-flows.

## Chapter 4.

### Utility

Individuals have different indifference curves. Moreover, they have different utility functions. So economics doesn't say anything about them (although later in the chapter there are some rather poor argument as for _why_ that is).

All we assume, are five axioms of choice under utility:

(Axioms of carnial utility)

1. (Comparability/completeness) For two alternatives x, y in S we have either x > y or y > x or x ~ y (indifferent).
2. (Transitivity/consistency) If x > y and y > z then x > z.
3. (Strong independence) Let G(x,y;a) be the gamble with probability a of x and (1-a) of y. Let z be mutually exlusive of x, y. Then x ~ y => G(x,z;a) ~ G(y,z;a).
4. (Measureability) If x > y > z then there exists a s.t. y ~ G(x,z;a)
5. (Ranking) G preserves ordering, ie if x > u > z and x > v > z and u ~ G(x,z;a) and v ~ G(x,z,b) then b > a => v > u

They mean that individuals are rational and able to make decisions over arbitrarily many alternatives. Axiom 3 is usually the most controversial. Imagine if x is winning a left shoe and y a right shoe. z is also winning a right shoe. They are mutually exlusive but 3. tells us that after after winning a left or a right shoe, we don't care about winning a second right shoe.

6. We assume individuals to be greedy, ie marginal utility of wealth is always positive.

Utility is about establishing utility functions using the above axioms that apply without knowing individuals indifference curves.

Two properties:
1. Utility functions are order preserving, ie x > y => U(x) > U(y)
2. Utility is linear: U[G(x,y;a)] = a*U(x) + (1-a)*U(y)

So by assigning gambles to choice we can calculate expected utitity (which we will maximize).

Here the book makes some silly claims about the impossibility of comparing the individuals utility functions:

1. Give $100 to two individuals. Both experience increase in utility. "Who's increased more? It is impossible to say!"
2. "Interpersonal comparison of utiity functions are impossible." Argument: "If it were not, we could establish a social welfare function that would combine everyone's utility and we could then use it to solve such problems as the optimal distribution of wealth. We could maximize society's utility by taking wealth from individual i and giving it to individual j. However, it is not possible to know how real-world utility functions for different individuals should be aggregated. It follows that group utility functions, such as the utility function of a firm, have no meaning". This is a circular argument!

### Risk aversion

Since we can convert the axioms of utility into a utility function we can compare utility functions. If we set up a gamble between two prospects x and y, ie G(x,y;a) will we prefer the expected value of the gamble or the gamble itself?

U[E(W)] > E[U(W)] : risk aversion      : risk function concave
U[E(W)] = E[U(W)] : risk indifferent   : risk function linear
U[E(W)] < E[U(W)] : risk loving        : risk function convex

We can also talk about _(markowitz) risk premium_, the price an individual is willing to pay to avoid the gamble. This is calculated from the individual's utility function. If she is offered an insurance against the gamble which is below this price, she will buy it.

We will now assume the individual is risk averse. One can look at _relative risk aversion_ (RRA) (following Pratt-Arrow)

RRA = -W U''(W)/U'(W) which is )absolute risk aversion_ multiplied by weight. Emperical data (and intuition) dictates that a utility function will have the following properties:

1. Marginal utility of wealth > 0
2. Utility decreases with increasing wealth
3. ARA decreases with wealth
4. RRA is constant

This discounts a quadratic utility function often used in the literature. Instead it suggests a _power utility function_

U(W) = W^(-1)
U'(W) = W^(-2) > 0
U''(W) = -2W^(-3) < 0

### Stochastic dominance

We use cumulative distribution functions to compare assets.

First-order stochastic dominance applies to any increasing utility function. 

F_x(W) <= G_y(W) for all W

Second order stochastic dominance applies to risk-averse utility functions.

Integral(-\infinity, W_1. [G_y(W) - F_x(W)]dW) >= 0 for all W

These are criterions independent of the individuals utility functions.

### Mean and variance

If we assume that probability distribtions are normal, we can resort to just calculating combinations by their mean and variance. The indifference curves for a risk-averse investor becomes functions of mean and variance.

