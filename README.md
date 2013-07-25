# BankJob

TODO: Write a gem description

## Installation


    git clone git@github.com:kkosuge/bank_job.git
    cd bank_job
    rake install
    

## Usage

    require 'bank_job'
    
    bj = BankJob.new

    bj.register do |bank|
      bank.strategy = BankJob::Strategy::SMBC.new
      bank.number   = '0123456789'
      bank.pin      = '01234'
    end

    p bj.agents.first.deposits #=> 100円
    
## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request