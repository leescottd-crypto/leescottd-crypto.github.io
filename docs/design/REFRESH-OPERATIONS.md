# Dashboard refresh repair — October 2, 2026

The LaunchAgent runs at 06:00, 12:00 and 17:00 in the Mac local timezone. It needs the Mac awake and logged in. This is not an always-on cloud schedule.

Data refresh succeeded but public publishing failed starting September 29 at 17:00: GitHub authenticated as scotthexxy-sketch instead of the repository owner, leescottd-crypto.

The local publisher at ~/.hermes/bin/multi-asset-dashboard-publish.sh now obtains the existing repository-owner login for each Git operation without changing the global active account. Credentials are supplied through process environment and never written to source or logs. It pulls the current public source before syncing only public/data, preserves approved UI styling, and pushes previously pending commits even if the data has not changed. A pre-repair backup was retained beside the script.

Inspect ~/.hermes/logs/multi-asset-cycle-dashboard/refresh.log and publish.log independently. Refresh success alone does not mean publication succeeded. Validate the Pages build and the public assets.json after publication.
