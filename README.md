# EMR Location

# Scope
This represents a physical location within the EMR. This may be an office, a room, a bed, a chair.

# Usage
This contains a simple `Makefile` for automating validation and document generation.  
- `make test`: Validate each versioned schema against all of its example files.
- `make doc`: Compile human readable HTML documentation for each versioned schema
- `make clean`: Cleans up all generated files

# Implementation Notes
* `name` is expected to either be non-empty OR an extension would be defined that defines the reason why its missing. This reason is what gets stored in `nameAbsentReason`. The extension would look like the following in the original FHIR.
```
_name: {
  extension: [
    {
      "url": "http://hl7.org/fhir/StructureDefinition/data-absent-reason",
      "valueCode": "unknown"
    }  
  ]
}
```

# Links
- [Event Contract Management Standard](https://projectronin.atlassian.net/wiki/spaces/ENG/pages/1797521454/Event+Contract+Management+Standard)
- [Ronin Event Standard](https://projectronin.atlassian.net/wiki/spaces/ENG/pages/1748041738/Ronin+Event+Standard)
- [Event Topic Standards](https://projectronin.atlassian.net/wiki/spaces/ENG/pages/1765998701/Event+Topic+Standards)
- [Event Contract Tooling Docker Image](https://github.com/projectronin/ronin-contract-event-tooling)
- [Event Contract CI/CD Workflow](https://github.com/projectronin/github/blob/event_contract_cicd/.github/workflows/event_contract_cicd.yaml)
