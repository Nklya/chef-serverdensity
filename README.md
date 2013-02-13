# chef-serverdensity

## Description

This cookbook provides an easy way to install the [Server Density agent](https://github.com/serverdensity/sd-agent/).

## Requirements

### Cookbooks:

This cookbook has dependencies on the following cookbooks:

 * [apt](https://github.com/opscode-cookbooks/apt)
 * [yum::epel](https://github.com/opscode-cookbooks/yum)

### Platforms:

 * Ubuntu
 * Debian
 * RHEL
 * CentOS
 * Fedora

## Attributes

 * `node['serverdensity']['agent_key']` - Your Server Density agent key
 * `node['serverdensity']['sd_url']` - Your Server Density subdomain, prefixed with either `http://` or `https://`

## Usage

 1. Include `recipe[serverdensity]` in a run list to implicly run `recipe[serverdensity::install]`

 2. Then:
  * Override the attribute on a [higher level](http://wiki.opscode.com/display/chef/Attributes#Attributes-AttributesPrecedence) *recommended*
  * **or** change the `node['serverdensity']['agent_key']` attribute to your Server Density agent key

## References

 * [Server Density home page](http://www.serverdensity.com/)
 * [akatz/chef-serverdensity](https://github.com/akatz/chef-serverdensity)
 * [Jonty/chef-serverdensity](https://github.com/Jonty/chef-serverdensity)


## Authors

 * Original Author: Avrohom Katz <iambpentameter@gmail.com>
 * Modified by: Jonty Wareing <jonty@jonty.co.uk>
 * Modified further by: Server Density <hello@serverdensity.com>

## License

Copyright Avrohom Katz: 2012

Unless otherwise noted, all files are released under the MIT license,
possible exceptions will contain licensing information in them.

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
