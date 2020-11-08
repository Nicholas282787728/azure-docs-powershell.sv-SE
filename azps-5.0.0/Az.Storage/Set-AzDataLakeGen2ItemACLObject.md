---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azdatalakegen2itemaclobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemACLObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemACLObject.md
ms.openlocfilehash: d16a476bea988afb53ddff7b34a83658e0f274e1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269011"
---
# Set-AzDataLakeGen2ItemAclObject

## Sammanfattning
Skapar/uppdaterar ett DataLake-Gen2 objekt, som kan användas i Update-AzDataLakeGen2Item cmdlet.

## FRÅGESYNTAXEN

```
Set-AzDataLakeGen2ItemAclObject [-EntityId <String>] [-DefaultScope] -Permission <String>
 [-InputObject <PSPathAccessControlEntry[]>] -AccessControlType <AccessControlType> [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **set-AzDataLakeGen2ItemAclObject** skapar/uppdaterar ett DataLake-objekt, som kan användas i Update-AzDataLakeGen2Item cmdlet.
Om den nya ACL-posten med samma AccessControlType/EntityId/DefaultScope inte finns i indata-ACL: en skapar en ny ACL-post, annars kan du uppdatera behörigheten för befintlig ACL-post.

## BESKRIVS

### Exempel 1: skapa ett ACL-objekt med 3 ACL-post och uppdatera ACL för en katalog
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

Det här kommandot skapar ett ACL-objekt med 3 ACL-poster (Use-InputObject-parametern för att lägga till ACL-posten i befintligt ACL-objekt) och uppdatera ACL för en katalog.

### Exempel 2: skapa ett ACL-objekt med 4 ACL-poster och uppdatera behörighet för en befintlig ACL-post
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

Det här kommandot skapar först ett ACL-objekt med 4 ACL-poster och kör cmdleten igen med olika behörigheter men samma AccessControlType/EntityId/DefaultScope för en befintlig ACL-post.
Behörigheten för ACL-posten uppdateras men ingen ny ACL-post läggs till.

## MALLPARAMETRAR

### -AccessControlType
Det finns fyra typer: "användare" ger rättigheter till ägaren eller en namngiven användare, "grupp" ger rättigheterna till den ägande gruppen eller en namngiven grupp, "mask" begränsar rättigheterna till namngivna användare och medlemmar i grupper och "Övrigt" ger rättigheter till alla användare som inte finns i någon av de andra posterna.

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
Ange den här parametern för att ange ACE tillhör standard åtkomst kontroll för en katalog; i övrigt är omfattningen implicit och ACE: en åtkomst kontrol lista.

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
ID för användaren eller gruppen.
Den utelämnas för AccessControlType "mask" och "Övrigt".
Användarens eller gruppens identifierare utelämnas också för gruppen ägare och ägande.

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
Om du anger PSPathAccessControlEntry \[ \] -objektet läggs den nya åtkomst kontrol listan till som ett nytt element i PSPathAccessControlEntry- \[ \] objektet.

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

### -Tillstånd
Behörighets fältet är en sekvens med 3 tecken där det första tecknet är "r" för att bevilja Läs åtkomst, det andra tecknet är "w" för att ge skriv åtkomst och det tredje tecknet är "x" för att ge behörigheten Kör.
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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen

## VÄRDEN

### Microsoft. WindowsAzure. commands. Storage. Model. ResourceModel. PSPathAccessControlEntry

## ANMÄRKNINGAR

## RELATERADE LÄNKAR
