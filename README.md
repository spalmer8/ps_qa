ps_qa
=====

Experimental Repo for the QA team at PS.


Installation
============

      # Install Ruby
      curl -L https://get.rvm.io | bash -s stable --ruby
      
      # Install Gherkin
      gem install gherkin
      
      # Install Cucumber
      gem install cucumber
       
      # Install Cucumber
      gem install rspec


Naming Conventions
==================

Please make sure we have the PS component name as a directory under this repo.
i.e.:

      /ps_qa/corporate_portal/
      /ps_qa/shipment_server/
      /ps_qa/rails_base/trunk/   # (aka Yardhound)


Under each component should be a directory named features and within the feautes directory should be a sub directory called step_definitions.

i.e.:
      /ps_qa/rails_base/trunk/features/step_definitions


In the features directory place your appropriately named feature file in the format:

      descriptive_functional_area.feature


In the step_definitions directory place your appropriately named steps file in the format:

      descriptive_functional_area_steps.rb


To see if your tests work go to the directory above the features directory and run:

      cucumber

The example contained within in this repo should display something like:

      $ pwd
      .../ps_qa/HelloCucumber
      
      $ cucumber

      Feature: Hello World Feature
        In order to ensure that my installation works
        As a Developer
        I want to run a quick Cucumber test
      
        Scenario: Hello World Scenario      # features/basic.feature:6
          Given The Action is Hello         # features/step_definitions/basic_steps.rb:3
           When The Subject is World         # features/step_definitions/basic_steps.rb:7
          Then The Greeting is Hello, World # features/step_definitions/basic_steps.rb:11
      
       1 scenario (1 passed)
       3 steps (3 passed)
       0m0.003s

For more information, please refer to PS QA Cucumber / Gherkin  documentation off the wush.net wiki page.
