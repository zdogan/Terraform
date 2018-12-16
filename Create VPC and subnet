provider "aws" {
  region     = "us-east-2"
}
resource "aws_vpc" "main" {
  cidr_block       = "10.0.0.0/16"
  instance_tenancy = "default"

  tags {
    Name = "main"
  }
}
resource "aws_subnet" "example" {
  vpc_id            = "${aws_vpc.main.id}"
  availability_zone = "us-east-2a"
  cidr_block        = "10.0.1.0/24"

  tags {
    Name = "Subnet1"
  }

}
