---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azdatalakegen2itemaclobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemAclObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemAclObject.md
ms.openlocfilehash: 209cb5ded738faabfdafc113d3d9524f7c01e927
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100253532"
---
# Set-AzDataLakeGen2ItemAclObject

## SYNOPSIS
Skapar/uppdaterar ett DataLake gen2-objekt med ACL-objekt, som kan användas Update-AzDataLakeGen2Item en cmdlet.

## SYNTAX

```
Set-AzDataLakeGen2ItemAclObject [-EntityId <String>] [-DefaultScope] -Permission <String>
 [-InputObject <PSPathAccessControlEntry[]>] -AccessControlType <AccessControlType> [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Set-AzDataLakeGen2ItemAclObject** skapar/uppdaterar ett ACL-objekt med DataLake gen2 som kan användas i Update-AzDataLakeGen2Item cmdlet.
Om den nya ACL-posten med samma AccessControlType/EntityId/DefaultScope inte finns i indata-ACL skapas en ny ACL-post. Då uppdateras behörigheten för den befintliga ACL-posten.

## EXEMPEL

### Exempel 1: Skapa ett ACL-objekt med 3 ACL-post och uppdatera ACL i en katalog
```
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx -DefaultScope
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\>Update-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/dir3" -ACL $acl

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir3            True                         2020-03-23 09:34:31Z rwxrw-rw-+   $superuser           $superuser
```

Det här kommandot skapar ett ACL-objekt med 3 ACL-poster (använd -InputObject-parameter för att lägga till encl-post i befintliga acl-objekt) och uppdaterar ACL i en katalog.

### Exempel 2: Skapa ett ACL-objekt med 4 ACL-poster och uppdatera behörigheten för en befintlig ACL-post
```
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx -DefaultScope
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission rwx -InputObject $acl 
PS C:\>$acl

DefaultScope AccessControlType EntityId                             Permissions
------------ ----------------- --------                             -----------
True         User                                                   rwx        
False        Group                                                  rw-        
False        Other                                                  rw-        
False        User              ********-****-****-****-************ rwx        

PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission r-x -InputObject $acl 
PS C:\>$acl  

DefaultScope AccessControlType EntityId                             Permissions
------------ ----------------- --------                             -----------
True         User                                                   rwx        
False        Group                                                  rw-        
False        Other                                                  rw-        
False        User              ********-****-****-****-************ r-x
```

Det här kommandot skapar först ett ACL-objekt med 4 ACL-poster och kör sedan cmdleten igen med annan behörighet men samma AccessControlType/EntityId/DefaultScope för en befintlig ACL-post.
Sedan uppdateras behörigheten för ACL-posten, men ingen ny ACL-post läggs till.

## PARAMETERS

### -AccessControlType
Det finns fyra typer: "användare" beviljar rättigheter till ägaren eller en namngiven användare, "grupp" beviljar rättigheter till den egna gruppen eller en namngiven grupp, "mask" begränsar rättigheter som ges till namngivna användare och medlemmar i grupper, och "andra" beviljar rättigheter till alla användare som inte finns i någon av de andra posterna.

```yaml
Type: Azure.Storage.Files.DataLake.Models.AccessControlType
Parameter Sets: (All)
Aliases:
Accepted values: User, Group, Mask, Other

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultScope
Ange den här parametern för att ange att ACE tillhör standard-ACL för en katalog. i annat fall är omfattningen implicit och ACE hör till åtkomst-ACL.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EntityId
Identifierare för användare eller grupp.
Den utelämnas för posterna "mask" och "annan" i AccessControlType.
Användar- eller gruppidentifieraren utelämnas också för ägaren och ägargruppen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Om du matar in PSPathAccessControlEntry-objektet, lägger du till den nya ACL som ett nytt element i \[ \] inmatningsobjektet PSPathAccessControlEntry. \[ \]

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Behörighet
Behörighetsfältet är en 3-teckenssekvens där det första tecknet är "r" för att tilldela läsbehörighet, det andra tecknet är "w" för att tilldela skrivåtkomst och det tredje tecknet är "x" för att tilldela behörighet att utföra.
Om åtkomst inte beviljas används tecknet "-" för att ange att behörigheten nekas.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### Ingen

## UTDATA

### Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry

## ANTECKNINGAR

## RELATERADE LÄNKAR
