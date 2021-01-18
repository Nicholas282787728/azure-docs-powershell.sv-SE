---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B423C1A1-1988-4721-81E7-3B7EC163B03A
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchCertificate.md
ms.openlocfilehash: b7b3dae97e5af4b7d31edabb215ef25a32be6caf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524761"
---
# New-AzBatchCertificate

## Sammanfattning
Lägger till ett certifikat till det angivna batch-kontot.

## FRÅGESYNTAXEN

### Fil (standard)
```
New-AzBatchCertificate [-FilePath] <String> [-Password <SecureString>] [-Kind <PSCertificateKind>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### RawData
```
New-AzBatchCertificate [-RawData] <Byte[]> [-Password <SecureString>] [-Kind <PSCertificateKind>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzBatchCertificate** lägger till ett certifikat till det angivna Azure Batch-kontot.

## BESKRIVS

### Exempel 1: lägga till ett certifikat från en fil
```
PS C:\>New-AzBatchCertificate -FilePath "E:\Certificates\MyCert.cer" -BatchContext $Context
```

Det här kommandot lägger till ett certifikat till det angivna batch-kontot med hjälp av filen E:\Certificates\MyCert.cer.

### Exempel 2: lägga till ett certifikat från rå data
```
PS C:\>$RawData = [System.IO.File]::ReadAllBytes("E:\Certificates\MyCert.pfx")
PS C:\> New-AzBatchCertificate -RawData $RawData -Password "Password1234" -BatchContext $Context
```

Det första kommandot läser in data från filen med namnet "cert. pfx" i $RawData variabel.
Det andra kommandot lägger till ett certifikat till det angivna batch-kontot med hjälp av rå data som lagras i $RawData.

## MALLPARAMETRAR

### -BatchContext
Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.
Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten. Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKey cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda. När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard. Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Sökväg
Anger sökvägen till certifikat filen.
Certifikat filen måste vara i. cer-eller. PFX-format.

```yaml
Type: System.String
Parameter Sets: File
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Sort
Den typ av certifikat som ska skapas. Om det inte anges antas det att alla certifikat utan lösen ord är CER och att alla certifikat med lösen ord är PFX.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCertificateKind
Parameter Sets: (All)
Aliases:
Accepted values: Cer, Pfx

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Lösen ord
Anger lösen ordet för att komma åt certifikatets privata nycklar.
Du måste ange den här parametern om du anger ett certifikat i PFX-format.

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RawData
Anger rå data för certifikat i. cer-eller. PFX-format.

```yaml
Type: System.Byte[]
Parameter Sets: RawData
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## KOSTNADS

### System. byte []

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## VÄRDEN

### System. Void

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzBatchCertificate](./Get-AzBatchCertificate.md)

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Remove-AzBatchCertificate](./Remove-AzBatchCertificate.md)

[Cmdlets för Azure Batch](/powershell/module/Az.Batch/)
