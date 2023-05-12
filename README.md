# create-s3-bucket-terraform
this is s3 bucket using terraform



resource "aws_s3_bucket" "bucket1" {
  bucket = "my-bucket-12-2023"

  tags = {
    Name        = "My bucket"
    Environment = "Dev"
  }
}

resource "aws__bucket_object" "object"  {
bucket  = "my-bucket-12-2023"
key =  "vpc1"
source = "c://users/hp//documents//vpc1.txt"
}
terraform plan
terraform apply
upload multiple files using terraform

resource "null_resource" "multiple" {
  provisioner "local-exec" {
    command = "aws s3 sync D :// misc s3://"my-bucket-12-2023"
  }
}

save

terraform apply -auto -apporve

















terraform init
terraform plan
terraform apply -auto -approve
bucket create completed check to the aws account

