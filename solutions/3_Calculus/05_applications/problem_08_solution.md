# Problem 8: Number of Requests Handled by a Server

## 1. Original Problem
Request rate is $r(t)=100+20t$ requests/min for $0\le t\le5$. Find total requests, average rate, and compare endpoint rates.

## 2. What We Are Trying to Find
Integrate the changing rate to accumulate total requests, then divide by time to find the average rate.

## 3. Key Idea or Theorem Needed Before the Calculation
A rate integrated over time gives total accumulated quantity. Average rate equals total divided by elapsed time.

## 4. Step-by-Step Solution
Integrate over five minutes:
$$R=\int_0^5(100+20t)dt=[100t+10t^2]_0^5=500+250=750.$$
Thus total arrivals are 750 requests. Average rate is $750/5=150$ requests per minute. Endpoint rates are $r(0)=100$ and $r(5)=200$ requests/min.

## 5. Why Each Step Is Valid
The rate is continuous, and its units are requests per minute; multiplying by minutes through integration leaves requests. As a linear increase, its average equals the midpoint of its endpoint rates.

## 6. Final Answer in Words
750 requests arrived; average rate was 150 requests/min, between 100 and 200.

## 7. Quick Verification
A linear rate rises from 100 to 200, so the average 150 over five minutes predicts $150\cdot5=750$ requests.

## 8. Common Mistakes
- Reporting 750 as a rate rather than a total.
- Forgetting the time units when interpreting the average.

## 9. Short In-Class Explanation
Integrate the rate over five minutes to get 750 requests. Divide by five for an average of 150 requests per minute, between the endpoint values.
