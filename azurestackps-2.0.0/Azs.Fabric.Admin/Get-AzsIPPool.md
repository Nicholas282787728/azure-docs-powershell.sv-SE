---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsippool
schema: 2.0.0
ms.openlocfilehash: 532dcd2a91591b639b93b5b67851a4118457068b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923193"
---
# Get-AzsIPPool

## Sammanfattning
Returnera den begärda IP-poolen.

## FRÅGESYNTAXEN

### Lista (standard)
```
Get-AzsIPPool [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### Lära
```
Get-AzsIPPool -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzsIPPool -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Returnera den begärda IP-poolen.

## BESKRIVS

### Exempel 1: 
```powershell
PS C:\> Get-AzsIpPool

Return an all infrastructure ip pools.
```

Skaffa en IP-pool för alla infrastrukturer.

### Exempel 2: 
```powershell
PS C:\> Get-AzsIpPool -Name "08786a0f-ad8c-43aa-a154-06083abfc1ac"

Get an infrastructure ip pool based on name.
```

Skaffa en IP-adresspool för infrastruktur baserat på namn.

## MALLPARAMETRAR

### -DefaultProfile


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
Parametern OData filter.

```yaml
Type: System.String
Parameter Sets: List
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
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### -Plats
Plats för resursen.

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### -Namn
IP-poolnamn.

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -PassThru
Returnerar true när kommandot lyckas

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

### -ResourceGroupName
Namnet på resurs gruppen.

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### -SubscriptionId
Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.
Prenumerations-ID: t utgör en del av URI: n för varje service samtal.

```yaml
Type: System.String[]
Parameter Sets: Get, List
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

### Microsoft. Azure. PowerShell. cmdletar. FabricAdmin. Models. IFabricAdminIdentity

## VÄRDEN

### Microsoft. Azure. PowerShell. cmdletar. FabricAdmin. Models. Api20160501. IIPPool



## ANMÄRKNINGAR

KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper. Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.

INPUTOBJECT <IFabricAdminIdentity> : identitets parameter
  - `[Drive <String>]`: Lagrings enhetens namn.
  - `[EdgeGateway <String>]`: Namnet på Edge Gateway.
  - `[EdgeGatewayPool <String>]`: Namnet på Edge Gateway-poolen.
  - `[FabricLocation <String>]`: Fabric-plats.
  - `[FileShare <String>]`: Fil resurs namn för Fabric.
  - `[IPPool <String>]`: IP-poolnamn.
  - `[Id <String>]`: Sökväg till resurs identitet
  - `[InfraRole <String>]`: Infrastruktur roll namn.
  - `[InfraRoleInstance <String>]`: Namnet på en infrastruktur roll instans.
  - `[Location <String>]`: Resursens plats.
  - `[LogicalNetwork <String>]`: Namnet på det logiska nätverket.
  - `[LogicalSubnet <String>]`: Namnet på det logiska under nätet.
  - `[MacAddressPool <String>]`: MAC-adresspoolen namn.
  - `[Operation <String>]`: Åtgärds-ID.
  - `[ResourceGroupName <String>]`: Resurs gruppens namn.
  - `[ScaleUnit <String>]`: Enhetens namn.
  - `[ScaleUnitNode <String>]`: Namnet på noden för Scale Unit.
  - `[SlbMuxInstance <String>]`: Namnet på en SLB MUX-instans.
  - `[StoragePool <String>]`: Namn på lagringspool.
  - `[StorageSubSystem <String>]`: Lagrings systemets namn.
  - `[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget. Prenumerations-ID: t utgör en del av URI: n för varje service samtal.
  - `[Volume <String>]`: Lagrings volymens namn.

## RELATERADE LÄNKAR

