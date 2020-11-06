---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: B5CA6FD9-49EE-4115-8477-551CE5D8E6CE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: dc8a1e6cfe8c3d68af0f8c413a0e96cac9feaee8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579360"
---
# Get-AzureRmSiteRecoveryJob

## Sammanfattning
Hämtar åtgärds informationen för det aktuella Site Recovery-valvet.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### ByParam (standard)
```
Get-AzureRmSiteRecoveryJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByName
```
Get-AzureRmSiteRecoveryJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByObject
```
Get-AzureRmSiteRecoveryJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureRmSiteRecoveryJob** får Azure Site Recovery-jobb.
Du kan använda denna cmdlet för att Visa åtgärds informationen för det aktuella Site Recovery-valvet.

## BESKRIVS

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

### -Slut tid
Anger slut tiden för jobben.
Denna cmdlet hämtar alla jobb som startade före angiven tid.
Om du vill hämta ett **datetime** -objekt för den här parametern använder du Get-Date cmdlet.
Om du vill ha mer information skriver du `Get-Help Get-Date` .

```yaml
Type: DateTime
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Jobb
Anger återställnings jobbet för webbplatsen.

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Namn
Anger ett unikt namn som identifierar jobbet.

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartTime
Anger start tiden för jobben.
Denna cmdlet hämtar alla jobb som startas efter den angivna tiden.

```yaml
Type: DateTime
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -State
Anger inmatnings läget för ett webbplats återställnings jobb.
Denna cmdlet hämtar alla jobb som matchar det angivna tillståndet.
De acceptabla värdena för den här parametern är:

- NotStarted
- Inaktive
- Utför
- Övrigt
- Startade
- Annullerats
- Hängande

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 
Accepted values: NotStarted, InProgress, Succeeded, Other, Failed, Cancelled, Suspended

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetObjectId
Anger ID för det objekt som är inriktat för jobbet.

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### ASRJob
Parametern ' Job ' godkänner värdet av typen ' ASRJob ' från pipeline

## VÄRDEN

### System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRJob]

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Restart-AzureRmSiteRecoveryJob](./Restart-AzureRmSiteRecoveryJob.md)

[Resume-AzureRmSiteRecoveryJob](./Resume-AzureRmSiteRecoveryJob.md)

[Stopp-AzureRmSiteRecoveryJob](./Stop-AzureRmSiteRecoveryJob.md)
