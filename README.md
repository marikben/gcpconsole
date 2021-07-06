# gcpconsole
Get all the Virtual Machines (aka Compute Engines) from all the projects in an organization

for PROJECT in $(\ <br>
  gcloud projects list \ <br>
  --format="value(PROJECT_ID)") <br>
do <br>
  echo "Project: ${PROJECT}" <br>
  echo "Compute Engine instances" <br>
  gcloud compute instances list --project=${PROJECT} <br>
done <br>
