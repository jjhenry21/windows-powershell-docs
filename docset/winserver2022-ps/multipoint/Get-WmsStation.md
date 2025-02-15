---
description: Use this topic to help manage Windows and Windows Server technologies with Windows PowerShell.
external help file: MultiPoint.dll-Help.xml
Module Name: MultiPoint
ms.date: 12/20/2016
online version: https://docs.microsoft.com/powershell/module/multipoint/get-wmsstation?view=windowsserver2022-ps&wt.mc_id=ps-gethelp
schema: 2.0.0
title: Get-WmsStation
---

# Get-WmsStation

## SYNOPSIS
Gets station information.

## SYNTAX

### GetById
```
Get-WmsStation [-StationId] <UInt32[]> [-Server <String>] [<CommonParameters>]
```

### GetAll
```
Get-WmsStation [-All] [-Server <String>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-WmsStation** cmdlet gets information for the specified station or for all stations.

## EXAMPLES

### Example 1: Get information for all stations
```
PS C:\> Get-WmsStation -All
StationId         : 1
Name              : 1
IsAutoLogOn       : False
IsSplit           : False
CollabId          : 0
RemoteConnectionServerName   : 
VirtualMachineName           :  
VirtualMachineId  : 
AutoLogOnUserName :  
AutoLogOnPassword : 
DeviceTypes       : {DT_Keyboard, DT_Mouse, DT_Audio, DT_Image...} 
DeviceCounts      : {1, 0, 0, 0...} 
ComputerName      : Test1
SessionId         : 3
SessionHostServer  : Test1
DisplayOrientation : Landscape
```

This command gets MultiPoint Server station information, along with the remote desktop session ID, if a session is associated with it.

If no session is associated with the station, 4294967295 is returned as the session ID.

## PARAMETERS

### -All
Indicates that this operation applies to all sessions on the target host.

```yaml
Type: SwitchParameter
Parameter Sets: GetAll
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Server
Specifies the fully qualified host name of the MultiPoint Server that is the target of the command.
The default is localhost.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ComputerName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StationId
Specifies an array of station IDs.

```yaml
Type: UInt32[]
Parameter Sets: GetById
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.UInt32[]

### System.String

## OUTPUTS

### Microsoft.WindowsServerSolutions.MultipointServer.PowerShell.Commands.Library.WmsStation

## NOTES

## RELATED LINKS

[Clear-WmsStation](./Clear-WmsStation.md)

[Join-WmsStation](./Join-WmsStation.md)

[Set-WmsStation](./Set-WmsStation.md)

[Split-WmsStation](./Split-WmsStation.md)

[Update-WmsStation](./Update-WmsStation.md)

