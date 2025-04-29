# Cloud Platform Delete Old Snapshots

[![Ministry of Justice Repository Compliance Badge](https://github-community.service.justice.gov.uk/repository-standards/api/cloud-platform-delete-oldsnapshots/badge)](https://github-community.service.justice.gov.uk/repository-standards/cloud-platform-delete-oldsnapshots)

This project deletes snapshots older than 1 year, in the Cloud Platform AWS account.

## How to run

To run the application locally, you must have the following:

- An variable set called `ownerId` with the value of your AWS Account ID.
- An variable set called `awsRegion` that contains the valid AWS region.
- An variable set called `daysOld` to delete the snapshots older than given days.

Then you can run:

```bash
go run delete-oldsnapshots.go
```

## Releasing

To release a new image create a new release bumping the version number. You can then reference this tag in the [delete-old-snapshots](https://github.com/ministryofjustice/cloud-platform-terraform-concourse/blob/main/pipelines/manager/main/delete-oldsnapshots.yaml) pipeline.
