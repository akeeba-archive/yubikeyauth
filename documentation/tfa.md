# About Two Factor Authentication

## What is Two Factor Authentication (TFA)?

Two factor authentication is generally considered more secure than one factor authentication. In two factor authentication the users needs to use something they _know_ (username and password) and something they _have_, typically an ever-changing code or secure signature generated by a device of some kind. This is more resilient than single factor authentication of any kind. If the user's password is intercepted / stolen / guessed the attacker cannot gain access to the site as they do not have the device generating the additional code. Likewise, if the device is lost / stolen the attacker cannot gain access to the site as they do not know the username and/or password of the user.

## Should I use TFA?

You might be thinking that you don't need TFA because your site isn't really worth all that much. You are wrong. Any site is valuable to malicious hackers. They want to break into your site and have it serve malware or send spam emails which bring them illicit income. This means that every site *is* a target. 

Have you ever logged in to your site from a Wi-Fi connection you don't own, such as a café, airport or hotel? Have you ever used someone else's computer, tablet or smartphone to log in to your site? It is possible that malware installed in any of these Wi-Fi network devices or computer, unbeknownst to their owners, has snooped your username and password and reported it to one of those malicious hackers. Adding TFA is a sensible method to prevent your site from being hijacked even in these circumstances.

The same applies to your site's visitors. Humans tend to choose weak passwords and reuse them all over the place. It's very likely that their password was stolen somewhere else and the attacker uses it to impersonate your users on your site. The effects could vary from mild annoyance to severe issues for your users, depending on the services your site is providing. Better be safe than sorry and let your users set up TFA on their accounts. All major Internet companies –Facebook, Google, Apple etc– do that and so can you. All you need is the latest Joomla! 3 version and the TFA plugins.

## Which methods are supported by your plugins?

The plugins we have created support three different methods for Two Factor Authentication. From least to most secure they are:

* [Time-based One Time Passwords](http://en.wikipedia.org/wiki/Time-based_One-time_Password_Algorithm#Client_implementations) such as Google Authenticator, Authy, etc. These are typically implemented as smartphone / desktop applications. They generate a 6 digit PIN which changes every 30 seconds. It's hard to guess, nearly impossible to clone without knowing the secret key used to generate the code, require no additional hardware (you already own a smartphone, tablet or computer) but you need to type in the code yourself.

* [YubiKey](https://www.yubico.com/products/yubikey-hardware/yubikey-2/). This is a secure hardware token that the user needs to plug in to a USB socket and touch its button or, in the case of the NFC-equipped version, get it in close proximity to the mobile device logging in to the site. This is a very secure method for Two Factor Authentication.
 
* [U2F (Universal Second Factor)](https://www.yubico.com/products/yubikey-hardware/fido-u2f-security-key/). This is the incumbent standard for two factor authentication. You plug in this hardware token into a USB socket and touch its button when prompted. This will generate a very secure cryptographic signature which can *only* be verified by the site requesting the second factor authentication. It's even more secure than plain YubiKey. You can also find [cheaper, standards compliant](http://www.amazon.com/Plug-up-International-U2F-SK-01-FIDO-Security/dp/B00OGPO3ZS) devices which work under this scheme.
