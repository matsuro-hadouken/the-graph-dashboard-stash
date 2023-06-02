# Heavily Tuned Grafana Dashboards for The Graph Indexer Stack

As the MIP program comes to an end this month, and we are moving towards production deployment, it is essential to preserve these dashboards for future use. 

When our team arrived for the MIP program, we had only a very basic knowledge of the stack. Through the MIP campaign, we have been learning all aspects of the architecture in depth from scratch. This process requires a lot of monitoring, as well as building tools to monitor seemingly unmonitorable things _(of which there are plenty)_. 

This collection is a heavily modified version of dashboards we found across various internet resources such as chats, old deprecated guides, and Github repositories lacking maintenance. The initial dashboards we found were very basic and built for specific environments, some supporting old, vulnerable Grafana versions. The dashboards in this repository are upgrades; many custom plots have been added for in-depth debugging and analytics.

Some dashboards contain data provided by node_exporter for tracking correlations in one place. Dashboards also share the same data from various sources for quick debugging and comparison without switching. 

Statistics can be easily observed in the selected `$range` instead of _"since last restart"_ and similar unreliable time frames.

* `endpoints_and_network_a3mc_exporter-grafana-dashboard.json`

Custom exporter built by ART3MIS.CLOUD | [screenshot](https://raw.githubusercontent.com/matsuro-hadouken/the-graph-dashboard-stash/main/screenshots/test-endpoints-network.png) |  [exporter repository](https://github.com/a3mc/graph-toolbox/tree/master/graph-prom-exporter) |

* `firehose-modified-grafana-dashboard.json`

Early firehose metrics modified to accept more host variables, cleaned up some variable names for better visibility, added extra plots for alerting. | [screenshot](https://raw.githubusercontent.com/matsuro-hadouken/the-graph-dashboard-stash/main/screenshots/firehose.png) |

* `indexing-performance-metrics-modified-grafana-dashboard.json`

Reworked Indexer Performance dashboard, lots of refactoring, optimized for debugging. Chain trackers for all MIP chains integrated, allows easy alerting and latency observation for each archive connection. | [screenshot](https://raw.githubusercontent.com/matsuro-hadouken/the-graph-dashboard-stash/main/screenshots/indexing-performance.png) |

* `main-face-autoagora-debug-grafana-dashboard.json`

All-in-one Indexer Face based on Autoagora and additional modules. | [screenshot](https://raw.githubusercontent.com/matsuro-hadouken/the-graph-dashboard-stash/main/screenshots/autoagora.png) |

* `query-performance-modified-grafana-dashboard.json`

Heavily refactored Query Performance dashboard, optimized for debugging. | [screenshot](https://raw.githubusercontent.com/matsuro-hadouken/the-graph-dashboard-stash/main/screenshots/query-performance.png) |

WARNING: These dashboards are not beginner-friendly _(probably, needs testing, we don't know)_ and require a good understanding of the [Grafana] / [Prometheus] combo. Some things may not work out of the box _(perhaps)_, sources need to be set properly. This collection is the result of intense work over many months due to the MIP competition battle, where we had to solve complex puzzles on the fly. Bringing this repository to a user-friendly state will take some more time.