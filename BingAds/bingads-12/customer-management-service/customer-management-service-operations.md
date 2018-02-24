---
title: Customer Management Service Operations
ms.service: bing-ads-customer-management-service
ms.topic: article
author: eric-urban
ms.author: eur
description: Service operations reference for the CustomerManagement service.
---
# Customer Management Service Operations

> [!IMPORTANT]
> This v12 preview documentation is subject to change.

The Customer Management service defines the following service operations.

|Service Operation|Description|Request Limits|
|---|---|---|
|[AddClientLinks](addclientlinks)|Initiates the client link process to manage the account of another customer.|10 *ClientLink*|
|[DeleteAccount](deleteaccount)|Deletes an account.|1 *AccountId*|
|[DeleteCustomer](deletecustomer)|Deletes a customer.|1 *CustomerId*|
|[DeleteUser](deleteuser)|Deletes a user.|1 *UserId*|
|[FindAccounts](findaccounts)|Gets a list of accounts owned by the specified customer that match the specified filter criteria.|1 *CustomerId*|
|[FindAccountsOrCustomersInfo](findaccountsorcustomersinfo)|Gets a list of the accounts and customers that match the specified filter criteria.|Not applicable.|
|[GetAccount](getaccount)|Gets the details of an account.|1 *AccountId*|
|[GetAccountsInfo](getaccountsinfo)|Gets a list of objects that contains account identification information, for example the name and identifier of the account, for the specified customer.|1 *CustomerId*|
|[GetCustomer](getcustomer)|Gets the details of a customer.|1 *CustomerId*|
|[GetCustomerPilotFeatures](getcustomerpilotfeatures)|Gets a list of the pilot programs in which the specified customer participates.|1 *CustomerId*|
|[GetCustomersInfo](getcustomersinfo)|Gets a list of objects that contain customer identification information, for example the name and identifier of the customer.|Not applicable.|
|[GetUser](getuser)|Gets the details of a user.|1 *UserId*|
|[GetUsersInfo](getusersinfo)|Gets a list of objects that contains user identification information, for example the user name and identifier of the user.|1 *CustomerId*|
|[SearchAccounts](searchaccounts)|Searches for accounts that match a specified criteria.|1 *Predicates*|
|[SearchClientLinks](searchclientlinks)|This feature is not supported in sandbox.Searches for the client links for the customer of the current authenticated user, filtered by the search criteria.|1 *Predicates*|
|[SearchCustomers](searchcustomers)|Searches for customers that match a specified criteria.|10 *Predicates*|
|[SearchUserInvitations](searchuserinvitations)|Searches for user invitations that match a specified criteria.|1 *Predicates*|
|[SendUserInvitation](senduserinvitation)|Sends an invitation for  a Microsoft account user to manage one or more Bing Ads customer accounts.|1 *UserInvitation*|
|[SignupCustomer](signupcustomer)|Signs up a customer with Bing Ads.|1 *Customer*<br /><br />1 *Account*|
|[UpdateAccount](updateaccount)|Updates the details of the specified account.|1 *Account*|
|[UpdateClientLinks](updateclientlinks)|Updates the status of the specified client links.|10 *ClientLink*|
|[UpdateCustomer](updatecustomer)|Updates the details of the specified customer.|1 *Customer*|
|[UpdateUser](updateuser)|Updates the details of the specified user.|1 *User*|
|[UpdateUserRoles](updateuserroles)|Updates the roles of the specified user.|1 *NewRoleId*<br /><br />1 *UserId*|
