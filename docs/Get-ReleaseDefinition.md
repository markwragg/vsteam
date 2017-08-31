---
external help file: Team-Help.xml
Module Name: 
online version: 
schema: 2.0.0
---

# Get-ReleaseDefinition

## SYNOPSIS
Gets the release defintions for a team project.

## SYNTAX

### UNNAMED_PARAMETER_SET_1
```
Get-ReleaseDefinition [-ProjectName] <String> [-Expand <String>]
```

### UNNAMED_PARAMETER_SET_2
```
Get-ReleaseDefinition [-ProjectName] <String> [-Id <Int32[]>]
```

## DESCRIPTION
The Get-ReleaseDefinition function gets the release defintions for a team
project.
The project name is a Dynamic Parameter which may not be displayed
in the syntax above but is mandatory.

With just a project name, this function gets all of the release definitions
for that team project.
You can also specify a particular release defintion
by ID.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
Get-ReleaseDefinition -ProjectName demo | Format-List *
```

This command gets a list of all release definitions in the demo project.
The
pipeline operator (|) passes the data to the Format-List cmdlet, which
displays all available properties (*) of the release defintion objects.

## PARAMETERS

### -ProjectName
Specifies the team project for which this function operates.

You can tab complete from a list of available projects.

You can use Set-DefaultProject to set a default project so
you do not have to pass the ProjectName with each call.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Expand
Specifies which property should be expanded in the list of Release
Definition (environments, artifacts, none).

```yaml
Type: String
Parameter Sets: UNNAMED_PARAMETER_SET_1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id
Specifies one or more release defintions by ID.
To specify multiple IDs, use
commas to separate the IDs.
To find the ID of a release defintion, type
Get-ReleaseDefinition.

```yaml
Type: Int32[]
Parameter Sets: UNNAMED_PARAMETER_SET_2
Aliases: ReleaseDefinitionID

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## INPUTS

### Int[]

## OUTPUTS

### Team.ReleaseDefinition

## NOTES

## RELATED LINKS

[Add-TeamAccount]()

[Set-DefaultProject]()

[Add-ReleaseDefinition]()

[Remove-ReleaseDefinition]()
