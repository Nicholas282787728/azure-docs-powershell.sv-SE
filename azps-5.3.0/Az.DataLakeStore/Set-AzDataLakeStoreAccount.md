---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 0EB5C25C-D0A1-4444-AEA2-C963D5069CFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreAccount.md
ms.openlocfilehash: 15a99d07630f6060473f66f985cfa8b8bf06d1e4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98520092"
---
# Set-AzDataLakeStoreAccount

## Sammanfattning
Ändrar ett data Lake Store-konto.

## FRÅGESYNTAXEN

```
Set-AzDataLakeStoreAccount [-Name] <String> [[-DefaultGroup] <String>] [[-Tag] <Hashtable>]
 [[-TrustedIdProviderState] <TrustedIdProviderState>] [[-FirewallState] <FirewallState>]
 [[-ResourceGroupName] <String>] [-Tier <TierType>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-KeyVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **set-AzDataLakeStoreAccount** ändrar ett data Lake Store-konto.

## BESKRIVS

### Exempel 1: lägga till en tagg till ett konto
```powershell
PS C:\>Set-AzDataLakeStoreAccount -Name "ContosoADL" -Tags @{"stage"="production"}
```

Det här kommandot lägger till angiven tagg i kontot data Lake Store med namnet ContosoADL.

### Exempel 2

Ändrar ett data Lake Store-konto. (automatiskt genererat)

<!-- Aladdin Generated Example -->
```powershell
Set-AzDataLakeStoreAccount -FirewallState Enabled -Name 'ContosoADL'
```

## MALLPARAMETRAR

### -AllowAzureIpState
Tillåt/blockera Azure med IP-adresser via brand väggen.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.FirewallAllowAzureIpsState]
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultGroup
Anger ID för en AzureActive.
Den här gruppen är standard gruppen för filer och mappar som du skapar.

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

### -FirewallState
Aktivera eller inaktivera befintliga brand Väggs regler.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.FirewallState]
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Version
Om krypterings typen är tilldelad användaren kan användaren rotera sin huvud version med den här parametern.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namn
Anger namnet på ett data Lake Store-konto.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på den resurs grupp som innehåller det data Lake Store-konto som ska ändras.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tagg
Anger taggar som par med nyckelord.
Du kan använda taggar för att identifiera ett data Lake Store-konto från andra Azure-resurser.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tier
Önskad åtagande nivå för det här kontot.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.TierType]
Parameter Sets: (All)
Aliases:
Accepted values: Consumption, Commitment1TB, Commitment10TB, Commitment100TB, Commitment500TB, Commitment1PB, Commitment5PB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TrustedIdProviderState
Alternativt kan du aktivera eller inaktivera befintliga betrodda ID-leverantörer.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.TrustedIdProviderState]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String

### System. Collections. hash

### System. Nullable ' 1 [[Microsoft. Azure. Management. DataLake. Store. Models. TrustedIdProviderState, Microsoft. Azure. Management. DataLake. Store, version = 2.0.0.0; Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]

### System. Nullable ' 1 [[Microsoft. Azure. Management. DataLake. Store. Models. FirewallState, Microsoft. Azure. Management. DataLake. Store, version = 2.0.0.0; Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]

### System. Nullable ' 1 [[Microsoft. Azure. Management. DataLake. Store. Models. TierType, Microsoft. Azure. Management. DataLake. Store, version = 2.0.0.0; Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]

### System. Nullable ' 1 [[Microsoft. Azure. Management. DataLake. Store. Models. FirewallAllowAzureIpsState, Microsoft. Azure. Management. DataLake. Store, version = 2.0.0.0; Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]

## VÄRDEN

### Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzDataLakeStoreAccount](./Get-AzDataLakeStoreAccount.md)

[New-AzDataLakeStoreAccount](./New-AzDataLakeStoreAccount.md)

[Remove-AzDataLakeStoreAccount](./Remove-AzDataLakeStoreAccount.md)

[Test-AzDataLakeStoreAccount](./Test-AzDataLakeStoreAccount.md)


