# Dreamforce 23 - Adopt Package Based Development with Org-Dependent Packaging

Repository for the "Happy Soup" org metadata from my Dreamforce 23 theatre session.
The "Happy Soup" refers to the metadata present in a Salesforce instance has been
developed over the years in an unmanaged fashion - multiple point solutions to solve
specific business problems. 

## Installation

To deploy the metadata to your org, execute :

`sf project deploy start {-o <username>}`

where `<username>` is the username for the org you want to install the package into, that you have previously authenticated using the CLI.

Assign yourself the publishing administrator permissionset

`sf org assign permset -n PublishingAdmin {-o <username>}`

Create some sample data : 
`sf apex run {-o <username>}`
`> BookStoreSampleData.CreateBookStoreSampleData();`

Then login to the org, go to the Store Search tab and search for some books.

Then install the org-dependent package - you can find details of this in the package repo : [https://github.com/keirbowden/DF23Package](https://github.com/keirbowden/DF23Package)