# ec2-instances-info

Golang library providing specs and pricing information about AWS EC2 instances,
based on the data that is also powering the comprehensive
[www.ec2instances.info](http://www.ec2instances.info) instance comparison
website.

## History

This used to be a part of my other project
[AutoSpotting](https://github.com/cristim/autospotting) which uses it
intensively, but I decided to extract it into a dedicated project sice it may be
useful to someone else out there.

Some data fields that were not needed in AutoSpotting may not yet be exposed but
they can be added upon demand.

## Installation or update

```text
go get -u github.com/cristim/ec2-instances-info/...
```

## Usage

```golang
import "github.com/cristim/ec2-instances-info"

data, err := ec2instancesinfo.Data() // only needed once

// This would print all the available instance type names:
for _, i := range data{
  fmt.Println("Instance type", i.InstanceType)
}
```

See the examples directory for a working code example.

## Contributing

Pull requests and feedback are welcome.