---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D79080D5-2785-4C46-86FD-FDAA11117D17
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: fb600edb4fd8d18ee82cb7f83d651e6588acaa42
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98520144"
---
# Get-AzDataLakeStoreTrustedIdProvider

## Sammanfattning
Hämtar den angivna betrodda identitets leverantören i den angivna data Lake Store.
Om ingen leverantör anges visas alla providrar för kontot.

## FRÅGESYNTAXEN

```
Get-AzDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzDataLakeStoreTrustedIdProvider** hämtar den angivna betrodda identitets leverantören i den angivna data Lake Store.
Om ingen leverantör anges visas alla providrar för kontot.

## BESKRIVS

### Exempel 1: skaffa en särskild betrodd identitets leverantör
```
PS C:\> Get-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

Returnerar leverantören med namnet "$" från kontot "ContosoADL"

### Exempel 2: lista alla leverantörer i ett konto
```
PS C:\> Get-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL"
```

Visar alla leverantörer under kontot "ContosoADL"

## MALLPARAMETRAR

### -Konto
Data Lake Store-konto för att hämta den betrodda identitets leverantören

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure

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
Namnet på den betrodda identitets leverantör som ska hämtas

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Namn på resurs gruppen som du vill hämta angivet konto för betrodd identitets leverantör för.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String

## VÄRDEN

### Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStoreTrustedIdProvider

## ANMÄRKNINGAR

## RELATERADE LÄNKAR
