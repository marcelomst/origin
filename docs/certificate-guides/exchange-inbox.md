# Exchange Inbox
**Reference Implementation:** [https://origin-ui-canary.herokuapp.com/certificate/exchange-inbox](https://origin-ui-canary.herokuapp.com/certificate/exchange-inbox)  

The Exchange Inbox allows admin users to sell, withdraw, transfer and export certificates that are currently in the organization’s Exchange Deposit Address.  Certificates in this inbox are in the custody of the platform operator and are active on the exchange. This inbox is associated with your Organization's [Exchange Deposit Address](../user-guide-reg-onboarding.md#exchange-deposit-address).   

**When the issuing body approves a certificate request, the certificate is first deposited into the Exchange Inbox.** Certificates must be in the Exchange Inbox in order to be:  

1. Posted for sale
2. Transferred to another exchange deposit address
3. Transferred to the [Blockchain Inbox](./blockchain-inbox.md)
4. Exported to an I-REC account. 

If you want to move certificate hours from this inbox into your organization’s [Blockchain Inbox](./blockchain-inbox.md), you must use the [Withdraw](#withdraw) tab on this interface. 

![Certificates-exchangeinbox](../images/certificates/certificates-exchangeinbox.png)  

The Exchange Inbox shows all certificates that are currently active on the Exchange that are associated with your organization’s [Exchange Deposit Address](../user-guide-reg-onboarding.md#exchange-deposit-address). Certificate hours in your Exchange Deposit address are active and can be sold on the Exchange using the [Sell tab](#sell).

## View Certificate Details

You can view a certificate’s details by clicking on ‘View’:

![Certificate-viewdetailsbutton](../images/certificates/certificate-viewdetailsbutton.png)

## Sell 

To put generated Mwh on the exchange for sale, select the certificate that you want to sell and navigate to the Sell tab. Set a price per Mwh. 

Note that by default, all of the Mwh that the certificate represents will be for sale. You can edit the amount of Mwh that you want to sell by clicking on the edit icon and entering in the desired number. 

![certificate-sell](../images/certificates/certificate-sell.png)

When you are satisfied with the price and number of Mwh to sell, click ‘Sell Certificate’. This will create an [ask](../user-guide-glossary.md#ask) on the exchange:

![exchange-ask](../images/exchange/exchange-ask.png)

## Withdraw

To withdraw certificates from the exchange to your organization’s Blockchain Inbox account, select the certificate you want to withdraw and navigate to the Withdraw tab.  

![certificate-exchangeinbox-withdraw](../images/certificates/certificate-exchangeinbox-withdraw.png)

Note that by default, all of the Mwh that the certificate represents will be up for withdrawal. You can edit the amount of Mwh that you want to withdraw by clicking on the edit icon and entering in the desired number.   

Once you withdraw the Mwh, they  will be transferred to your [Blockchain Inbox](./blockchain-inbox.md) under the generation device.

## Transfer

Mwh from certificates can be transferred to another Exchange Deposit address if you would like to perform a transfer or a sale off of the exchange interface. To transfer Mwh from a certificate to another Exchange inbox account, select the certificate that you would like to transfer and navigate to the Transfer tab. 

![certificate-exchangeinbox-transfer](../images/certificates/certificate-exchangeinbox-transfer.png)

Note that you can edit the number of Mwh you would like to transfer by clicking the pencil icon next to the Mwh. By default, the number of Mwh to transfer is the total number of Mwh available from the certificate. 

Enter the exchange deposit address and click “Transfer Certificate”. 

## Export













