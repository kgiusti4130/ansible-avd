=== "Table"

    | Variable | Type | Required | Default | Value Restrictions | Description |
    | -------- | ---- | -------- | ------- | ------------------ | ----------- |
    | [<samp>router_ospf</samp>](## "router_ospf") | Dictionary |  |  |  |  |
    | [<samp>&nbsp;&nbsp;process_ids</samp>](## "router_ospf.process_ids") | List, items: Dictionary |  |  |  |  |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;- id</samp>](## "router_ospf.process_ids.[].id") | Integer | Required, Unique |  |  | OSPF Process ID |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;vrf</samp>](## "router_ospf.process_ids.[].vrf") | String |  |  |  | VRF Name for OSPF Process |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;passive_interface_default</samp>](## "router_ospf.process_ids.[].passive_interface_default") | Boolean |  |  |  |  |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;router_id</samp>](## "router_ospf.process_ids.[].router_id") | String |  |  |  | IPv4 Address |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;distance</samp>](## "router_ospf.process_ids.[].distance") | Dictionary |  |  |  |  |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;external</samp>](## "router_ospf.process_ids.[].distance.external") | Integer |  |  | Min: 1<br>Max: 255 |  |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;inter_area</samp>](## "router_ospf.process_ids.[].distance.inter_area") | Integer |  |  | Min: 1<br>Max: 255 |  |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;intra_area</samp>](## "router_ospf.process_ids.[].distance.intra_area") | Integer |  |  | Min: 1<br>Max: 255 |  |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;log_adjacency_changes_detail</samp>](## "router_ospf.process_ids.[].log_adjacency_changes_detail") | Boolean |  |  |  |  |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;network_prefixes</samp>](## "router_ospf.process_ids.[].network_prefixes") | List, items: Dictionary |  |  |  |  |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- ipv4_prefix</samp>](## "router_ospf.process_ids.[].network_prefixes.[].ipv4_prefix") | String | Required, Unique |  |  |  |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;area</samp>](## "router_ospf.process_ids.[].network_prefixes.[].area") | String |  |  |  |  |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;bfd_enable</samp>](## "router_ospf.process_ids.[].bfd_enable") | Boolean |  |  |  |  |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;bfd_adjacency_state_any</samp>](## "router_ospf.process_ids.[].bfd_adjacency_state_any") | Boolean |  |  |  |  |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;no_passive_interfaces</samp>](## "router_ospf.process_ids.[].no_passive_interfaces") | List, items: String |  |  |  |  |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- &lt;str&gt;</samp>](## "router_ospf.process_ids.[].no_passive_interfaces.[].&lt;str&gt;") | String |  |  |  | Interface Name |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;distribute_list_in</samp>](## "router_ospf.process_ids.[].distribute_list_in") | Dictionary |  |  |  |  |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;route_map</samp>](## "router_ospf.process_ids.[].distribute_list_in.route_map") | String |  |  |  |  |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;max_lsa</samp>](## "router_ospf.process_ids.[].max_lsa") | Integer |  |  |  |  |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;timers</samp>](## "router_ospf.process_ids.[].timers") | Dictionary |  |  |  |  |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;lsa</samp>](## "router_ospf.process_ids.[].timers.lsa") | Dictionary |  |  |  |  |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;rx_min_interval</samp>](## "router_ospf.process_ids.[].timers.lsa.rx_min_interval") | Integer |  |  | Min: 0<br>Max: 600000 | Min interval in msecs between accepting the same LSA |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;tx_delay</samp>](## "router_ospf.process_ids.[].timers.lsa.tx_delay") | Dictionary |  |  |  |  |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;initial</samp>](## "router_ospf.process_ids.[].timers.lsa.tx_delay.initial") | Integer |  |  | Min: 0<br>Max: 600000 | Delay to generate first occurrence of LSA in msecs |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;min</samp>](## "router_ospf.process_ids.[].timers.lsa.tx_delay.min") | Integer |  |  | Min: 1<br>Max: 600000 | Min delay between originating the same LSA in msecs |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;max</samp>](## "router_ospf.process_ids.[].timers.lsa.tx_delay.max") | Integer |  |  | Min: 1<br>Max: 600000 | 1-600000 Maximum delay between originating the same LSA in msec |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;spf_delay</samp>](## "router_ospf.process_ids.[].timers.spf_delay") | Dictionary |  |  |  |  |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;initial</samp>](## "router_ospf.process_ids.[].timers.spf_delay.initial") | Integer |  |  | Min: 0<br>Max: 600000 | Initial SPF schedule delay in msecs |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;min</samp>](## "router_ospf.process_ids.[].timers.spf_delay.min") | Integer |  |  | Min: 0<br>Max: 65535000 | Min Hold time between two SPFs in msecs |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;max</samp>](## "router_ospf.process_ids.[].timers.spf_delay.max") | Integer |  |  | Min: 0<br>Max: 65535000 | Max wait time between two SPFs in msecs |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;default_information_originate</samp>](## "router_ospf.process_ids.[].default_information_originate") | Dictionary |  |  |  |  |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;always</samp>](## "router_ospf.process_ids.[].default_information_originate.always") | Boolean |  |  |  |  |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;metric</samp>](## "router_ospf.process_ids.[].default_information_originate.metric") | Integer |  |  | Min: 1<br>Max: 65535 | Metric for default route |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;metric_type</samp>](## "router_ospf.process_ids.[].default_information_originate.metric_type") | Integer |  |  | Valid Values:<br>- 1<br>- 2 | OSPF metric type for default route |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;summary_addresses</samp>](## "router_ospf.process_ids.[].summary_addresses") | List, items: Dictionary |  |  |  |  |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- prefix</samp>](## "router_ospf.process_ids.[].summary_addresses.[].prefix") | String | Required, Unique |  |  | Summary Prefix Address |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;tag</samp>](## "router_ospf.process_ids.[].summary_addresses.[].tag") | Integer |  |  |  |  |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;attribute_map</samp>](## "router_ospf.process_ids.[].summary_addresses.[].attribute_map") | String |  |  |  |  |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;not_advertise</samp>](## "router_ospf.process_ids.[].summary_addresses.[].not_advertise") | Boolean |  |  |  |  |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;redistribute</samp>](## "router_ospf.process_ids.[].redistribute") | Dictionary |  |  |  |  |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;static</samp>](## "router_ospf.process_ids.[].redistribute.static") | Dictionary |  |  |  |  |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;route_map</samp>](## "router_ospf.process_ids.[].redistribute.static.route_map") | String |  |  |  | Route Map Name |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;include_leaked</samp>](## "router_ospf.process_ids.[].redistribute.static.include_leaked") | Boolean |  |  |  |  |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;connected</samp>](## "router_ospf.process_ids.[].redistribute.connected") | Dictionary |  |  |  |  |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;route_map</samp>](## "router_ospf.process_ids.[].redistribute.connected.route_map") | String |  |  |  | Route Map Name |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;include_leaked</samp>](## "router_ospf.process_ids.[].redistribute.connected.include_leaked") | Boolean |  |  |  |  |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;bgp</samp>](## "router_ospf.process_ids.[].redistribute.bgp") | Dictionary |  |  |  |  |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;route_map</samp>](## "router_ospf.process_ids.[].redistribute.bgp.route_map") | String |  |  |  | Route Map Name |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;include_leaked</samp>](## "router_ospf.process_ids.[].redistribute.bgp.include_leaked") | Boolean |  |  |  |  |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;auto_cost_reference_bandwidth</samp>](## "router_ospf.process_ids.[].auto_cost_reference_bandwidth") | Integer |  |  |  | Bandwidth in mbps |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;areas</samp>](## "router_ospf.process_ids.[].areas") | List, items: Dictionary |  |  |  |  |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- id</samp>](## "router_ospf.process_ids.[].areas.[].id") | String | Required, Unique |  |  |  |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;filter</samp>](## "router_ospf.process_ids.[].areas.[].filter") | Dictionary |  |  |  |  |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;networks</samp>](## "router_ospf.process_ids.[].areas.[].filter.networks") | List, items: String |  |  |  |  |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- &lt;str&gt;</samp>](## "router_ospf.process_ids.[].areas.[].filter.networks.[].&lt;str&gt;") | String |  |  |  | IPv4 Prefix |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;prefix_list</samp>](## "router_ospf.process_ids.[].areas.[].filter.prefix_list") | String |  |  |  | Prefix-List Name |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;type</samp>](## "router_ospf.process_ids.[].areas.[].type") | String |  | `normal` | Valid Values:<br>- normal<br>- stub<br>- nssa |  |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;no_summary</samp>](## "router_ospf.process_ids.[].areas.[].no_summary") | Boolean |  |  |  |  |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;nssa_only</samp>](## "router_ospf.process_ids.[].areas.[].nssa_only") | Boolean |  |  |  |  |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;default_information_originate</samp>](## "router_ospf.process_ids.[].areas.[].default_information_originate") | Dictionary |  |  |  |  |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;metric</samp>](## "router_ospf.process_ids.[].areas.[].default_information_originate.metric") | Integer |  |  | Min: 1<br>Max: 65535 | Metric for default route |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;metric_type</samp>](## "router_ospf.process_ids.[].areas.[].default_information_originate.metric_type") | Integer |  |  | Valid Values:<br>- 1<br>- 2 | OSPF metric type for default route |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;maximum_paths</samp>](## "router_ospf.process_ids.[].maximum_paths") | Integer |  |  | Min: 1<br>Max: 128 |  |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;max_metric</samp>](## "router_ospf.process_ids.[].max_metric") | Dictionary |  |  |  |  |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;router_lsa</samp>](## "router_ospf.process_ids.[].max_metric.router_lsa") | Dictionary |  |  |  |  |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;external_lsa</samp>](## "router_ospf.process_ids.[].max_metric.router_lsa.external_lsa") | Dictionary |  |  |  |  |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;override_metric</samp>](## "router_ospf.process_ids.[].max_metric.router_lsa.external_lsa.override_metric") | Integer |  |  | Min: 1<br>Max: 16777215 |  |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;include_stub</samp>](## "router_ospf.process_ids.[].max_metric.router_lsa.include_stub") | Boolean |  |  |  |  |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;on_startup</samp>](## "router_ospf.process_ids.[].max_metric.router_lsa.on_startup") | String |  |  |  | "wait-for-bgp" or Integer 5-86400<br>Example: "wait-for-bgp" Or "222"<br> |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;summary_lsa</samp>](## "router_ospf.process_ids.[].max_metric.router_lsa.summary_lsa") | Dictionary |  |  |  |  |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;override_metric</samp>](## "router_ospf.process_ids.[].max_metric.router_lsa.summary_lsa.override_metric") | Integer |  |  | Min: 1<br>Max: 16777215 |  |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;mpls_ldp_sync_default</samp>](## "router_ospf.process_ids.[].mpls_ldp_sync_default") | Boolean |  |  |  |  |
    | [<samp>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;eos_cli</samp>](## "router_ospf.process_ids.[].eos_cli") | String |  |  |  | Multiline EOS CLI rendered directly on the Router OSPF process ID in the final EOS configuration |

=== "YAML"

    ```yaml
    router_ospf:
      process_ids:
        - id: <int>
          vrf: <str>
          passive_interface_default: <bool>
          router_id: <str>
          distance:
            external: <int>
            inter_area: <int>
            intra_area: <int>
          log_adjacency_changes_detail: <bool>
          network_prefixes:
            - ipv4_prefix: <str>
              area: <str>
          bfd_enable: <bool>
          bfd_adjacency_state_any: <bool>
          no_passive_interfaces:
            - <str>
          distribute_list_in:
            route_map: <str>
          max_lsa: <int>
          timers:
            lsa:
              rx_min_interval: <int>
              tx_delay:
                initial: <int>
                min: <int>
                max: <int>
            spf_delay:
              initial: <int>
              min: <int>
              max: <int>
          default_information_originate:
            always: <bool>
            metric: <int>
            metric_type: <int>
          summary_addresses:
            - prefix: <str>
              tag: <int>
              attribute_map: <str>
              not_advertise: <bool>
          redistribute:
            static:
              route_map: <str>
              include_leaked: <bool>
            connected:
              route_map: <str>
              include_leaked: <bool>
            bgp:
              route_map: <str>
              include_leaked: <bool>
          auto_cost_reference_bandwidth: <int>
          areas:
            - id: <str>
              filter:
                networks:
                  - <str>
                prefix_list: <str>
              type: <str>
              no_summary: <bool>
              nssa_only: <bool>
              default_information_originate:
                metric: <int>
                metric_type: <int>
          maximum_paths: <int>
          max_metric:
            router_lsa:
              external_lsa:
                override_metric: <int>
              include_stub: <bool>
              on_startup: <str>
              summary_lsa:
                override_metric: <int>
          mpls_ldp_sync_default: <bool>
          eos_cli: <str>
    ```
