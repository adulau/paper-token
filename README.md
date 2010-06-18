paper token
===========

paper token is a PDF generator to create paper-based OTP (RFC 4226) token.

why?
----

Hardware tokens are very costly and often require a proprietary infrastructure.
(near impossible to find HOTP-compatible hardware token without 
requiring the linked proprietary infrastructure)
Software tokens can be also painful and always require a second device like
a phone to operate properly.

security?
---------

Paper is not less secure than a phone running a software token. With
a sheet paper and a pencil, you have the control of the token. Do you
have the control of your phone and the software running on it? 

For a negligible cost, you have a token and you just need to protect
that sheet of paper. It's simple.

An OTP is just an one-time password and this recommendation makes a
lot of sense for the paper-based token too :

"Simply, people can no longer remember passwords good enough to reliably defend against dictionary attacks, and are much more secure if they choose a password too complicated to remember and then write it down. We're all good at securing small pieces of paper. I recommend that people write their passwords down on a small piece of paper, and keep it with their other valuable small pieces of paper: in their wallet. —Bruce Schneier 2005"

perl requirements
-----------------

* Authen::HOTP
* PDF::API2
* PDF::Table
* Getopt::Compact

how to use it
=============

perl paper-token.pl  --output test.pdf --counter 0 --end 200 --secret 3132333435363738393031323334353637383930 --digits 6

paper token - http://www.foo.be/paper-token/ v0.1
usage: paper-token.pl [options] 
options                                                                            
-h, --help      This help message                                                  
-s, --secret    Secret of the token in hex format - default is RFC 4226 test vector
-o, --output    Output filename                                                    
-c, --counter   Starting counter - default is 0                                    
-e, --end       Ending counter - default is 500                                    
-w, --window    Window of authentication (one line) - default is 14                
-d, --digits    Digits showed per OTP value - default is 6 - dec31.6               
    --man       Display documentation     

sample token (PDF)
==================

* [Sample token using test vector from RFC 4226](http://github.com/adulau/paper-token/raw/master/examples/test.pdf)

OpenOTP server installation
===========================
You have various free software solution to run
on the server side for the authentication of the
tokens. You can have a look at the setting up
of an OpenOTP server to work with those paper-based
token.

* [For more information](http://www.foo.be/cgi-bin/wiki.pl/SettingOOTP)

LICENSE
=======
    
Copyright (C) 2010 Alexandre Dulaunoy, http://www.foo.be/

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.

