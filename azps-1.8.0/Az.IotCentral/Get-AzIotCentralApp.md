---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/get-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
ms.openlocfilehash: a58be60e10be53c1251d8efac5d5fc1551182043
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916521"
---
# Get-AzIotCentralApp

## Sammanfattning
Hämtar egenskaper för antingen en eller flera IoT Central program.

## FRÅGESYNTAXEN

### ListIotCentralAppsParameterSet (standard)
```
Get-AzIotCentralApp [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### InteractiveIotCentralParameterSet
```
Get-AzIotCentralApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceIdParameterSet
```
Get-AzIotCentralApp -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Hämtar metadata för antingen ett specifikt IoT Central program, eller alla program i en resurs grupp eller ett abonnemang, beroende på parameter uppsättning. 

## BESKRIVS

### Exempel 1 skaffa specifika IoT Central program.
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

Hämtar metadata för det angivna IoT Central programmet.

Exempel på utdata:

ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName namn: MyAppResourceName typ: Microsoft. IoTCentral/IoTApps plats: taggen för västkusten: {[Key, val]} SKU: Microsoft. Azure. commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXXXXXXXXXX:: för att visa namnet under domän: MyAppSubdomain Template: XXXXXXXX-XXXX- iotc-default@1.0.0 xxxx-ResourceGroupName: MyResourceGroupName

### Exempel 2 få IoT Central program i abonnemanget.
```powershell
PS C:\> Get-AzIotCentralApp
```

Hämtar metadata för alla IoT Central program i det aktuella abonnemanget.

Exempel på utdata:

ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName namn: MyAppResourceName typ: Microsoft. IoTCentral/IoTApps plats: taggen för västkusten: {[Key, val]} SKU: Microsoft. Azure. commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXXXXXXXXXX:: för att visa namnet under domän: MyAppSubdomain Template: XXXXXXXX-XXXX- iotc-default@1.0.0 xxxx-ResourceGroupName: MyResourceGroupName

ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName2 namn: MyAppResourceName2 typ: Microsoft. IoTCentral/IoTApps Location: taggen väst: {[Key, val]} SKU: Microsoft. Azure. kommandon. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: mitt eget visnings namn 2 under domän: MyAppSubdomain2-mallen: iotc-default@1.0.0 SubscriptionId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName: MyResourceGroupName2

### Exempel 3 skaffa IoT Central program i resurs gruppen.
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName"
```

Hämtar metadata för alla IoT Central program i resurs gruppen.

Exempel på utdata:

ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName namn: MyAppResourceName typ: Microsoft. IoTCentral/IoTApps plats: taggen för västkusten: {[Key, val]} SKU: Microsoft. Azure. commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXXXXXXXXXX:: för att visa namnet under domän: MyAppSubdomain Template: XXXXXXXX-XXXX- iotc-default@1.0.0 xxxx-ResourceGroupName: MyResourceGroupName

ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName2 namn: MyAppResourceName2 typ: Microsoft. IoTCentral/IoTApps Location: taggen väst: {[Key, val]} SKU: Microsoft. Azure. kommandon. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: mitt eget visnings namn 2 under domän: MyAppSubdomain2-mallen: iotc-default@1.0.0 SubscriptionId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName: MyResourceGroupName

## MALLPARAMETRAR

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namn
Namnet på IoT Central program resursen.

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Namnet på resurs gruppen.

```yaml
Type: System.String
Parameter Sets: ListIotCentralAppsParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
IoT Central program resurs-ID.

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String

## VÄRDEN

### Microsoft. Azure. commands. IotCentral. Models. PSIotCentralApp

## ANMÄRKNINGAR

## RELATERADE LÄNKAR
