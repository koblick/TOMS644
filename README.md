# TOMS644
C      REMARK ON ALGORITHM 644, COLLECTED ALGORITHMS FROM ACM.
C      THIS WORK PUBLISHED IN TRANSACTIONS ON MATHEMATICAL SOFTWARE,
C      VOL. 21, NO. 4, December, 1995, P.  388--393.
C
C*** Readme
             INSTALLATION HINTS FOR ALGORITHM 644

                          D. E. AMOS
                 Sandia National Laboratories
-----------------------------------------------------------------

Algorithm 644 [2],[3] computes all major Bessel functions of a complex
argument and nonnegative order.  The single precision callable routines are
denoted by CBESH, CBESI, CBESJ, CBESK, CBESY, CAIRY AND CBIRY for the H, I,
J, K, Y, and Airy functions Ai and Bi.
CBESH computes H functions of kinds 1 and 2 and an option exists for the
derivatives of the Airy functions in CAIRY and CBIRY.
Scaling to remove exponential underflow or overflow and generation of sequences
in increasing orders are auxiliary options where appropriate.

It is convenient to consider the package in four parts:

   (1) Quick check PROGRAMS (CQC??) which exercise the main callable routines
       in double precision arithmetic:

          CQCBH   to test CBESH
          CQCBI   to test CBESI
          CQCBJ   to test CBESJ
          CQCBK   to test CBESK
          CQCBY   to test CBESY
          CQCAI   to test CAIRY and CBIRY and auxiliary subroutine CBESYH.

       The documentation for the latest versions of these quick checks is
       found in reference [4].  These routines need not be a permanent part of
       the installation once they have been compiled and successfully executed.

   (2) The main callable subroutines which comprise the algorithm
       in single and double precision arithmetic:

          CBESH   for H functions of kinds 1 and 2
          CBESI   for I functions
          CBESJ   for J functions
          CBESK   for K functions
          CBESY   for Y functions
          CAIRY   for Airy function Ai and Ai'
          CBIRY   for Airy function Bi and Bi'
          GAMLN and DGAMLN for lngamma(x), x > 0.

          Each subroutine or function has a prologue which defines the calling
          sequence.  These routines, along with those of (3) and (4), make up
          the permanent installation.


   (3) Lower level non-callable routines

The latest version containing all improvements is dated 930101.

REFERENCES

1. Abramowitz, M. and Stegun, I. A., Handbook of Mathematical Functions,
   NBS Applied Math Series 55, U.S. Dept. of Commerce, Washington, D.C., 1955

2. Amos, D. E., Algorithm 644, A Portable Package For Bessel Functions of a
   Complex Argument and Nonnegative Order, ACM Transactions on Mathematical
   Software, Vol. 12, No. 3, September 1986, Pages 265-273

3. Amos, D. E., Remark on Algorithm 644, ACM Transactions on Mathematical
   Software, Vol. 16, No. 4, December 1990, Page 404

4. Amos, D. E., Remark on Algorithm 644 (Improvements in Algorithm 644),
   ACM Transactions on Mathematical Software, (Estimated date 1995)
