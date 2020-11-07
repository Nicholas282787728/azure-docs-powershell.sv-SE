---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/remove-azurermservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricClientCertificate.md
ms.openlocfilehash: e508afc5ab66a3e2aec49131bf2c8bf0e9d31259
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755583"
---
# Remove-AzureRmServiceFabricClientCertificate

## Sammanfattning
Ta bort ett eller flera klient certifikat eller certifikat subjekt namn som används för klientautentisering till klustret.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### SingleUpdateWithCommonName
```
Remove-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SingleUpdateWithThumbprint
```
Remove-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### MultipleUpdatesWithCommonName
```
Remove-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### MultipleUpdatesWithThumbprint
```
Remove-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Använd **Remove-AzureRmServiceFabricClientCertificate** om du vill ta bort ett eller flera klient certifikat eller certifikat subjekt namn som används för klientautentisering till klustret.

## BESKRIVS

### Exempel 1
```
PS c:> Remove-AzureRmServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

Det här kommandot tar bort klient certifikatet med tumavtrycket ' 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A ' från klustret.

## MALLPARAMETRAR

### -AdminClientThumbprint
Ange tumavtryck för klient certifikat som bara har administratörs behörighet.

```yaml
Type: String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ClientCertificateCommonName
Ange klientens allmänna namn, utfärdarens tumavtryck och autentiseringstyp.

```yaml
Type: PSClientCertificateCommonName[]
Parameter Sets: MultipleUpdatesWithCommonName
Aliases: CertCommonName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -CommonName
Ange klient certifikatets allmänna namn.

```yaml
Type: String
Parameter Sets: SingleUpdateWithCommonName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

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

### -IssuerThumbprint
Ange tumavtryck för klient certifikat utfärdare.

```yaml
Type: String
Parameter Sets: SingleUpdateWithCommonName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Namn
Ange namnet på klustret.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ReadonlyClientThumbprint
Ange tumavtryck för klient certifikat som har Skriv behörighet.

```yaml
Type: String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på resurs gruppen.

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

### -Tumavtryck
Ange tumavtryck för klient certifikat.

```yaml
Type: String
Parameter Sets: SingleUpdateWithThumbprint
Aliases: ClientCertificateThumbprint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Bekräfta
Du uppmanas att bekräfta innan du kör cmdleten.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som händer om cmdleten körs. Cmdleten körs inte.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. Collections. hash
System. String

System. Boolean

## VÄRDEN

### Microsoft. Azure. commands. ServiceFabric. Models. PsCluster

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Add-AzureRmServiceFabricClientCertificate](./Add-AzureRmServiceFabricClientCertificate.md)
