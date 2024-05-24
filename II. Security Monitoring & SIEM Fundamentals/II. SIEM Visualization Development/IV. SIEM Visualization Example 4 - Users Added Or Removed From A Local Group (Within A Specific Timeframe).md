# SIEM Visualization Example 4: Users Added Or Removed From A Local Group (Within A Specific Timeframe)

In this SIEM visualization example, we aim to create a visualization to monitor user additions or removals from the local "Administrators" group from March 5th 2023 to date.

Our visualization will be based on the following Windows event logs.

- 4732: A member was added to a security-enabled local group
- 4733: A member was removed from a security-enabled local group

## Steps

1. Navigate to http://[Target IP]:5601, click on the side navigation toggle, and click on "Dashboard".

2. Click on the "pencil"/edit icon.

3. Click on the "Create visualization" button.

4. On the new window, notice the following:

- A filter option to filter data (in this case, event IDs 4732 and 4733, and local group "Administrators").
- The "Index pattern" field to specify the data set (in this case, `windows*`).
- A search bar to verify the presence of a specific field (in this case, `user.name.keyword`).
- A drop-down menu to select the visualization type (in this case, "Table").

5. Configure the "Rows" settings as follows:

- `winlog.event_data.MemberSid.keyword` (to show which user was added/removed)
- `group.name.keyword` (to show the group name, i.e., "Administrators")
- `event.action.keyword` (to show whether the user was added or removed)
- `host.name.keyword` (to show the machine where the action occurred)

6. In the "Metrics" window, select "count" as the desired metric.

7. Click "Save and return".

8. To narrow the scope to a specific timeframe (March 5th 2023 to date):

- Click the "Edit Visualization" button.
- Add a filter for `@timestamp` greater than or equal to `2023-03-05T00:00:00.000Z`.

9. Click "Save" to persist the changes.

Please allow 3-5 minutes for Kibana to become available after spawning the target of the questions below.
