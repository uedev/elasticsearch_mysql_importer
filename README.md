# elasticsearch_mysql_importer [![Build Status](https://travis-ci.org/y-ken/elasticsearch_mysql_importer.png?branch=master)](https://travis-ci.org/y-ken/elasticsearch_mysql_importer)

It is importing from mysql table with SQL to elasticsearch. Not only that, it could generating nested documents.

## Install

Add this line to your application's Gemfile:

    gem 'elasticsearch_mysql_importer'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install elasticsearch_mysql_importer

## Usage

    # Clone repository
    $ git clone https://github.com/y-ken/elasticsearch_mysql_importer.git
    $ cd elasticsearch_mysql_importer
    $ bundle install --path vendor/bundle
    
    # Setup mysql connection and query
    $ vim example.rb
    
    # Execute script, then it outputs result into ./requests.json
    $ bundle exec ruby example/example.rb 
    
    # Index document for elasticsearch if you didn't call 'write_elasticsearch' in example.rb
    $ curl -s -XPOST localhost:9200/_bulk --data-binary @example/requests.json

## TODO

Pull requests are very welcome!!

* support thread
* support CLI command

## Contributing

1. Fork it ( https://github.com/y-ken/elasticsearch_mysql_importer/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request

## Copyright

Copyright © 2014- Kentaro Yoshida ([@yoshi_ken](https://twitter.com/yoshi_ken))

## License

MIT License
