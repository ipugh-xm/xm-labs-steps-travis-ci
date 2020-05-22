# Travis CI Steps

This step allows you to get the commit details from a given repo and user. Great for enriching notifications with relevant code commit information. 


---------

<kbd>
  <img src="https://github.com/xmatters/xMatters-Labs/raw/master/media/disclaimer.png">
</kbd>

---------

# Files

* [TravisCISteps.zip](TravisCISteps.zip) - Workflow zip file with the step and example flow
* [travisci.png](/travisci.png) - Travis CI logo

# How it works
This step posts a request to Travis CI to build a branch of a Git repository.


# Installation

## Travis CI Setup
This requires a Travis CI account.
1. Go to **Account > Settings**.
2. Find your API key in the **Settings** tab.

## xMatters Setup
1. Download the [TravisCISteps.zip](TravisCISteps.zip) file onto your local computer
2. Navigate to the Workflows tab of your xMatters instance
3. Click Import, and select the zip file you just downloaded
4. Adjust the **Travis CI** endpoint. `https://api.travis-ci.org/repo` or `https://api.travis-ci.com/repo`
5. Add a constant for your API Key.


## Usage
The **Travis CI - Trigger Build** step is now available in your custom steps. So navigate to the appropriate canvas so you can add the step there. If you'd like to experiment with it, the **Trigger Build** workflow has a canvas that can be triggered via HTTP call. 

### Inputs
| Name  | Required? | Min | Max | Help Text | Default Value | Multiline |
| ----- | ----------| --- | --- | --------- | ------------- | --------- |
| API Token | Yes | 0 | 2000 | Personal API Token for Travis CI | | No |
| Repository | Yes | 0 | 2000 | Full repo name `user/repo` | | No |
| Branch | Yes | 0 | 2000 | Branch to build from | master | No |


### Outputs

| Name | Description |
| ---- | ----------  |
| results | results of the API request |



## Example
This is an example of the **Travis CI - Trigger Build** step being triggered by an HTTP Trigger.

<kbd>
	<img src="/media/ExampleFlow.png">
</kbd>

