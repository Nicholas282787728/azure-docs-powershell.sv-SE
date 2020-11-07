---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzProviderOperation.md
ms.openlocfilehash: 21e1af2a36478f2e0b8e470660d0fbe2539a396e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924009"
---
# Get-AzProviderOperation

## Sammanfattning
Hämtar de åtgärder för en Azure-adressresurs som är skyddade med Azure RBAC.

## FRÅGESYNTAXEN

```
Get-AzProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Get-AzProviderOperation får de operationer som tillhandahålls av Azure Resource providers.
Operationer kan skapas för att skapa anpassade roller i Azure RBAC.
Kommandot tar sig en gång i Sök strängen (med möjliga jokertecken ( *)-tecken) som avgör vilka verksamhets uppgifter som ska visas. Använd Get-AzProviderOperation * för att få alla funktioner för alla Azure Resource-leverantörer. Använd Get-AzProviderOperation Microsoft. Compute/* för att få alla funktioner i Microsoft. Compute Resource Provider.

## BESKRIVS

### Få alla åtgärder för alla providrar
```
PS C:\> Get-AzProviderOperation *
```

### Få instruktioner för en viss resurs leverantör
```
PS C:\> Get-AzProviderOperation Microsoft.Insights/*
```

### Hämta alla åtgärder som kan utföras på virtuella datorer
```
PS C:\> Get-AzProviderOperation */virtualMachines/*
```

## MALLPARAMETRAR

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OperationSearchString
Sök strängen för åtgärden (med möjliga jokertecken (*))

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: "*"
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String
Parametrar: OperationSearchString (ByValue)

## VÄRDEN

### Microsoft. Azure. commands. Resources. Models. PSResourceProviderOperation

## ANMÄRKNINGAR
Nyckelord: Azure, AZ, arm, resurs, hantering, chef, resurs, grupp, Mall, distribution

## RELATERADE LÄNKAR
