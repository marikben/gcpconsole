# gcpconsole
Get all the Virtual Machines (aka Compute Engines) from all the projects in an organization

for PROJECT in $(\ <br>
  gcloud projects list \
  --format="value(PROJECT_ID)")
do
  echo "Project: ${PROJECT}"
  echo "Compute Engine instances"
  gcloud compute instances list --project=${PROJECT}
done
