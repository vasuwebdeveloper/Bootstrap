# Issue 1:
Trying to create new token and web url is opening to: https://system.netsuite.com/app/login/secure/authorizetoken.nl?oauth_token=undefined which produces and unexpected error. This is with the current set of Extension Tools. 

# Solution:

**SCA Developer Tools**

In the developer tools source code, open Commons\ns_npm_repository\oauth1\index.js and make the following change:
// Find this
const hostnameStep1 = this.vm ? hostName : `rest${molecule}.netsuite.com`;
 
// And replace it with this
const hostnameStep1 = this.vm ? hostName : `system${molecule}.netsuite.com`;


**Extension Developer Tools**

In the developer tools source code, open ns_npm_repository\oauth1\index.js and make the following change:
// Find this
let hostnameStep1;
if (this.vm) {
    hostnameStep1 = hostName;
} else if (this.account) {
    hostnameStep1 = `${this.account}.restlets.api${molecule}.netsuite.com`;
} else {
    hostnameStep1 = `rest${molecule}.netsuite.com`;
}
 
// And replace it with this
const hostnameStep1 = this.vm ? hostName : `system${molecule}.netsuite.com`;

# Issue 2:
Deployment struck for a long time with the pending status

# Solution: 
open the SC ExtMech Activation List custom record and change the Activation State as ERROR and save It. Using this, you can reactivate the record quickly instead of waiting for a long time.