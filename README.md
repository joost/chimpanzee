# Chimpanzee

SurveyMonkey API (v2) wrapper in Ruby.
NOTE: Current version has some Rails.logger dependencies.

## Installation

Add this line to your application's Gemfile:

    gem 'chimpanzee'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install chimpanzee

## Usage

Add config/initializers/chimpanzee.rb:

    Chimpanzee.configure do |config|
      config.api_key = 'YOUR_KEY'
      config.access_token = 'YOUR_OAUTH_ACCESS_TOKEN' # Use oAuth to authenticate a User and get the token (or via API console)
    end

Perform actions like:

    Chimpanzee::Api2.surveys.get_survey_list # => {"status"=>0, "data"=>{"surveys"=>[{"survey_id"=>"123"}], "page"=>1, "page_size"=>1000}}

## Contributing

1. Fork it ( https://github.com/[my-github-username]/chimpanzee/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request
