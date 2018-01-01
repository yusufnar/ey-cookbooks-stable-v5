# Hello World,1-2

This example demonstrates the minimum effort required to add a NEW custom cookbook. The `hello_wold1` and The `hello_wold2` cookbooks do nothing other than output "Hello World1" and "Hello World2" to the chef log. It can also be used to validate that custom cookbooks are working properly.

Steps to use this example:

1. Setup an environment
2. Run `ey-core recipes upload --environment=<nameofenvironment> --file=<pathtocookbooksfolder> --apply --verbose`
    * The `ey-core` executable can be obtained by installing the [ey-core](https://github.com/engineyard/core-client-rb) gem locally.

This example consists of 2 cookbooks:

1. The `ey_custom` cookbook. This cookbook is already included with the main chef run, but does nothing by default. It exists for the purpose of being overriden by customers for custom chef. In this example we override `cookbooks/ey-custom/metadata.rb` and `cookbooks/ey-custom/recipes/before-main.rb` to invoke the `hello_world1` cookbook and the `hello_world2` cookbook
3. The `hello_word1` cookbook and The `hello_word2` cookbook. This cookbooks include the bare minimum: a `metadata.rb` file and a `default.rb` recipe. (the log output line is in the default recipe).
