---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
ms.openlocfilehash: 5f2ccffd0b0ba82b215db018ee15f4e495704f15
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525235"
---
# Get-AzWvdApplicationGroup

## Sammanfattning
Skaffa en program grupp.

## FRÅGESYNTAXEN

### List1 (standard)
```
Get-AzWvdApplicationGroup [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### Lära
```
Get-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### Förteckning
```
Get-AzWvdApplicationGroup -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Skaffa en program grupp.

## BESKRIVS

### Exempel 1: skaffa en Windows Virtual Desktop-ApplicationGroup med namn
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName -Name ApplicationGroupName

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

Det här kommandot får en Windows-ApplicationGroup för virtuella skriv bord i en resurs grupp.

### Exempel 2: lista ApplicationGroups för virtuella skriv bord i Windows
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName

Location   Name                  Type
--------   ----                  ----
eastus     ApplicationGroupName1 Microsoft.DesktopVirtualization/applicationgroups
eastus     ApplicationGroupName2 Microsoft.DesktopVirtualization/applicationgroups
```

Det här kommandot listar en ApplicationGroups för Windows virtuella skriv bord i en resurs grupp.

## MALLPARAMETRAR

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Filter
OData filter-uttryck.
Giltiga egenskaper för filtrering är applicationGroupType.

```yaml
Type: System.String
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Namn
Namnet på program gruppen

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Namnet på resurs gruppen.
Namnet är Skift läges okänsligt.

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
ID för mål prenumerationen.

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## KOSTNADS

### Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. IDesktopVirtualizationIdentity

## VÄRDEN

### Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. Api20201102Preview. IApplicationGroup

## ANMÄRKNINGAR

ALIAS

KOMPLEXA PARAMETER EGENSKAPER

Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan. Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.


INPUTOBJECT <IDesktopVirtualizationIdentity> : identitets parameter
  - `[ApplicationGroupName <String>]`: Namnet på program gruppen
  - `[ApplicationName <String>]`: Namnet på programmet i den angivna program gruppen
  - `[DesktopName <String>]`: Namnet på Skriv bordet i angiven Skriv bords grupp
  - `[HostPoolName <String>]`: Namnet på den värdbaserade poolen i den angivna resurs gruppen
  - `[Id <String>]`: Sökväg till resurs identitet
  - `[MsixPackageFullName <String>]`: Det versions specifika paketet fullständigt namn för MSIX paketet i angivet hostpool
  - `[ResourceGroupName <String>]`: Namnet på resurs gruppen. Namnet är Skift läges okänsligt.
  - `[SessionHostName <String>]`: Namnet på sessions värden i den angivna poolen
  - `[SubscriptionId <String>]`: Mål prenumerationens ID.
  - `[UserSessionId <String>]`: Namnet på användarsessionen inom den angivna värd
  - `[WorkspaceName <String>]`: Arbets ytans namn

## RELATERADE LÄNKAR

