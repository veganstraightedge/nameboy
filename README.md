# nameboy

http://github.com/veganstraightedge/nameboy

## DESCRIPTION

Batch edit passwords for domains managed at
[http://access.enom.com](http://access.enom.com)

## FEATURES/PROBLEMS

* change all of your domain passwords in one command
* is not interactive
* all domains passwords must be the same at the start
* all domains passwords will end up the same

## SYNOPSIS

    nameboy enom:password current_password new_password https://raw.github.com/veganstraightedge/nameboy/master/domains.txt

## REQUIREMENTS

* ruby
* rubygems
* mechanize
* domains at [http://access.enom.com](http://access.enom.com)
* internet access

## INSTALL

* sudo gem install nameboy

## DEVELOPERS

After checking out the source, run

    rake newb

This task will install any missing dependencies, run the tests/specs,
and generate the RDoc.

## LICENSE

**PUBLIC DOMAIN**.
Your heart is as free as the air you breathe.
The ground you stand on is liberated territory.

## Usage

### Help

    nameboy
    nameboy -h
    nameboy help

Prints this help text

### Namespace:Action

    nameboy enom:password

For now, this is the only action.
There are plans for more, thus the namespace.

### Change Passwords

    nameboy enom:password current_password new_password domains_file_url

      current_password : what you use to log into access.enom.com
          new_password : what you use to log into access.enom.com
      domains_file_url : publicly accessible url of a plain text listing of domains

This will change all of the domains' passwords listed in `domains_file_url`
from `current_password` to `new_password`.

### Change Passwords

    nameboy enom:password current_password new_password domains_file_url -l

      -l : turns on the Logger with STDERR

Handy for debugging.

### Example domains.txt

    example.com
    example.org
    example.net

**Note** The file name can be anything, not just `domains.txt`.

### Example

    nameboy enom:password foo bar https://raw.github.com/veganstraightedge/nameboy/master/domains.txt
