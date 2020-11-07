---
external help file: Microsoft.Azure.Commands.IotCentral.dll-Help.xml
Module Name: AzureRM.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iotcentral/get-azurermiotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Get-AzureRmIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Get-AzureRmIotCentralApp.md
ms.openlocfilehash: fdf674b5ec2dfcefe8fcada92cfaf0fd1073f7f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758185"
---
# Get-AzureRmIotCentralApp

## Sammanfattning
Hämtar egenskaper för antingen en eller flera IoT Central program.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### ListIotCentralAppsParameterSet (standard)
```
Get-AzureRmIotCentralApp [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### InteractiveIotCentralParameterSet
```
Get-AzureRmIotCentralApp [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdParameterSet
```
Get-AzureRmIotCentralApp -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Hämtar metadata för antingen ett specifikt IoT Central program, eller alla program i en resurs grupp eller ett abonnemang, beroende på parameter uppsättning. 

## BESKRIVS

### Exempel 1 skaffa specifika IoT Central program.
```powershell
PS C:\> Get-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

Hämtar metadata för det angivna IoT Central programmet.

Exempel på utdata:

ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName namn: MyAppResourceName typ: Microsoft. IoTCentral/IoTApps plats: taggen för västkusten: {[Key, val]} SKU: Microsoft. Azure. commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXXXXXXXXXX:: för att visa namnet under domän: MyAppSubdomain Template: XXXXXXXX-XXXX- iotc-default@1.0.0 xxxx-ResourceGroupName: MyResourceGroupName

### Exempel 2 få IoT Central program i abonnemanget.
```powershell
PS C:\> Get-AzureRmIotCentralApp
```

Hämtar metadata för alla IoT Central program i det aktuella abonnemanget.

Exempel på utdata:

ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName namn: MyAppResourceName typ: Microsoft. IoTCentral/IoTApps plats: taggen för västkusten: {[Key, val]} SKU: Microsoft. Azure. commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXXXXXXXXXX:: för att visa namnet under domän: MyAppSubdomain Template: XXXXXXXX-XXXX- iotc-default@1.0.0 xxxx-ResourceGroupName: MyResourceGroupName

ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName2 namn: MyAppResourceName2 typ: Microsoft. IoTCentral/IoTApps Location: taggen väst: {[Key, val]} SKU: Microsoft. Azure. kommandon. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: mitt eget visnings namn 2 under domän: MyAppSubdomain2-mallen: iotc-default@1.0.0 SubscriptionId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName: MyResourceGroupName2

### Exempel 3 skaffa IoT Central program i resurs gruppen.
```powershell
PS C:\> Get-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName"
```

Hämtar metadata för alla IoT Central program i resurs gruppen.

Exempel på utdata:

ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName namn: MyAppResourceName typ: Microsoft. IoTCentral/IoTApps plats: taggen för västkusten: {[Key, val]} SKU: Microsoft. Azure. commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXXXXXXXXXX:: för att visa namnet under domän: MyAppSubdomain Template: XXXXXXXX-XXXX- iotc-default@1.0.0 xxxx-ResourceGroupName: MyResourceGroupName

ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName2 namn: MyAppResourceName2 typ: Microsoft. IoTCentral/IoTApps Location: taggen väst: {[Key, val]} SKU: Microsoft. Azure. kommandon. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: mitt eget visnings namn 2 under domän: MyAppSubdomain2-mallen: iotc-default@1.0.0 SubscriptionId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName: MyResourceGroupName

## MALLPARAMETRAR

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namn
Namnet på IoT Central program resursen.

```yaml
Type: String
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
Type: String
Parameter Sets: ListIotCentralAppsParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
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
Type: String
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
