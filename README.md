paper token
===========

paper token is a PDF generator to create paper-based OTP token.

perl requirements
-----------------

* Authen::HOTP
* PDF::API2
* PDF::Table
* Getopt::Compact

how to use it
=============

perl paper-token.pl  --output test.pdf --counter 0 --end 200 --secret 3132333435363738393031323334353637383930 --digits 6

OpenOTP server installation
===========================

* For more information - http://www.foo.be/cgi-bin/wiki.pl/SettingOOTP

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

