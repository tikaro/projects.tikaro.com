This repository holds the files for a portfolio site currently hosted through Google Cloud Storage and visible at http://projects.tikaro.com

I'm using this site as a way to learn Google's [Material Design Lite](https://getmdl.io/).

##Deploying
I'm currently using `gsutil` to deploy via the command line

To [sync the contents](https://cloud.google.com/storage/docs/gsutil/commands/rsync) of the local directory to the remote bucket:
`gsutil -m rsync -d -r ~/code/projects.tikaro.com gs://projects.tikaro.com`

To [grant read access](https://cloud.google.com/storage/docs/gsutil/commands/acl#ch-examples) to all users:
`gsutil acl ch -u AllUsers:R gs://projects.tikaro.com`