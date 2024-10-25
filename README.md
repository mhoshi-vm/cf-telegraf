# Prereq
- VM with cf cli installed
- Install telegraf
- cf authenticated via `cf login`

# Exec
```
telegraf --config telegraf.conf &
```

Check metrics

```
curl http://[::]:9273/metrics
```

# Metrics sample
```
# HELP cf_app_usage_events_instance_count_current Telegraf collected metric
# TYPE cf_app_usage_events_instance_count_current untyped
cf_app_usage_events_instance_count_current{app_guid="00432c36-b10d-4ac1-858c-2adeaca17dc1",app_name="autoscale",host="jump",organization_guid="6d496114-f7d9-416e-9820-5bd14e0a3858",space_guid="9da31a1e-1507-44b4-bbec-241e60aa360c",space_name="autoscaling",state_current="STAGING_STARTED"} 1
cf_app_usage_events_instance_count_current{app_guid="4f9a7c5d-5f8f-480e-87b4-7df3ecc0709a",app_name="apps-manager-js-green",host="jump",organization_guid="6d496114-f7d9-416e-9820-5bd14e0a3858",space_guid="e793e930-5ac6-4785-a120-eb37a4f81d44",space_name="system",state_current="STAGING_STARTED"} 1
cf_app_usage_events_instance_count_current{app_guid="565637ce-d8dd-4284-b44d-83b14decc939",app_name="app-usage-scheduler",host="jump",organization_guid="6d496114-f7d9-416e-9820-5bd14e0a3858",space_guid="e793e930-5ac6-4785-a120-eb37a4f81d44",space_name="system",state_current="STARTED"} 1
cf_app_usage_events_instance_count_current{app_guid="832b3991-760d-4f48-95db-4f91701de210",app_name="app-usage-server",host="jump",organization_guid="6d496114-f7d9-416e-9820-5bd14e0a3858",space_guid="e793e930-5ac6-4785-a120-eb37a4f81d44",space_name="system",state_current="STARTED"} 2
cf_app_usage_events_instance_count_current{app_guid="97d24286-88a9-45dc-ba4c-0245fe9f11d4",app_name="app-usage-worker",host="jump",organization_guid="6d496114-f7d9-416e-9820-5bd14e0a3858",space_guid="e793e930-5ac6-4785-a120-eb37a4f81d44",space_name="system",state_current="STARTED"} 1
cf_app_usage_events_instance_count_current{app_guid="9fde6c0e-f748-46e1-87f0-65587a2ff558",app_name="autoscale-api",host="jump",organization_guid="6d496114-f7d9-416e-9820-5bd14e0a3858",space_guid="9da31a1e-1507-44b4-bbec-241e60aa360c",space_name="autoscaling",state_current="STAGING_STARTED"} 1
cf_app_usage_events_instance_count_current{app_guid="b947616d-f461-469b-96fd-27e8da9f11b6",app_name="search-server-green",host="jump",organization_guid="6d496114-f7d9-416e-9820-5bd14e0a3858",space_guid="e793e930-5ac6-4785-a120-eb37a4f81d44",space_name="system",state_current="STAGING_STARTED"} 1
cf_app_usage_events_instance_count_current{app_guid="c44721bf-d60c-4b48-9b12-694029796c04",app_name="p-invitations-green",host="jump",organization_guid="6d496114-f7d9-416e-9820-5bd14e0a3858",space_guid="e793e930-5ac6-4785-a120-eb37a4f81d44",space_name="system",state_current="STAGING_STARTED"} 1
cf_app_usage_events_instance_count_current{app_guid="db453a87-ca42-4b38-90c6-5e457254ab67",app_name="notifications-ui",host="jump",organization_guid="6d496114-f7d9-416e-9820-5bd14e0a3858",space_guid="edf5f169-56cf-411b-9edd-9fdd7d6bbcf7",space_name="notifications-with-ui",state_current="STAGING_STARTED"} 1
cf_app_usage_events_instance_count_current{app_guid="e22762ca-891f-406d-8d73-da7c027f0f58",app_name="nfsbroker",host="jump",organization_guid="6d496114-f7d9-416e-9820-5bd14e0a3858",space_guid="f25ff7ef-06a1-44f8-b0f5-957e606f17e7",space_name="nfs",state_current="STAGING_STARTED"} 1
cf_app_usage_events_instance_count_current{app_guid="ebd1a08c-09e5-46e6-a8ea-e9fb4fd67028",app_name="app-31216",host="jump",organization_guid="6d496114-f7d9-416e-9820-5bd14e0a3858",space_guid="c48c9fbd-14c7-4166-85fb-4d97327ab372",space_name="space-5745",state_current="STAGING_STARTED"} 1
# HELP cf_app_usage_events_instance_count_previous Telegraf collected metric
# TYPE cf_app_usage_events_instance_count_previous untyped
cf_app_usage_events_instance_count_previous{app_guid="00432c36-b10d-4ac1-858c-2adeaca17dc1",app_name="autoscale",host="jump",organization_guid="6d496114-f7d9-416e-9820-5bd14e0a3858",space_guid="9da31a1e-1507-44b4-bbec-241e60aa360c",space_name="autoscaling",state_current="STAGING_STARTED"} 1
cf_app_usage_events_instance_count_previous{app_guid="4f9a7c5d-5f8f-480e-87b4-7df3ecc0709a",app_name="apps-manager-js-green",host="jump",organization_guid="6d496114-f7d9-416e-9820-5bd14e0a3858",space_guid="e793e930-5ac6-4785-a120-eb37a4f81d44",space_name="system",state_current="STAGING_STARTED"} 1
cf_app_usage_events_instance_count_previous{app_guid="565637ce-d8dd-4284-b44d-83b14decc939",app_name="app-usage-scheduler",host="jump",organization_guid="6d496114-f7d9-416e-9820-5bd14e0a3858",space_guid="e793e930-5ac6-4785-a120-eb37a4f81d44",space_name="system",state_current="STARTED"} 1
cf_app_usage_events_instance_count_previous{app_guid="832b3991-760d-4f48-95db-4f91701de210",app_name="app-usage-server",host="jump",organization_guid="6d496114-f7d9-416e-9820-5bd14e0a3858",space_guid="e793e930-5ac6-4785-a120-eb37a4f81d44",space_name="system",state_current="STARTED"} 2
cf_app_usage_events_instance_count_previous{app_guid="97d24286-88a9-45dc-ba4c-0245fe9f11d4",app_name="app-usage-worker",host="jump",organization_guid="6d496114-f7d9-416e-9820-5bd14e0a3858",space_guid="e793e930-5ac6-4785-a120-eb37a4f81d44",space_name="system",state_current="STARTED"} 1
cf_app_usage_events_instance_count_previous{app_guid="9fde6c0e-f748-46e1-87f0-65587a2ff558",app_name="autoscale-api",host="jump",organization_guid="6d496114-f7d9-416e-9820-5bd14e0a3858",space_guid="9da31a1e-1507-44b4-bbec-241e60aa360c",space_name="autoscaling",state_current="STAGING_STARTED"} 1
cf_app_usage_events_instance_count_previous{app_guid="b947616d-f461-469b-96fd-27e8da9f11b6",app_name="search-server-green",host="jump",organization_guid="6d496114-f7d9-416e-9820-5bd14e0a3858",space_guid="e793e930-5ac6-4785-a120-eb37a4f81d44",space_name="system",state_current="STAGING_STARTED"} 1
cf_app_usage_events_instance_count_previous{app_guid="c44721bf-d60c-4b48-9b12-694029796c04",app_name="p-invitations-green",host="jump",organization_guid="6d496114-f7d9-416e-9820-5bd14e0a3858",space_guid="e793e930-5ac6-4785-a120-eb37a4f81d44",space_name="system",state_current="STAGING_STARTED"} 1
cf_app_usage_events_instance_count_previous{app_guid="db453a87-ca42-4b38-90c6-5e457254ab67",app_name="notifications-ui",host="jump",organization_guid="6d496114-f7d9-416e-9820-5bd14e0a3858",space_guid="edf5f169-56cf-411b-9edd-9fdd7d6bbcf7",space_name="notifications-with-ui",state_current="STAGING_STARTED"} 1
cf_app_usage_events_instance_count_previous{app_guid="e22762ca-891f-406d-8d73-da7c027f0f58",app_name="nfsbroker",host="jump",organization_guid="6d496114-f7d9-416e-9820-5bd14e0a3858",space_guid="f25ff7ef-06a1-44f8-b0f5-957e606f17e7",space_name="nfs",state_current="STAGING_STARTED"} 1
cf_app_usage_events_instance_count_previous{app_guid="ebd1a08c-09e5-46e6-a8ea-e9fb4fd67028",app_name="app-31216",host="jump",organization_guid="6d496114-f7d9-416e-9820-5bd14e0a3858",space_guid="c48c9fbd-14c7-4166-85fb-4d97327ab372",space_name="space-5745",state_current="STAGING_STARTED"} 1
# HELP cf_app_usage_events_memory_in_mb_per_instance_current Telegraf collected metric
# TYPE cf_app_usage_events_memory_in_mb_per_instance_current untyped
cf_app_usage_events_memory_in_mb_per_instance_current{app_guid="00432c36-b10d-4ac1-858c-2adeaca17dc1",app_name="autoscale",host="jump",organization_guid="6d496114-f7d9-416e-9820-5bd14e0a3858",space_guid="9da31a1e-1507-44b4-bbec-241e60aa360c",space_name="autoscaling",state_current="STAGING_STARTED"} 1024
cf_app_usage_events_memory_in_mb_per_instance_current{app_guid="4f9a7c5d-5f8f-480e-87b4-7df3ecc0709a",app_name="apps-manager-js-green",host="jump",organization_guid="6d496114-f7d9-416e-9820-5bd14e0a3858",space_guid="e793e930-5ac6-4785-a120-eb37a4f81d44",space_name="system",state_current="STAGING_STARTED"} 1024
cf_app_usage_events_memory_in_mb_per_instance_current{app_guid="565637ce-d8dd-4284-b44d-83b14decc939",app_name="app-usage-scheduler",host="jump",organization_guid="6d496114-f7d9-416e-9820-5bd14e0a3858",space_guid="e793e930-5ac6-4785-a120-eb37a4f81d44",space_name="system",state_current="STARTED"} 1024
cf_app_usage_events_memory_in_mb_per_instance_current{app_guid="832b3991-760d-4f48-95db-4f91701de210",app_name="app-usage-server",host="jump",organization_guid="6d496114-f7d9-416e-9820-5bd14e0a3858",space_guid="e793e930-5ac6-4785-a120-eb37a4f81d44",space_name="system",state_current="STARTED"} 1024
cf_app_usage_events_memory_in_mb_per_instance_current{app_guid="97d24286-88a9-45dc-ba4c-0245fe9f11d4",app_name="app-usage-worker",host="jump",organization_guid="6d496114-f7d9-416e-9820-5bd14e0a3858",space_guid="e793e930-5ac6-4785-a120-eb37a4f81d44",space_name="system",state_current="STARTED"} 2048
cf_app_usage_events_memory_in_mb_per_instance_current{app_guid="9fde6c0e-f748-46e1-87f0-65587a2ff558",app_name="autoscale-api",host="jump",organization_guid="6d496114-f7d9-416e-9820-5bd14e0a3858",space_guid="9da31a1e-1507-44b4-bbec-241e60aa360c",space_name="autoscaling",state_current="STAGING_STARTED"} 1024
cf_app_usage_events_memory_in_mb_per_instance_current{app_guid="b947616d-f461-469b-96fd-27e8da9f11b6",app_name="search-server-green",host="jump",organization_guid="6d496114-f7d9-416e-9820-5bd14e0a3858",space_guid="e793e930-5ac6-4785-a120-eb37a4f81d44",space_name="system",state_current="STAGING_STARTED"} 1024
cf_app_usage_events_memory_in_mb_per_instance_current{app_guid="c44721bf-d60c-4b48-9b12-694029796c04",app_name="p-invitations-green",host="jump",organization_guid="6d496114-f7d9-416e-9820-5bd14e0a3858",space_guid="e793e930-5ac6-4785-a120-eb37a4f81d44",space_name="system",state_current="STAGING_STARTED"} 1024
cf_app_usage_events_memory_in_mb_per_instance_current{app_guid="db453a87-ca42-4b38-90c6-5e457254ab67",app_name="notifications-ui",host="jump",organization_guid="6d496114-f7d9-416e-9820-5bd14e0a3858",space_guid="edf5f169-56cf-411b-9edd-9fdd7d6bbcf7",space_name="notifications-with-ui",state_current="STAGING_STARTED"} 1024
cf_app_usage_events_memory_in_mb_per_instance_current{app_guid="e22762ca-891f-406d-8d73-da7c027f0f58",app_name="nfsbroker",host="jump",organization_guid="6d496114-f7d9-416e-9820-5bd14e0a3858",space_guid="f25ff7ef-06a1-44f8-b0f5-957e606f17e7",space_name="nfs",state_current="STAGING_STARTED"} 1024
cf_app_usage_events_memory_in_mb_per_instance_current{app_guid="ebd1a08c-09e5-46e6-a8ea-e9fb4fd67028",app_name="app-31216",host="jump",organization_guid="6d496114-f7d9-416e-9820-5bd14e0a3858",space_guid="c48c9fbd-14c7-4166-85fb-4d97327ab372",space_name="space-5745",state_current="STAGING_STARTED"} 1024
# HELP cf_app_usage_events_memory_in_mb_per_instance_previous Telegraf collected metric
# TYPE cf_app_usage_events_memory_in_mb_per_instance_previous untyped
cf_app_usage_events_memory_in_mb_per_instance_previous{app_guid="00432c36-b10d-4ac1-858c-2adeaca17dc1",app_name="autoscale",host="jump",organization_guid="6d496114-f7d9-416e-9820-5bd14e0a3858",space_guid="9da31a1e-1507-44b4-bbec-241e60aa360c",space_name="autoscaling",state_current="STAGING_STARTED"} 1024
cf_app_usage_events_memory_in_mb_per_instance_previous{app_guid="4f9a7c5d-5f8f-480e-87b4-7df3ecc0709a",app_name="apps-manager-js-green",host="jump",organization_guid="6d496114-f7d9-416e-9820-5bd14e0a3858",space_guid="e793e930-5ac6-4785-a120-eb37a4f81d44",space_name="system",state_current="STAGING_STARTED"} 1024
cf_app_usage_events_memory_in_mb_per_instance_previous{app_guid="565637ce-d8dd-4284-b44d-83b14decc939",app_name="app-usage-scheduler",host="jump",organization_guid="6d496114-f7d9-416e-9820-5bd14e0a3858",space_guid="e793e930-5ac6-4785-a120-eb37a4f81d44",space_name="system",state_current="STARTED"} 1024
cf_app_usage_events_memory_in_mb_per_instance_previous{app_guid="832b3991-760d-4f48-95db-4f91701de210",app_name="app-usage-server",host="jump",organization_guid="6d496114-f7d9-416e-9820-5bd14e0a3858",space_guid="e793e930-5ac6-4785-a120-eb37a4f81d44",space_name="system",state_current="STARTED"} 1024
cf_app_usage_events_memory_in_mb_per_instance_previous{app_guid="97d24286-88a9-45dc-ba4c-0245fe9f11d4",app_name="app-usage-worker",host="jump",organization_guid="6d496114-f7d9-416e-9820-5bd14e0a3858",space_guid="e793e930-5ac6-4785-a120-eb37a4f81d44",space_name="system",state_current="STARTED"} 2048
cf_app_usage_events_memory_in_mb_per_instance_previous{app_guid="9fde6c0e-f748-46e1-87f0-65587a2ff558",app_name="autoscale-api",host="jump",organization_guid="6d496114-f7d9-416e-9820-5bd14e0a3858",space_guid="9da31a1e-1507-44b4-bbec-241e60aa360c",space_name="autoscaling",state_current="STAGING_STARTED"} 1024
cf_app_usage_events_memory_in_mb_per_instance_previous{app_guid="b947616d-f461-469b-96fd-27e8da9f11b6",app_name="search-server-green",host="jump",organization_guid="6d496114-f7d9-416e-9820-5bd14e0a3858",space_guid="e793e930-5ac6-4785-a120-eb37a4f81d44",space_name="system",state_current="STAGING_STARTED"} 1024
cf_app_usage_events_memory_in_mb_per_instance_previous{app_guid="c44721bf-d60c-4b48-9b12-694029796c04",app_name="p-invitations-green",host="jump",organization_guid="6d496114-f7d9-416e-9820-5bd14e0a3858",space_guid="e793e930-5ac6-4785-a120-eb37a4f81d44",space_name="system",state_current="STAGING_STARTED"} 1024
cf_app_usage_events_memory_in_mb_per_instance_previous{app_guid="db453a87-ca42-4b38-90c6-5e457254ab67",app_name="notifications-ui",host="jump",organization_guid="6d496114-f7d9-416e-9820-5bd14e0a3858",space_guid="edf5f169-56cf-411b-9edd-9fdd7d6bbcf7",space_name="notifications-with-ui",state_current="STAGING_STARTED"} 1024
cf_app_usage_events_memory_in_mb_per_instance_previous{app_guid="e22762ca-891f-406d-8d73-da7c027f0f58",app_name="nfsbroker",host="jump",organization_guid="6d496114-f7d9-416e-9820-5bd14e0a3858",space_guid="f25ff7ef-06a1-44f8-b0f5-957e606f17e7",space_name="nfs",state_current="STAGING_STARTED"} 1024
cf_app_usage_events_memory_in_mb_per_instance_previous{app_guid="ebd1a08c-09e5-46e6-a8ea-e9fb4fd67028",app_name="app-31216",host="jump",organization_guid="6d496114-f7d9-416e-9820-5bd14e0a3858",space_guid="c48c9fbd-14c7-4166-85fb-4d97327ab372",space_name="space-5745",state_current="STAGING_STARTED"} 1024
```
