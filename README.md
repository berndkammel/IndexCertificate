# Ethereum Solidity based Index Certificate

IndexCertificate is a trading function which allows the issuer to setup up new index certificates. Potential buyers have the possibility to take part on the action of the certificate by using the platform which refers to the contract of the index certificate. 

#Smart contract 

The contract source code, IndexCertificate, is written in Solidity, Ethereum's language for constructing smart contracts.

#Smart contract structure

**- string UnderlyingName :** Underlying Index Reference 

**- bool BuyerLong :**  Long or short position of the Buyer  

**- uint IndexStrike :**  Strike Price  

**- uint PayAmount :**  Reward, if Strike is reached. Could also be a formula, etc.  

**- uint ContractPremium :**  Premium to be paid by the buyer  

**- uint IndexValue :**  Actual index value   

**- address Issuer :**  address of the issuer, will be  determined and set automatically 

**- address Buyer :**  address of the buyer,  will be determined and set automatically 

**- function initiateCertificate(bool bLong, string uName, uint iStrike, uint cPremium, uint iValue, uint pAmount) :**
Initialize of the Contract with the basis information. ContractPrice should be separate from the rest (constant and immutable
contract vs variable contract premium. Or other values declared private) **

**-  function buyCertificate(uint cPremium):** The Buyer enters into the contract here by paying the Contract Premium.
	The Issuer gets the Premium immediately.

**- function updatePrice(uint cPremium, uint iValue) :** only the issuer can update the contract premium and Index Value. Usually at the same time.

**- function buyCertificate(uint cPremium) :**  the Buyer agrees to the contract, here by paying the Contract Premium. The out come of this is that Issuer gets the Premium immediately.


#License information

Copyright (c) 2016 Fimas Market Solution

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

