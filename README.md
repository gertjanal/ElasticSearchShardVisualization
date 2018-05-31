# ElasticSearch shards distribution visualization

Live demo available at: [gertjanal.github.io/ElasticSearchShardVisualization](https://gertjanal.github.io/ElasticSearchShardVisualization)

## Introduction
At one point, we reached the ElasticSearch cluster nodes limits in terms of disk and memory usage.
After adding new nodes, we saw that too much of the shards on the old data nodes moved to the new nodes.
This made the cluster very unhealthy.

For more insight, I created a visualization for shards per index per data node. After removing some old indices, ES was able to repair itself, what can be seen in the visualization.
To create your own visualization, export the json from `/_cat/shards?format=json&h=index,node` (or run a script that exports this including a datestamp)

![Screenshot.png](https://raw.githubusercontent.com/gertjanal/ElasticSearchShardVisualization/master/Screenshot.png)
