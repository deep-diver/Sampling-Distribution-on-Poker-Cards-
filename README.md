# cards-sampling-distribution

![Image of Playing Card](https://raw.githubusercontent.com/deep-diver/cards-sampling-distribution/master/playing-cards.png)

#### 1. First, create a histogram depicting the relative frequencies of the card values for a single draw. Report the mean, median, and standard deviation of the value distribution.

* This experiment will require the use of a standard deck of playing cards. This is a deck of fifty-two cards divided into four suits (spades (♠), hearts (♥), diamonds (♦), and clubs (♣)), each suit containing thirteen cards (Ace, numbers 2-10, and face cards Jack, Queen, and King).

![Image of Frequency Histogram](https://raw.githubusercontent.com/deep-diver/cards-sampling-distribution/master/freq_hist.png)

* As you can see, values 1 to 9 has equal frequency(4), but the value 10 has much higher frequency(16).
* Features
  * **Mean:** 6.54  
  * **Median:** 7
  * **Standard Deviation(SD):** 3.15

#### 2. Take a look at the distribution of the three-card sums from the samples that you obtained from Generated Data. Report descriptive statistics for the samples you have drawn. Include at least two measures of central tendency and two measures of variability.

* **Generated Card Data (30 samples) -> Converted Value :**  
(7h Kh 3d) -> 20, (Jd Kh 9d) -> 29  
(2c Qs Jd) -> 22, (8h 8d 6c) -> 22  
(Qs Kc 3h) -> 23, (4h Ac Qc) -> 24  
(2s 9d Ad) -> 21, (9c 3d 8c) -> 20  
(7h 7c Ac) -> 24, (7d Jc Qc) -> 27  
(Kd 7d 3s) -> 20, (Jd 3h 10h) -> 23  
(Jc 10d 10h) -> 30, (Qd 8d 3s) -> 21  
(6s 9c 8c) -> 23, (4c 3s 6h) -> 13  
(Ac 10h 5s) -> 25, (4s 4d Qs) -> 18  
(4s Ks Jh) -> 24, (3c Qd 2c) -> 15  
(Kh 5d Ac) -> 25, (2d 7s 5h) -> 14  
(Ac 3c 10c) -> 23, (Jd Jc Ad) -> 30  
(10d 5s 6s) -> 21, (2h 2d 6c) -> 10  
(Kh 3d 6d) -> 19, (2c Jd 5c) -> 17  
(5s 6h 9d) -> 20, (5s 10d 3h) -> 18  


* **Measures ( central tendency )**
  * Mean: 21.37
  * Modal: 20, 23 (if bin size is 5, modal is range of 20~25)
  * Median: 21.5
  
* **Measured ( variability )** 
  * Min: 10, Max: 30
  * Q1: 19, Q2: 21.5, Q3: 24
  * Q3-Q1: 5
  * Sampling Deviation(SD): 4.64
 
#### 3. Create a histogram of the sampled three-card sums. Compare its shape to that of the original distribution. How are they different, and can you explain why this is the case?

![Image of Avg. of three-card sums](https://raw.githubusercontent.com/deep-diver/cards-sampling-distribution/master/Avg.%20of%20three-card%20sums.png)

* the original distribution histogram looks uniformly distributed even though the value 10 has higher frequency than others, but the sampling distribution histogram looks normally distributed. 
* the original case gives every cards to be selected with equal probability. However, in the latter case, every combination of 3 cards to be selected at once has different probability. It is very rare to pick (1, 1, 1) or (10, 10, 10) combinations comparing to the randomly shuffled combinations. It makes the left and right side of the histogram to be shallower than center.

#### 4. Make some estimates about values you would get on future draws. Within what range will you expect approximately 90% of your draw values to fall? What is the approximate probability that you will get a draw value of at least 20? Make sure you justify how you obtained your values.

* Within what range will you expect approximately 90% of your draw values to fall?
  * first, need to know where the first 5% and the last 5% fall.
    * by changing to the standard normal distribution scale, the first and the last 5% are -1.64 and 1.64 respectively according to the z-table.
  * second, we can conver the z-table values into the actual value by calculating "value / SD = z-table value". 
    * since standard deviation is 4.64, those two values are -7.61 and 7.61.
  * third, add the mean value(21.37) from the sample distribution to the -7.61 and 7.61 values.
  * calculated range which approximately 90% of values to fall is "13.26 ~ 28.98"
  
* What is the approximate probability that you will get a draw value of at least 20?
  * first, find where "20" is in the standard normal distribution, and the location is its z-table value.
    * (20 - mean(21.37)) / SD(4.64) == -0.29
  * second, find the probability for the -0.29 z-table value. 
    * by looking up the z-table, it is "0.3859"
  * 1 - 0.3859 = 0.6141 == 61.41%
