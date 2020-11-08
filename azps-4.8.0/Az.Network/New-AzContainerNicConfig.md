---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-AzContainerNicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfig.md
ms.openlocfilehash: 11051c8030fb9a57b84f738ff487b00d6652749c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260749"
---
# New-AzContainerNicConfig

## Sammanfattning
Skapar ett nytt konfigurations objekt för behållarens nätverks gränssnitt.

## FRÅGESYNTAXEN

```
New-AzContainerNicConfig [-Name <String>] [-IpConfiguration <PSIPConfigurationProfile[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzContainerNicConfig** skapar ett nytt konfigurations objekt för behållaren för nätverks gränssnitt. Det här objektet bestämmer egenskaperna för behållar nätverks gränssnittet som skapas och den överordnade nätverks profilen.

## BESKRIVS

### Exempel 1
```powershell
$containerNicConfig = New-AzContainerNicConfig -Name cnicConfig1

$networkProfile = New-AzNetworkProfile -Name np1 -ResourceGroupName rg1 -Location westus -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

Det första kommandot skapar en tom konfiguration för nätverks gränssnitt för behållare. Den andra skapar en ny nätverks profil och skickar den tidigare skapade konfigurationen för nätverks gränssnitt för behållare som ett argument till New-NetworkProfile cmdlet.

### Exempel 2

Skapar ett nytt konfigurations objekt för behållarens nätverks gränssnitt. (automatiskt genererat)

<!-- Aladdin Generated Example -->
```powershell
New-AzContainerNicConfig -IpConfiguration <PSIPConfigurationProfile[]> -Name cnic
```

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

### -IpConfiguration
Insamling av IP-konfigurationsinställningar som avgör vilka IP-konfigurationer som skapas när en container-NIC instansieras från den här nätverks gränssnitts konfigurationen

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIPConfigurationProfile[]
Parameter Sets: (All)
Aliases: IpConfig

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namn
Namn på behållarens nätverks gränssnitts konfiguration.

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

### -Bekräfta
Du uppmanas att bekräfta innan du kör cmdleten.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som händer om cmdleten körs.
Cmdleten körs inte.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Microsoft. Azure. commands. Network. Models. PSIPConfigurationProfile []

## VÄRDEN

### Microsoft. Azure. commands. Networks. Models. PSContainerNetworkInterfaceConfiguration

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[New-AzContainerNicConfigIpConfig](./New-AzContainerNicConfigIpConfig.md)
