# Learning Elasticsearch
[ES Book](https://www.elastic.co/guide/en/elasticsearch/guide/current/index.html)

These notes are based on my experiences with learning Elasticsearch from the tutorial on [Elastic](https://www.elastic.co).

## Part 1: Setting up Elasticsearch

On MacOS, Elasticsearch can be installed using Homebrew:  
`$ brew install elasticsearch`  

Elasticsearch can be launched in the following two ways:  
1. Using `launchd` to start Elasticsearch and restart upon login as a background service:  
`$ brew services start elasticsearch`
2. If Elasticsearch does not need to be run as a background service:  
`$ elasticsearch`  

More information can be found [here](https://www.elastic.co/guide/en/elasticsearch/reference/current/brew.html).

### Additional: Setting up Kibana  
On MacOS, Kibana can be installed using Homebrew:  
`$ brew install kibana`  

Kibana can be launched in the following two ways:  
1. Using `launchd` to start Kibana and restart upon login as a background service:  
`$ brew services start kibana`
2. If Kibana does not need to be run as a background service:  
`$ kibana`  

More information can be found [here](https://www.elastic.co/guide/en/kibana/current/brew.html).