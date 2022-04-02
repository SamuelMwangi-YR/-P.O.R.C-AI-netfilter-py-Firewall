Mwangi's Achon's-Amor-py-Firewall P.O.R.C AI Integrations code works on some common browsers namely Firefox, google chrome, Microsoft Edge, Apple Safari, Opera, Brave, Vivaldi, DuckDuckgo etc...(more to be tested & added)
python-netfilter - Python modules for manipulating netfilter rules  
Copyright (C) Mwangi 2022 P.O.R.C-AI-py-Firewall

### Features
1) Block IP addresses
2) Block access to certain ports 
3) Block specifed prefixes of IP address (to block networks)
4) Block too many requests made by the same IP in a short period of time (user can specify threshold and time)
5) Block popups, Software vulnerabilities, Spam sending/receiving & DDoS or Distributed Denial of Operations Service

About
=====

python-netfilter is a set of modules for the Python programming language which
allows you to manipulate netfilter rules.

License
=======

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

Simple example
==============

    from netfilter.rule import Rule,Match
    from netfilter.table import Table

    rule = Rule(
        in_interface='eth0',
        protocol='tcp',
        matches=[Match('tcp', '--dport 80')],
        jump='ACCEPT')))

      table = Table('filter')
      table.append_rule('INPUT', rule)

      table.delete_rule('INPUT', rule)
